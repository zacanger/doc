# ip addresses

```
+------------------------++-----------------------+
|  ip addr1 -> 10.1.1.1  || ip addr2 -> 10.1.1.2  |
+------------------------++-----------------------+
             |                        |
             |                        |
             +------------------------+
             |
             v
  +--------------------+
  |                    |
  |       Device       |
  |                    |
  +--------------------+
```

* One device can have one or more than one ip address.

When I do `ip address` in linux, it will print out:

```shell
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2. eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:1a:b1:01 brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.15/24 brd 10.0.2.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::784:a34a:587c:970/64 scope link
       valid_lft forever preferred_lft forever
```

Here, the first `lo` is `loopback`. Can see it binds a ipv4 address `127.0.0.1`.
And `eth0` binds a address `10.0.2.15`.

### Add a address to a device

If I run `ip addr add 10.0.2.16 dev eth0`, it will add a ip address `10.0.2.16`,
to `eth0`. Show in graph:

```
+------------------------++-----------------------+
| ip addr1 -> 10.0.2.15  || ip addr2 -> 10.0.2.16*|
+------------------------++-----------------------+
             |                        |
             |                        |
             +------------------------+
             |
             v
  +--------------------+
  |                    |
  |        eth0        |
  |                    |
  +--------------------+
```

The result of the query also will looks like:

```
eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:1a:b1:01 brd ff:ff:ff:ff:ff:ff
    inet 10.0.2.15/24 brd 10.0.2.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet 10.0.2.16/32 scope global eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::784:a34a:587c:970/64 scope link
       valid_lft forever preferred_lft forever
```

The different between `inet 10.0.2.15` and `inet 10.0.2.16` is that, `10.0.2.16`,
don't have a `brd` option, and the `brd` value is `10.0.2.255`, this `brd` is
called `broadcast` address. What does it do?

#### broadcast address

Broadcast addresses are special values in the *host-identification* part of an
IP address. And it used for sending `diagrams(aka udp)` packets.

> How to calculate a broadcast address?

If a ip using a `subnet space` `172.16.0.0/12`, then its subnet mask is:

```
12 ones -> 11111111 11110000 00000000 00000000
then invert it
           00000000 00001111 11111111 11111111
```

the binary ip is:

```
172.16.0.0 -> 10101100 00010000 00000000 00000000
```

So, the broadcast ip will be:

```
    10101100 00010000 00000000 00000000
or  00000000 00001111 11111111 11111111
---------------------------------------
    10101100 00011111 11111111 11111111
    172      31       255      255
```

#### Actual use cases for the broadcase address

Host configuration protocol, `BOOTP` and `DHCP`. From the Microsoft Technet, it
said that:

    The bootstrap protocol (BOOTP) is a host configuration protocol developed before DHCP.

So I will only focus on `DHCP` here.

    DHCP -> Dynamic Host Configuration Protocol

What is `DHCP` for? When a device connect to a internet gateway, it needs a ip
address to identity itself inside the network. Instead of configured by human
manually. DHCP helps the administrator to do that work.

#### About 255.255.255.255

255.255.255.255 is a special broadcast address, which means "this network": it
lets you send a broadcast packet to the network you're connected to, without
actually caring about its address.  In this, is similar to 127.0.0.1, which is a
virtual address meaning "local host".

When the time I ran the `ip addr add` command, I didn't say what network mask it
will use. So it have the result like this:

```
inet 10.0.2.15/24 brd 10.0.2.255 scope global eth0
   valid_lft forever preferred_lft forever
inet 10.0.2.16/32 scope global eth0
   valid_lft forever preferred_lft forever
```

Which means that the broadcast address of ip `10.0.2.16` is `255.255.255.255`.
So if I need to change it to make sure that two ips shares the same brocast
address. Just simply remove the `16` one and add it back with network mask.

```
ip address delete 10.0.2.16/32 dev eth0
ip address add 10.0.2.16/24 dev eth0 brd +
```

If I do `ip address add 10.0.2.16/24 dev eth0 brd +`, it will be different.
The host bit will be reset.

