# Support for MZP screens

# MegaMosquito's Notes:
1. I think you need to use the "full" Raspberry Pi OS image with graphical Desktop software (it's a dependency)
2. For current versions of Raspberry Pi OS you absolutely must use `sudo raspi-config` to configure **AdvancedOptions** -> **GLDriver** -> **G1Legacy** (this is for sure required becuase their software is not compatible with the new GL driver)
3. Maybe optional, but I run my machines headless so I also configure **InterfaceOptions** -> **VNC** and **DisplayOptions** -> **VNCResolution** -> **1920x1080**
4. I am pretty sure for this headless setup you also need to configure **SystemOptions** -> **Boot/AutoLogin** -> **DesktopAutoLogin**

# Common setup

    cd ~/

    git clone https://github.com/tianyoujian/MZDPI.git
    
# MZP280V
    cd MZDPI/vga

    sudo chmod +x mzdpi-vga-autoinstall-online

    sudo ./mzdpi-vga-autoinstall-online

    sudo reboot

# MZP351HV00BR
    cd MZDPI/mzp351hv00br

    sudo chmod +x ./mzdpi-hvga-autoinstall

    sudo ./mzdpi-hvga-autoinstall

    sudo reboot
