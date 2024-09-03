# Process Managers (For Node)

These tools can help keep your Node apps running if they crash, control
clustering, modify settings, and get some insight into performance and
resource usage.

## StrongLoop Process Manager

StrongLoop PM has built-in load balancing, monitoring, a graphical console,
and multi-host deployment. It can build, package, and deploy your Node app
locally or remotely; keep track of system (CPU) usage; run processes and clusters;
show performance metrics; and manage multi-host deployments with Nginx integration.
The CLI tool is `slc`; there's also a grpahical tool called Arc.

* `npm i -g strongloop`: install
* `cd appname ; slc start`: start an app
* `slc ctl`: view status of the process manager and all apps
* `slc ctl ls`: list all apps
* `slc ctl stop appname`: stop an app
* `slc ctl restart appname`: restart an app
* `slc ctl soft-restart appname`: restarts after a grace period to close existing connections
* `slc ctl remove appname`: remove app from management

## PM2

PM2 keeps your apps running, has a built-in load balancer, and can help with
logging, monitoring, and clustering.

* `npm i -g pm2`: install pm2
* `pm2 start script.js`: start that script
* `pm2 show [id or name]`: view info about that running script
* `pm2 list`: list all running processes
* `pm2 stop 0`: stop an app
* `pm2 restart 0`: restart an app
* `pm2 show 0`: view detailed info about an app
* `pm2 delete 0`: delete app from PM2's registry

## Forever

Forever is ideal for small apps/uses. It has more options than listed below,
and a programmatic API.

* `npm i -g forever`: install forever
* `forever start`: commands to run scripts
* `forever start script.js`: start that script in the background
* `forever script.js`: start that script in the foreground (attached to terminal)
* `forever start -a -l forever.log -o out.log -e err.log script.js`: start that script
  in the background, and append logs to those specified files
* `forever list`: view list of processes started with forever
* `forever stop`: commands to stop forever processes
* `forever stop 1`: stop the script running at that index (check `forever list`)
* `forever stop script.js`: stop that file
* `forever stopall`: stop all scripts run by forever

