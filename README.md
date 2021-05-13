# TWRP Device Tree for Walton Primo S7 for building TWRP recovery 

Primo S7 Basic specs:

Processor: MediaTek Helio P22 (MT6762)
RAM: 4 GB
Storage: 32 GB
Display: 6.26 in, IPS, 720 x 1520 pixels, 24 bit
Camera: 4032 x 3024 pixels, 1920 x 1080 pixels, 30 fps
Battery: 3900 mAh, Li-Polymer

# it's time to build a TWRP recovery image
Clone minimal TWRP environment
Follow the instruction in this page
https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni

Remember to clone the correct version of TWRP based on what Android version your phone have! If your phone have Android 8.0, clone twrp-8.0 branch

Move device tree to TWRP sources
Copy working/(brand)/(device) folder to device/(brand)/(device) folder in TWRP sources
Example:

brand name: Walton
device codename: Primo_S7
Copy working/Walton/Primo_S7 to device/Walton/Primo_S7 in TWRP sources

Open a terminal with the current dir pointing to TWRP sources root
Then type
. build/envsetup.sh
to initialize the environment

After that, type
lunch omni_codename-eng
where codename is the codename of your phone

If that is successful, type
mka recoveryimage
to build the recovery

If also that is successful, congratulation!
Go to out/target/product/codename/ (codename is your device codename) and you will find your recovery.img
