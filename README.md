# Monterey Hackintosh on the ASUS STRIX Z490F via OpenCore 0.7.5 with Navi GPU HW Acceleration

Hi! This repo is a result of me following [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/), and I insist you do the same for your Hackintosh. Here you can find my personal EFI folder using OpenCore 0.6.9 for use with my Hackintosh. I tend to update this repo as new macOS versions become available, in which case I'll update to the latest available OpenCore release plus kexts around that time. If you have hardware similar to mine you can probably use my EFI folder without much modification, if you intend to do so read on.

## Hardware
![HW info + HW Acceleration](static/working.jpg)
Here's the usual info screenshot plus Netflix working on Safari, a sign of working GPU HW Acceleration & DRM content. 

- Motherboard: ASUS STRIX Z490F
- Networking:
    - Ethernet: Intel I225-V
    - WiFi + Bluetooth: Fenvi T919 (BCM94360CD)
- CPU: Intel i7 10700K
- GPU: SAPPHIRE PULSE AMD Radeon RX 5600 XT 
- RAM: G.SKILL Aegis 16GB
- SSD: Kingston 500GB A2000 M.2 2280 NVME SSD
- Case: NZXT H510i (2020)

## Working
Everything appears to be working **OK**

## Usage
Feel free to use my personal EFI folder for your own Hackintosh projects, just be careful as your config needs may differ depending on your hardware, which may or may not result in failed boots, errors, or loss of data; All of which I bear NO responsibility for. You should follow [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) for configuring and installing OpenCore for your machine.

Otherwise if you do wind up using my config.plist make sure to add the proper values for MLB, ROM, SystemSerialNumber, and SystemUUID under the platforminfo section. More info on this is detailed in [Dortania's guide](https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#platforminfo). Likewise you will need to map your memory which can be found in the guide linked.

To automatically keep up to date with this project, I recommend cloning this repo. 
- `gh repo clone ocean-bee/asus-strix-z490f-hackintosh`

As well, if you're using a different motherboard / case, your USB ports will most likely differ in some way, which means you'll need to generate your own **USBmap.kext**. This process is detailed [here in Dortania's guide](https://dortania.github.io/OpenCore-Post-Install/usb/).
