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


![s1](https://i.imgur.com/xSC8of3.jpg)



https://github.com/c4pt000/komorebi-centos/releases/tag/seconds

https://github.com/c4pt000/komorebi-centos/releases/tag/deb-seconds

## macOS
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


## CentOS

<br>

yum install clutter* libgee-devel webkitgtk-devel.x86_64 webkitgtk4-devel.x86_64 vala-devel cmake3 devtoolset-6 gtk3-devel

<br>

yum install https://github.com/c4pt000/komorebi-centos/releases/download/gstreamer-libav/gstreamer1-libav-1.0.6-1.el7.nux.x86_64.rpm

<br>

scl enable devtoolset-6 bash
<br>
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
make -j8 package



# ** optional (nux-desktop)
<br>

 yum -y install epel-release && rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-5.el7.nux.noarch.rpm

<br>

yum install ffmpeg winff

# ** scripts to help edit or create video wallpaper

<br>
cat /usr/bin/ffmpeg-to-jpg-conv 
<br>
ffmpeg -i ./video.ogv -r 1 -f image2 image-%3d.jpeg

<br>
cat /usr/bin/ffmpeg-jpg-to-mp4-conv
<br>
ffmpeg -r 1 -f image2 -i image-%3d.jpeg video.ogv


# ** for conversion from .ogv to .mp4 format
<br>
ffmpeg -i video.ogv video.mp4





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



if you found this useful, anything helps

1LzcsiiKveiDrPp6VGhQCg44dnQzqY2vNv

https://www.binance.com/userCenter/deposit.html      << for bitcoin mc/visa


![s1](https://i.imgur.com/py97aYA.png)









