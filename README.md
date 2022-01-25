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

## Shutdown Computer at Specific Time

**Sometimes you will need to shutdown your computer some hours after your work hours have ended. You can configure your computer to shut down at specific time by using:**

```
sudo shutdown 21:00
```

**This will tell your computer to shut down at the specific time you have provided. You can also tell the system to shutdown after specific amount of minutes:**

```
sudo shutdown +15
```

## Using yes command for commands or scripts that need interactive response

**If there are some commands or scripts that need user interaction and you know that you have to enter Y each time it requires an input, you can use Yes command.**

```
yes | command_or_script
```

## Make file executable

The chmod command lets you change the mode of a file (permissions) quickly. It has a lot of options available with it.

The basic permissions a file can have are:

r (read)
w (write)
x (execute)
One of the most common use cases for chmod is to make a file executable by the user. To do this, type chmod and the flag +x, followed by the file you want to modify permissions on:

```
chmod +x 'file name'
```

