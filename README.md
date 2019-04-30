# Installing Linux on the AMD Personal Internet Communicator (PIC)

Notes on install Linux on the AMD [Personal Internet Communicator](https://en.wikipedia.org/wiki/Personal_Internet_Communicator) (PIC).

![AMD Personal Internet Communicator](media/amd-pic.jpg)

## Flashing the BIOS

The PIC was shipped with a locked-down BIOS which prevented the installation of any other operating system.  Fortunately, someone created a hacked BIOS which circumvents this: [PICMOD.ROM](https://github.com/pepaslabs/amd-pic-linux/raw/master/PICMOD.ROM).

However, first we need to get access to a command line in WinCE on the AMD PIC:
- Boot the AMD PIC into WinCE.
- Open "My Device" on the desktop.
- Select View/Options and unclick everything (show hidden file, os files, etc)
- Right click on "Control Panel.lnk" and select properties.
- Click on "shortcut" tab.
- Change path to "\windows\cmd.exe".
- Click Ok.
- Double click "Control Panel.lnk"
- You should be in a command prompt!

Now, on to flashing the BIOS:
- Download [PICMOD.ROM](https://github.com/pepaslabs/amd-pic-linux/raw/master/PICMOD.ROM) and copy it to a FAT32-formatted USB flash drive, then insert it into the AMD PIC.
- From the command line:
  - `cd "\USB device"`
  - `\Windows\FlashCE 256 "\USB device\PICMOD.ROM" 0x01dfd81a noreboot`

## Links

- https://en.wikipedia.org/wiki/Personal_Internet_Communicator
- http://www.amdboard.com/pic.html
- http://mozy.org/amd-pic/
- http://jsco.org/dectop/
- http://pair.offshore.ai/pic/
- http://www.dashfest.com/?p=327
- https://hardforum.com/threads/amd-personal-internet-communicator.990629/
- https://web.archive.org/web/20071022022658/http://www.linuxdevices.com/news/NS6147197554.html
- https://web.archive.org/web/20071022135648/http://pclab.nectec.or.th/wiki/index.php/Hardware#AMD_Personal_Internet_Communicator

## Credits

- [Photo](https://commons.wikimedia.org/wiki/File:50x15_Personal_Internet_Communicator_(PIC).jpg)
