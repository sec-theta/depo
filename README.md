Device repository for Intex Aqua Ace (ace) (CyanogenMod)
===========================
For Stock 3.10.65 kernel

Getting Started
***********************************************************************************************
Upload Tree to to your account Like Kill-Shot/android_device_intex_ace And Follow below commands
***********************************************************************************************

Initialize a repository with CyanogenMode:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-14.1
    
Sync sources:    

    repo sync
    
Build the code:
    
    cd device
    mkdir intex
    cd intex
    git clone https://github.com/Kill-Shot/android_device_intex_ace ace
    cd ace/patches
    . apply-patches.sh
    cd vendor
    mkdir intex
    cd intex
    git clone https://github.com/Kill-Shot/android_vendor_intex_ace ace
    cd ../../
    source build/envsetup.sh
    breakfast ace
    make -j 4 bacon

Current state
-------------

- Cyanogen boots
- Touch, screen, keyboard working
- Wifi is working
- Audio is working
- Telephony is working (see Known Issues)
    - USIM (3G) supported
    - Incoming/outgoung call
    - SMS, USSD
    - Data connectivity
- GPS
- Bluetooth (pairing only testes so far)
- Sensors

Known Issues
-------------
- Livedisplay (lagging)
- FMRadio
- VoLTE
- Gps without network connections?
- Camera
- Hardware OMX codecs are not working

Change log
----------

### v0.2
- Fixed an issue with proximity on some devices
- Fixed an issue with ICC IO in MTK ril (no radio with some SIM cards)
- Fixed a modem crash caused by mtk_agps request
- Fixed an issue with WiFi SoftAP
- Ported power HAL from CyanogenMod 6735 (also implements Double Tap To Wake feature)
- Ported FOTA solution from meilan2 cm-12.1

### v0.1
- Initial port from cm-14.0 (v0.3) to cm-14.1

