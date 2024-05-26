# terminal-hacks
A collection of Terminal tricks continuously updated to support my Debian transition.

**Search for directories with a particular string:**  
> find . type -d | grep STRING

**Delete all directories beginning with a particular string:**  
> rm -rf STRING*

**For when python is not found and python3 is required to be typed**  
> alias python='python3'

**To install the power manager**  
> sudo add-apt-repository ppa:linrunner/tlp  
> sudo apt update  
> sudo apt install tlp  
> sudo tlp setcharge 70 80 BATT  
Additionally, go to /etc/tlp.conf, and uncomment the respective lines for battery thresholds to make the changes permanent even after reboot.

**To change the touchpad scrolling speed (it is too fast by default in Ubuntu)**  
> sudo apt install libinput-tools  
> sudo libinput measure touchpad-size 100x100  
> sudo gedit /etc/udev/hwdb.d/61-evdev-local.hwdb  
> sudo systemd-hwdb update  
> sudo udevadm trigger /dev/input/event*

https://ubuntuhandbook.org/index.php/2023/05/adjust-touchpad-scrolling-ubuntu/

**To view graphics driver details in Ubuntu**  
> lshw -c video

**To control the scrolling speed in Firefox**  
> about:config, and then modify: mousewheel.default.delta_multiplier_y

**To kill an unresponsive application**  
> "xkill" in terminal, and then click on the window of the unresponsive application

**To zip multiple folders into one zip file**  
> zip -r zip_file_name.zip folder_1 folder_2

**To unzip a tar file**  
> tar -xf file_name.tar.xz

**To only list directories in the terminal**  
> ls -d */

**To install Awesome Tiles**
1.  Install gnome extension on Firefox
2.  sudo apt-get install chrome-gnome-shell

**To hide or unhide Power settings**  
> sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target  
> sudo systemctl unmask sleep.target suspend.target hibernate.target hybrid-sleep.target

**To split and unite PDF pages**  
Separate using first page and last page:  
> pdfseparate -f 5 -l 7 source_file.pdf output_file%d.pdf  
Unite using all the files generated:  
> pdfunite output_file5.pdf output_file6.pdf output_file7.pdf final_file.pdf

**To show hidden files along with folders in the terminal**  
> ls -ld .?*

**To change location of the default folders (for example, Documents)**  
In the Home directory:  
> nano .config  
Change the folder name as per your linking

**To add, remove, or update menu entries using a GUI**  
> sudo app install alacarte

**To run the previous command in the terminal with sudo**
> sudo !!

**Installing Elmer FEM**

> sudo apt-add-repository ppa:elmer-csc-ubuntu/elmer-csc-ppa
> sudo apt-get update
> sudo apt-get install elmerfem-csc-eg
> ElmerGUI

&nbsp;
