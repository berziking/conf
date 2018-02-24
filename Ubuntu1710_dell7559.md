
# Ubuntu on dell 7559

sudo apt update  
sudo apt dist-upgrade  

**Disable nvidia card**  
sudo apt install intel-microcode  
sudo apt install bbswitch-dkms  
sudo vi /etc/modules  
```bbswitch load_state=0```  
sudo vi /etc/modprobe.d/blacklist.conf  
```
blacklist nouveau
blacklist nvidia
```
sudo update-initramfs -us  

**Disable wayland**  
sudo vi /etc/gdm3/custom.conf  
```WaylandEnable=false```  

sudo reboot  

**Check server**  
echo $XDG_SESSION_TYPE  
```X11```

**Power management**  
sudo apt install tlp tlp-rdw  
sudo vi /etc/default/tlp  
```
CPU_SCALING_GOVERNOR_ON_AC=performance
CPU_SCALING_GOVERNOR_ON_BAT=powersave
CPU_MIN_PERF_ON_AC=0
CPU_MAX_PERF_ON_AC=100
CPU_MIN_PERF_ON_BAT=0
CPU_MAX_PERF_ON_BAT=30
CPU_BOOST_ON_AC=1
CPU_BOOST_ON_BAT=0
sudo reboot
```
**Extras**  
sudo apt install gnome-tweak-tool  
sudo apt install chromium-browser chrome-gnome-shell  
sudo apt install vim git build-essential  


**Gnome extensions**  
https://extensions.gnome.org/extension/7/removable-drive-menu/  
https://extensions.gnome.org/extension/1112/screenshot-tool/  
https://extensions.gnome.org/extension/1082/cpufreq/  
https://extensions.gnome.org/extension/8/places-status-indicator/  
https://extensions.gnome.org/extension/15/alternatetab/  
https://extensions.gnome.org/extension/906/sound-output-device-chooser/  
https://extensions.gnome.org/extension/826/suspend-button/  
