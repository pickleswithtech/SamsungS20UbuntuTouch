# Install Ubuntu Touch on Samsung Galaxy S20 (Code Name: x1s)
## [Progress of the Samsung Galaxy S20](https://github.com/pickleswithtech/SamsungS20UbuntuTouch/blob/halium-13/SamsungGalaxyS20)
							Requirements
								
   

 - Samsung Galaxy S20 with an Unlocked Bootloader.
 - PC/Laptop running **Ubuntu 22.04.3 LTS** get **Ubuntu 22.04.3 LTS** from [here](https://cdimage.ubuntu.com/releases/jammy/release/source/ubuntu-22.04.3-src-1.iso).

# 1. Unlock Bootloader

# Caution  

### Your device will have poor security and be factory reset. AFTER THIS IS DONE THERE IS NO UNDO!

For those who are experienced for that, for those who are new. I will give you a guide.

1.  Go to  **Settings > About phone**  and tap  **Build number**  3 or more times to enable  **Developer mode**.
2.  Go back to  **Settings**, open  **Developer options**, and enable  **OEM unlocking**. Enter your password if prompted.
3.  Restart the device and quickly connect a  **USB cable** to your computer.
4.  While connecting, press  **Volume Up + Volume Down**  buttons simultaneously to enter  **Odin mode**.
5.  In Odin mode, press the volume up button to  **unlock the bootloader**. The device will restart and reset to factory settings.

That's it! Your device should say the bootloader is unlocked and the device is not trusted.

Image1

# 2.  Set Binarys to Custom
If you have just Unlocked the Bootloader your binarys will be set to Samsung only because Samsung Knox still runs to set it to custom there's two methods.
# Method 1
Keep the phone on and connected to WIFI for at least a week.
# Method 2
Use tools like Samfw to overwrite Samsung Knox. Below will be a guide for Samfw.
# Samfw Method
1. Download Samfw from [here](https://samfw.com/SamFwToolSetup_v4.9.zip). Your antivirus may flag the setup file. Don't worry it's safe I have tested it myself on my main PC. This is a windows app ONLY! Use Ubuntu for everything else!
2. After the setup is done open Samfw.
3. Then put your phone into test mode by typing \*#0*# into the Phone app/Dialer
# Compile the files needed for Ubuntu Touch
First on your PC with **Ubuntu 22.04.3 LTS** open your terminal and enter `sudo apt update -y && sudo apt install -y \
    dialog bash sed wget git curl zip tar jq expect make cmake automake autoconf \
    llvm lld lldb clang gcc binutils bison perl gperf gawk flex bc python3 \
    zstd openssl unzip cpio build-essential ccache liblz4-tool libsdl1.2-dev \
    libstdc++6 libxml2 libxml2-utils lzop pngcrush schedtool squashfs-tools \
    xsltproc zlib1g-dev libncurses5-dev bzip2 gcc g++ libssl-dev \
    gcc-aarch64-linux-gnu gcc-arm-linux-gnueabihf gcc-arm-linux-gnueabi \
    libtinfo5 libelf-dev resolvconf dos2unix python3 python-is-python3 \
    kmod neofetch android-tools-fsutils fakeroot pahole
` This command will download all the required files for compiling Ubuntu Touch.

 
