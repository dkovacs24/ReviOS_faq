---
hide:
  - navigation
---

<style>
    div.admonition p:not(.admonition-title) {
        font-size: 125%;
    }
</style>

!!! info
    This page is still in the works, but it should cover almost all of the scenarios already.

# How to install drivers

!!! warning "About driver installer tools and Windows Update"
    Lots of users install their drivers incorrectly, like use a driver installer tool or Windows Update to install an outdated or not even working one. Do not use any of these methods. Driver installer software in the best case scenario install a not working or outdated driver. Worst case scenario, break your Windows and case Blue Screen of Death. Windows Update just bad. Most hardware it cannot identify, or installs older driver for it.

## Step 0: What drivers do you need

In the installation tutorial we discuss that the absolute bare minimum of drivers is the network drivers, because if your new installation cannot use the internet, cannot download the drivers needed, for example the network drivers. You see where this is going, it's a vicious circle.

After installing Windows, you only need drivers for those pieces of hardware that are not working. So if your Wi-Fi is working, but your Bluetooth and Audio not, you only need to download the last two, there is no point of downloading the Wi-Fi too.

## Step 1: Locating your drivers

The best way to find the driver of a not working hardware is to simple Google for it. The general idea is that you should only download the drivers from the website of the manufacturer of that hardware.

### PC (motherboard)

On PC, most of the hardware modules are on the motherboard, so you need to just Google `<your motherboard> drivers`. There, open the result, which takes you to the motherboard's manufacturer's website. Even better, if it is the page of the motherboard. There, the drivers are usually under the Support section or something like that. If you don't have that, look around the page, it must be there.

!!! example
    For example, if you have a ASUS PRIME H610M-K D4 motherboard. 
    
    First, you should Google `ASUS PRIME H610M-K D4 drivers`. 
    
    There, let us say you choose the ASUS Global search result. So it brings up [the website of the motherboard](https://www.asus.com/Motherboards-Components/Motherboards/PRIME/PRIME-H610M-K-D4/){target=_blank}.

    Now you look around and find a `Support` page next to the `Overview`, `Tech Specs` and `Review` pages. Click the [Support page](https://www.asus.com/Motherboards-Components/Motherboards/PRIME/PRIME-H610M-K-D4/HelpDesk_knowledge/){target=_blank}.

    There you can see a tab of the page called `Drivers & Utility`. From now on, I think it is obvious. Click on that tab, select your OS, and download the drivers you need.

!!! tip
    Another trick if you cannot find what you want is to look around on a different language region of the website. Like after googling, the first result is probably will be the official website of the manufacturer in your region, in your language. Other top results usually are the global version of the website. Look around on that, too. I have seen a vendor where the hardware was not on the local region website, but it was on the global.

### Laptop

On a laptop, the steps are almost exactly the same. Since the laptop's motherboard does not have a name, you Google the laptop's name similarly to the motherboard example.

### Other hardware

Other hardware that is not part of the motherboard.

#### GPU drivers

These drivers should only come from the manufacturer's website, with the case of GPUs it is either NVIDIA, AMD or Intel.

##### NVIDIA

Go to the official [NVIDIA website](https://www.nvidia.com/){target=_blank}, click the `Drivers` button on top top of the page, then select your driver. Download and install it. This should be trivial. For debloating and tweaking the driver, see the [Post-Install guide on the Revision website](https://www.revi.cc/revios/post-install#h.p_26IZH4oTRS4J){target=_blank}.

##### AMD

Go to the official [AMD website](https://www.amd.com/en/support){target=_blank}, and down the page select your hardware, download the driver and install it.

##### Intel

1. Given that you must know at least the name of your CPU, search for its specs.
2. Open the result, which takes you to the ark.intel.com website.
3. There on the left side of the page should be a menu option called `Drivers and Software`.
  
    It will take you directly to the graphical drivers. From here it should be trivial. Download and install.

If you cannot find your CPU on the ark website, you can go on a different method, but it is more "unstable", meaning this guide cannot take you through every step exactly:

<!-- this shows on the generated website starting from 1 -->
4. Find the `Processor Graphics` section on the specs page, there you can find out which integrated GPU you have. Take note of that or copy the name.
5. Google the name of the iGPU, for example `Intel HD 630 drivers`
6. Open one of the Intel website in the search results, and sadly here is the part where this guide says that you need to find the driver on the Intel website on your own. It is because depending on the search engine and the iGPU, the search results can vary and there is not really one, clean method. Intel's website is so messy.


## Step 2: Installing the driver

This is the easiest part. Extract the driver, if it comes in an archive file. Then you need to find an executable file, usually called `setup`, with the extensions `.exe` or `.msi`.

!!! example
    Continuing the PC motherboard example from the previous step, if you downloaded the audio driver, you need to first extract the zip file of the driver. Then find and execute the `setup.exe`. The installer wizard will walk you through the installation of the driver. After finishing, it usually offers to restart the PC. Restart it. Or if the timing of the restart is not good for you, you can delay it, but do not forget to do it later, because until you restart, the hardware will not work.


## Troubleshooting

If the downloaded driver is not working try the following:

- Did you restart after installing the driver? If not, it probably will fix it.
- Try to find and install an older driver.

## A LAST RESORT

!!! danger
    Again, ==**USE THIS ONLY AS A LAST RESORT**==, if you really cannot find a properly working driver for your hardware. Do not jump to this option directly.

You can use Snappy Driver Installer Origin.

1. Download SDIO from [the website of the software](https://www.snappy-driver-installer.org/){target=_blank}
2. Extract the zip file
3. Run `SDIO_auto.bat` and accept the license
4. Once the Welcome window pop-ups, click on `Download Indexes Only`
5. Here, only select the drivers that you need and could not find in any previous tries
6. Click on `Install`