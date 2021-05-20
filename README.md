* update 01-25-2020


* noticed gstreamer1-libav.x86_64 is mandatory and required for komorebi to function

<br>
* all original themes most edited themes


<br>
<br>
<br>
<br>
<br>
<br>

after pkg install rpm or deb
<br>
```cp -rf /System/Applications/komorebi /usr/bin/```
<br>
to run ```komorebi &```
<br>
regular startup script in System/Preferences/Startup Applications (on login)
<br>
https://github.com/c4pt000/komorebi-centos-debian/releases/download/bundled/komorebi-2.1.0-Linux.extras.deb
<br>
https://github.com/c4pt000/komorebi-centos-debian/releases/download/bundled/komorebi-2.1.0-2.x86_64.extras.rpm
<br>
if caja breaks use nemo

https://github.com/c4pt000/komorebi-centos<p align="center"><img src="https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/screenshots/komorebi-icon.png" width="130"></p>
<h2 align="center">Komorebi - Animated Wallpapers for Linux</h2>
<p align="center">(n) sunlight filtering through trees.</p>



<p align="center">
	<a href="http://www.kernel.org"><img alt="Platform (GNU/Linux)" src="https://img.shields.io/badge/platform-GNU/Linux-blue.svg"></a>
	<a href="https://github.com/sindresorhus/awesome"><img alt="Awesome" src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg"></a>
	<a href="https://travis-ci.org/cheesecakeufo/komorebi"><img alt="Build Status" src="https://travis-ci.org/phw/peek.svg?branch=master"></a>
</p>

<p align="center">
<a href="http://www.youtube.com/watch?feature=player_embedded&v=NvfRy5qMsos
" target="_blank"><img src="http://img.youtube.com/vi/NvfRy5qMsos/0.jpg" 
alt="Komorebi Demo" width="240" height="180" border="10" /><br>Watch demo</a>
</p>

https://github.com/c4pt000/komorebi-centos/releases


# *** From further checking it seems like it is broken on FGLRX / AMD as of now?
# *** 04-29-2019

# * added support to display seconds with the wallpaper clock
* first attempt "particles style animated low-res

![s1](https://i.imgur.com/xSC8of3.jpg)



https://github.com/c4pt000/komorebi-centos/releases/tag/seconds

https://github.com/c4pt000/komorebi-centos/releases/tag/deb-seconds



![s1](https://user-images.githubusercontent.com/46433702/64658445-90285c80-d405-11e9-93d7-0774ac4cf26e.gif)


https://github.com/c4pt000/komorebi-centos/releases/tag/blackjack-theme

![s1](https://raw.githubusercontent.com/c4pt000/komorebi-centos-debian/master/animated-out.gif)

https://github.com/c4pt000/komorebi-centos-debian/releases/tag/theme-no-audio

![animated-out](https://user-images.githubusercontent.com/46433702/65000037-1803e000-d8b8-11e9-92ac-6ce113f80175.gif)

https://github.com/c4pt000/komorebi-centos/releases/tag/joker_scrnsvr

## macOS (untested)
brew install cmake
<br>
brew install libffi
<br>
export PKG_CONFIG_PATH="/usr/local/opt/libffi/lib/pkgconfig"
<br>
brew install gtk+3 libgee pygobject clutter* gobject*
<br>
brew tap jcudit/homebrew-webkitgtk
<br>
brew install --HEAD jcudit/webkitgtk/webkitgtk
<br>
mkdir build
<br>
cd build
<br>
cmake ..
<br>
make -j16 install


## CentOS


<br>

devtoolset-4 or devtoolset-6 optional (devtoolset-6 recommended)

yum install devtoolset-6

yum install clutter* libgee-devel webkitgtk-devel.x86_64 webkitgtk4-devel.x86_64 vala-devel cmake3 gtk3-devel

<br>

yum install https://github.com/c4pt000/komorebi-centos/releases/download/gstreamer-libav/gstreamer1-libav-1.0.6-1.el7.nux.x86_64.rpm


(if devtoolset-6 is installed)
<br>
scl enable devtoolset-6 bash
<br>
cd /opt
<br>
git clone https://github.com/c4pt000/komorebi-centos
<br>
cd komorebi-centos
<br>
cp -rf CMakeLists.txt CMakeLists.txt.deb
<br>
cp -rf CMakeLists.txt.rpm CMakeLists.txt
<br>
mkdir build
<br>
cd build
<br>
cmake3 ..
<br>
make -j16 package


## errors with libglvnd0 during compile -> undefined symbol: _glapi_tls_Current '
<br>
for errors related to ' undefined symbol: _glapi_tls_Current '
<br>

https://bugs.debian.org/cgi-bin/bugreport.cgi?att=0;bug=878968;msg=5	
<br>
```
	cd /usr/lib64/
	yum reinstall libglvnd*
	mkdir libglvnd-nvidia-orig
	mv libGLESv2_nvidia.so.* libglvnd-nvidia-orig/
	ldconfig 
	cd /opt/komorebi-centos
	mkdir build
	cd build/
	cmake3 ..
	make -j16 package
        rpm -Uvh komorebi-2.1.0-Linux.rpm 
	/System/Applications
        cp -rf komorebi* /usr/bin/

```

# ** optional (nux-desktop)
<br>

 yum -y install epel-release && rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm



## (main theme set edits)

## https://github.com/c4pt000/komorebi-centos/releases/download/theme-mod/Komorebi.tar.gz


* other config
<br>
editing the config by setting Position=none
<br>
allows for free floating movement of date and time 
<br>
<br>
https://pixabay.com/videos/search/motion%20backgrounds/
<br>
<br>
<br>
Position=0             <<- in the theme config to allow free floating placement of the time date indicator
<br>
<br>
<br>
```
yum install ffmpeg winff -y
```
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

# * --start
# ** scripts to help edit or create video wallpaper
<br>
<br>
cat /usr/bin/ffmpeg-to-jpg-conv 
<br>
```
ffmpeg -i ./video.ogv -r 1 -f image2 image-%3d.jpeg
```
<br>
cat /usr/bin/ffmpeg-jpg-to-mp4-conv
<br>
```
ffmpeg -r 1 -f image2 -i image-%3d.jpeg video.ogv
```
<br>
jpg to mp4 (another alternative)
<br>
```
ffmpeg -pattern_type glob -i "*.jpg" -c:v libx264 -pix_fmt yuv420p -movflags +faststart output.mp4
```

# ** for conversion from .ogv to .mp4 format
<br>
```
ffmpeg -i video.ogv video.mp4
```


* other (blank 60 second audio interweave)
```
 ffmpeg -t 60 -s 640x480 -f rawvideo -pix_fmt rgb24 -r 25 -i /dev/zero -i mp3-60sec.mp3 videoandmp3.avi
```

<br>
<br>
<br>
<br>
<br>
<br>
mp4 to animated gif from 60 seconds que for 2.5 seconds
```
ffmpeg -ss 61.0 -t 2.5 -i video.mp4 -filter_complex "[0:v] fps=12,scale=480:-1,split [a][b];[a] palettegen [p];[b][p] paletteuse" animated-out.gif
```
# * --end
<br>
<br>
<br>
<br>
<br>
<br>

## reason of fork
## CentOS/Fedora/RHEL/SuSE












## What is Komorebi?

Komorebi is an awesome animated wallpapers manager for all Linux platforms.
It provides fully customizeable image, video, and web page wallpapers that can be tweaked at any time!

![s1](https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/screenshots/collage.jpg)


## How do I install Komorebi?

Two ways:

### Packaged install (easy)

1. Download `Komorebi` from the [Komorebi releases page](https://github.com/c4pt000/komorebi-centos/releases).
2. Install Komorebi using your favorite package installer (aka. double click on it)
3. Launch Komorebi!

### Manual Installing (advanced) Debian/Ubuntu

Run the following:
```
sudo add-apt-repository ppa:gnome3-team/gnome3 -y
sudo add-apt-repository ppa:vala-team -y
sudo add-apt-repository ppa:gnome3-team/gnome3-staging -y
sudo apt install cmake valac libgtk-3-dev libgee-0.8-dev libclutter-gtk-1.0-dev libclutter-1.0-dev libwebkit2gtk-4.0-dev libclutter-gst-3.0-dev
git clone https://github.com/c4pt000/komorebi-centos
cd komorebi
mkdir build && cd build
cmake .. && sudo make install && ./komorebi
```

### Manually Installing (advanced) CentOS/RHEL/Fedora
```
## CentOS

yum install clutter* libgee-devel webkitgtk-devel.x86_64 webkitgtk4-devel.x86_64 vala-devel cmake3 devtoolset-6 gtk3-devel

yum install https://github.com/c4pt000/komorebi-centos/releases/download/gstreamer-libav/gstreamer1-libav-1.0.6-1.el7.nux.x86_64.rpm

scl enable devtoolset-6 bash

cd /opt
git clone https://github.com/c4pt000/komorebi-centos
cd komorebi-centos
cp -rf CMakeLists.txt CMakeLists.txt.deb
cp -rf CMakeLists.txt.rpm CMakeLists.txt
mkdir build
cd build
cmake3 ..
make -j8 package
```


## Change Wallpaper & Desktop Preferences
To change desktop preferences or your wallpaper, right click anywhere on the desktop to show the menu.

![s1](https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/screenshots/preferences.jpg)

## How do I create my own wallpaper?

Komorebi provides a simple tool to create your own wallpapers! Simply, open your apps and search for 'Wallpaper Creator'

![s1](https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/screenshots/wallpaper_creator.jpg)

You can use either an image, a video, or a web page as a wallpaper and you have many different options to customize your very own wallpaper!

## Uninstall

### If you installed a packaged version of Komorebi

1. Open Terminal
2. `sudo apt remove komorebi`

### If you manually installed Komorebi

1. Open Terminal
2. `cd komorebi/build`
3. `sudo make uninstall`

## Questions? Issues?

### Komorebi is slow. What can I do about it?

Komorebi includes support for video wallpapers that might slow your computer down. You can disable support for video wallpapers in 'Desktop Preferences' → uncheck 'Enable Video Wallpapers'.

_note: you need to quit and re-open Komorebi after changing this option_


### After uninstalling, my desktop isn't working right (blank or no icons)

The latest Komorebi should already have a fix for this issue. If you've already uninstalled Komorebi and would like to fix the issue, simply run this (in the Terminal):
`curl -s https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/data/Other/postrm | bash -s`

If your issue has not already been reported, please report it *[`here`](https://github.com/cheesecakeufo/komorebi/issues/new)* and I'll try my best to fix them.

### Why does Komorebi install files in a macOS-like structure?

Komorebi was originally intended to run on an unreleased OS project. Since many people already use Komorebi, an update could potentially break Komorebi and custom-made wallpapers.

It is possible to change the file structure with code changes and a `postinst` script but I'd rather keep it as is for now or if you have the time to make one, feel free to do so and submit a PR!









## ** Forked from,   https://github.com/cheesecakeufo/komorebi

## Status of Development

Komorebi still receives updates but they are not as frequent due to my involvement in other open-source projects.


### Thanks To:

Pete Lewis ([@PJayB](https://github.com/PJayB)) for adding mult-monitor support













<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>







