# Clash Verge for Debian/Ubuntu  

This is an archive of installation package and dependencies of Clash Verge on Debian/Ubuntu.  
I mostly set it up so I won't be panicing after reinstalling Ubuntu and can't go over the big wall.  

## Why didn't I try [Clash Verge Rev](https://github.com/clash-verge-rev/clash-verge-rev)?  

I'm already used to using Clash and Clash Verge, and I prefer to have a little cat on my status bar instead of a fox.  
Besides, it seems using Clash Verge Rev also requires going through the hassle of installing extra dependencies.  
Not that different from installing Clash Verge, so I'll stick with the old friend.  

## Why I can't open Clash Verge/Clash Verge Rev after successful installation?  

There is a misunderstanding in this sentence. Your installation is not successful.  
Yes the app seems "installed" with trigger set up properly, but it won't open or load at all, because you are missing important dependencies.  

## How to install Clash Verge on Ubuntu?  

### Step 1: Download [Clash&nbsp;Verge](./clash-verge_1.3.8_amd64.deb) and Install  

- Double click to install via Snap Shop (possibly not working on Ubuntu 24.04), or  
- Use dpkg to install: `sudo dpkg -i PACKAGE`, replace `PACKAGE` with path to the package you just downloaded  

### Step 2: Try launching Clash Verge  

- If the little kitten opens, you're done!  
- However, if you are running a modern version of Debian/Ubuntu (e.g. Ubuntu version >= 20.04), chances are that it won't load at all.  
- Keep following the steps below to fix your installation.  

### Step 3: Install Dependencies  

- Download [libicu70_70.1-2_amd64.deb](./libicu70_70.1-2_amd64.deb), [libjavascriptcoregtk-4.0-18_2.36.0-2ubuntu1_amd64.deb](./libjavascriptcoregtk-4.0-18_2.36.0-2ubuntu1_amd64.deb) and [libwebkit2gtk-4.0-37_2.36.0-2ubuntu1_amd64.deb](./libwebkit2gtk-4.0-37_2.36.0-2ubuntu1_amd64.deb).  
- Install these packages with the following order:
```
sudo dpkg -i libicu70
sudo dpkg -i libjavascriptcoregtk-4.0-18
sudo dpkg -i libwebkit2gtk-4.0-37
```  
- Replace names of the packages with actual paths leading to the packages.
- If you did not follow the exact order, you may need to fix dependencies afterwards.  

### Step 4: Reinstall Clash Verge  

- Install Clash Verge again following instructions in [Step&nbsp;1](https://github.com/Kokodayo-CN/ClashVergeforUbuntu?tab=readme-ov-file#step-1).  

### Step 5: Finish  

- Congratulations! Your Clash Verge should have properly installed and can run like your real cat breaking walls.  

## Extra Reminder  

- If Clash Verge still refuses to open after steps above, check your terminal to check error messages after `dpkg -i` commands. Most likely you are still missing some dependencies, which will be clearly listed. Download them and use `sudo dpkg -i PACKAGE` to install.  
- Under most cases you can't use `sudo apt --fix-broken` to resolve missing dependencies, since your system already failed once on finding those dependencies when installing the packages. Download missing dependencies directly from Ubuntu Archives then install manually.  
- You can always replace `dpkg -i` with `apt install` or `apt-get install`.  
- This guide is only for users of Debian and Debian-derived distros. For folks on the Arch side, this guide won't be helpful at all.  
