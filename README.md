# Linux-Commands
Important commands for me


## Install Flat Remix Gnome
```
sudo add-apt-repository ppa:daniruiz/flat-remix
```
```
sudo apt update
```
```
sudo apt install flat-remix-gnome
```
## Install Flat Remix Icon Theme
```
sudo add-apt-repository ppa:daniruiz/flat-remix
```
```
sudo apt update
```
```
sudo apt install flat-remix
```
## Install Flat Remix GTK Theme
```
sudo add-apt-repository ppa:daniruiz/flat-remix
```
```
sudo apt update
```
```
sudo apt install flat-remix-gtk

```
## Convert extension of files
install `unoconv`
```
sudo apt install unoconv
```
Dont't forget to put the format you want to convert to instead of `<format>` and put your file name and it's extension instead of `file_name.extension`
```
unoconve -f <format> 'file_name.extension'
```
Example:
```
unoconv -f pdf 'Chapter 1.docx'
```
## Fix Black Screen in screen sharing
Open your terminal
```
sudoedit /etc/gdm3/custom.conf
```
remove `#` from `WaylandEnable=false`
```
sudo systemctl restart gdm3
```
## Permissions for NTFS partition
Got to `Disks` and unmounted the partition
To fix this.
```
sudo ntfsfix /dev/[DRIVE_MACHINE_NAME-FOR-PARTITION]
```

Example:
```
sudo ntfsfix /dev/sda1
```



