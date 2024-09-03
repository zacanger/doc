# Debian Cheatsheet

```shell
# Show installed packages
dpkg --get-selections

# Show installed packages with mouse in name
dpkg --get-selections | grep mouse
dpkg -S xserver-xorg-input-kbd

# Show locations of files within a package
dpkg -L xserver-xorg-input-mouse

# Reconfigure a package
sudo dpkg-reconfigure slim

# Search repository for package by name and description
apt-cache search xserver-xorg-input-kbd
aptitude search xserver-xorg-input-kbd

# Search packages querying in the name only
apt-cache search --names-only xorg

# Show detailed information about a package
apt-cache show xserver-xorg-input-mouse
apt-cache showpkg xserver-xorg-input-mouse

# Install a package
apt-get install dwb

# Add a user to the sudo group
# User must logout and login to take effect
adduser zacanger sudo

# Show type of video card system has
lspci -v | grep VGA

# File to set background image if using gdm
vim /usr/share/gdm/dconf/10-desktop-base-settings
picture-uri='file:///blahbla.jpg'

# Remove background picture
vim /usr/share/gdm/dconf/10-desktop-base-settings
[org/gnome/desktop/background]
picture-options='none'
primary-color='#000000'

# File to change the login screen for gdm3
vim /etc/gdm3/greeter.gsettings

# Reload gdm3 configuration on logout/reboot
dpkg-reconfigure gdm3

# Location of alternatives. Don't cat these they are binaries.
# Just use them to see what options you can throw at update alternatives.
/etc/alternatives

# Shows the symlinks for the default and alternative window managers
update-alternatives --display x-window-manager

# Shows alternatives and give choice of which to use
update-alternatives --config x-window-manager

# Set which browser to use as default
update-alternatives --config x-www-browser

# Add dwb to x-www-browser list and set it's priority to 100
update-alternatives --install /usr/bin/x-www-browser x-www-browser /usr/bin/dwb 100

```
