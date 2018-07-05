# 20180704Archlinuix
> 說明
>> ∵ 因為工作需要，要出差有配置一台高級筆電
>>
>> ∴ 趁機練習安裝系統/win10/linux mint /Archlinux

### 主機資訊
> DELL Dell Inspiron 15 7000 Gaming 
>> CPU: Intel Core i5-7300HQ. 
>>
>> RAM:       DDR4  4GB.
>>
>> Graphics:  Nvidia GeForce GTX 1060
>>
>> SSD: 	    M.2 SSD 256GB.
>>
>> Networking: 802.11ac wireless, Bluetooth 4.2.

### 系統資訊
> win 10 
>> 7/2  用 Rufus 來製作可安裝 Windows 用的開機隨身碟， 藉由 USB 安裝系統 ok
>> 
>> P.S 筆電需要用UEFI mode 開機，所以不能用混合模式的設定
>>
> linux mint
>> 7/2  用 YUMI-UEFI-0.0.0.8.exe 來製作可安裝 Windows 用的開機隨身碟， 藉由 USB 安裝系統 ok
>>
> Archlinux
>> 7/2 在公司就開始安裝，但一直卡在wifi設定上 
>>
>> 7/4 終於發現問題點是出在dhcp上，停用後wifi設定就不會衝突

## archlinux 安裝基礎設定 → preinstall.log   


## archlinux Befirstboot.log     

## Afisrtboot.log      

## 安裝顯卡驅動/WM~I3/DM ~ mate/ ~ installwm.log      
># Install Graphics driver
>>  yaourt -S --noconfirm  xf86-video-intel 
>>
>>  yaourt -S --noconfirm  xf86-video-vesa
>>
>>  yaourt -S --noconfirm  nvidia 


  yaourt -S --noconfirm   system-config-printer gtk3-print-backends blueberry orca mousetweaks arc-gtk-theme arc-icon-theme
  yaourt -S  --noconfirm  xf86-input-evdev xf86-input-keyboard xf86-input-mouse xf86-input-void libinput

# Install X-windows
  yaourt -S --noconfirm xorg xorg-xinit xorg-server xorg-server-utils
  yaourt -S --noconfirm xorg xorg-xinit xorg-server 
  yaourt -S --noconfirm xorg-twm xterm xorg-xclock

# Install Desktop environment 
  yaourt -S --noconfirm mate mate-extra

# Insatll fcix
  yaourt -S --noconfirm fcitx fcitx-im  fcitx-configtool fcitx-sunpinyin fcitx-chewing 

# install web bor 
  yaourt -S --noconfirm  firefox epiphany flashplugin

# install i3 feh conky
  yaourt -S --noconfirm  feh conky  compton i3-gaps

# install i3 like depend
  yaourt -S --noconfirm  xfce4-terminal xfce4-screenshooter xfce4-notifyd konsole
  yaourt -S --noconfirm gnome-keyring gnome-system-monitor gnome-screenshot screenfetch rofi gedit
  yaourt -S --noconfirm  pulseaudio pulseaudio-alsa pavucontrol 
 
# Install  Display manager
  yaourt -S  --noconfirm   lightdm lightdm-gtk-greeter lightdm-gtk-greeter-settings
  sudo systemctl enable lightdm.service

># install VirtualBox 
>>  yaourt -S  --noconfirm virtualbox
>>
>>  sudo modprobe vboxdrv
>>
>>  sudo modprobe vboxnetadp
>>
>>  sudo modprobe vboxnetflt
># 開機自動載入 VirtualBox 模組
>>  sudo echo vboxdrv > /etc/modules-load.d/virtualbox.conf
>>
>>  sudo echo vboxnetadp > /etc/modules-load.d/virtualbox.conf
>>
>>  sudo echo vboxnetflt > /etc/modules-load.d/virtualbox.conf

 


