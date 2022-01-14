# Linux-Commands
Important commands for me


## Convert extension of files
Dont't forget to put the format you want to convert to instead of <format> and put your file name and it's extension instead of file_name.extension
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
