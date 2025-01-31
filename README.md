# Flipper Zero asset pack with Monika from DDLC

This is a fan work, based on Monika from DDLC by Team Salvato (go try it!), the inspiration for facial expressions (based on assets/Icons/Passport icons) is by @KingBophades!

## TO-DO
- [x] base sctructure
- [ ] assets
  - [x] icons
  - [ ] animations
- [ ] set up fzmapbt
## Structure

- assets - the main asset pack source
  - Anims - Monika animations on the home screen
  - Icons - Monika icons and assets in apps (like Sub-GHz scanning or RFID emulation) and Passport icons
- development - extra assets for developing your own animations or icons
  - expressions - Monika's facial expressions adapted for Flipper format
  
## Compiling (Momentum)
### Auto way
It requires Python3 and pip3 preinstalled.

I made my own script for building asset packs for Momentum called FZMAPBT (Flipper Zero Momentum Asset Pack Build Tool).
First, make script executable.
```bash
chmod 755 fzmapbt
```

Then, launch the script
```bash
./fzmapbt
```

It will automatically compile into the 'asset_packs/' folder.

### Manual way

You must have installed Python3 and clone the repository (of course).
First, of course, clone the repo.

Then you must install dependencies for the asset packer (which will adapt files for Flipper).
```bash
pip3 install heatshrink2 Pillow
```

Move your assets folder as Monika (like this):
Before:
```
assets/
  Anims/
  Icons/
```
```
After:
Monika/
  Anims/
  Icons/
```

Now put [Momentum's asset_packer.py](https://github.com/Next-Flip/Momentum-Firmware/blob/dev/scripts/asset_packer.py) alongside the 'Monika' folder (like in example earlier)

Then run:
```bash
python3 asset_packer.py
```

You will see that picture:
```
goosedev72@Mac-Pro:~/making-zone/monikaflipper $ ls
Monika/ development/ asset_packs/ asset_packer.py
```

Now, in asset_packs/, you will see 'Monika' folder there. Now proceed to installation!
## Installation
Now installing the asset pack!
### Momentum Firmware

Compile the pack, or download precompile release.

Then, use qFlipper to upload the asset pack in this path:
FLIPPER SD/asset_packs/Monika

In that path, there will be 2 folders: 'Anims/' and 'Icons/'.

Now you can use Momentum app, Interface, Graphics, select the Monika pack.

Now explore your system!

### Other firmware (Official, Unleashed, etc.)

You need to clone the firmware source code and replace assets according to assets structure.
Sadly, only Momentum (remake of Xtreme on Official and Unleashed firmware code, made by the same developers to replace RougeMaster for stablity)
