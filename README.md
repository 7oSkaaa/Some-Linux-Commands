# Linux-Commands
Important commands for solving some problems


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

If you want to convert number of files together you can put them in folder together and use this command after open your folder in terminal

```
unoconv -f <format> *.file_extension
```

Example:

```
unoconv -f pdf *.pptx
```

**Convert files to pdf**

```
soffice --headless --convert-to pdf 'file_name.extension'
```

## Coonvert Multiple files and merge them into pdf

**First install Image Magick**

```
sudo apt install imagemagick
```

### Solving the Security Policy Error

```
sudo nano /etc/ImageMagick-6/policy.xml
```

**Find and edit the line:**

```
<policy domain="coder" rights="none" pattern="PDF" />
```

**to:**

```
<policy domain="coder" rights="read|write" pattern="PDF" />
```

**To convert use the following command after open the folder in the terminal:**

```
convert 'file_1.extension' 'file_1.extension' 'file_1.extension' 'pdf_name.pdf'
```

**Example:**

```
convert image1.jpg image2.png image3.bmp output.pdf
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
