# Steam Fedora Package for ARM64

Fedora package modified from [Terra](https://terrapkg.com/) and Terra has to be installed for dependencies.

Steam script modified from [ROCKNIX](https://rocknix.org/).

## Installation on distros other than Fedora

This is primarily for Fedora but Steam arm64 isnt readily available yet so im including this as a simple and easy way for people on other distros to get started (sudo/root privileges required):

#### WARNING: This will overwrite x86 Steam if you have it installed
```bash
git clone `https://github.com/JustRadical/steam-arm64-fedora.git`
cd steam-arm64-fedora
sudo mkdir -p /usr/share/steam && sudo cp *.vdf /usr/share/steam/
sudo cp steam /usr/bin/steam
sudo chmod +x /usr/bin/steam
```

## Setup

After installing the package you just run `steam` in a terminal to download, install and open steam.

### Playing games (ARM64EC Proton)

In order to play games using ARM64EC Proton you have to install "Proton 11.0 (ARM64) and "Steam Linux Runtime 4.0 - Arm64" from the Steam client:

<img width="839" height="238" alt="image" src="https://github.com/user-attachments/assets/09c2b942-686c-4997-b7a8-f10ee5d43d85" />

<img width="900" height="233" alt="image" src="https://github.com/user-attachments/assets/8e714c9e-720a-418b-bb76-27476cc4d9b4" />

After installing you can change the default compatibility tool in Steam from Settings (or alternatively you can change on a per-game basis through properties):

<img width="855" height="726" alt="image" src="https://github.com/user-attachments/assets/7fdea2bf-2dc4-4c7d-b164-b802a9804c0f" />


### Playing games (x86_64 Proton/x86_64 Native)

To play native games or through x86_64 Proton you need to have FEX installed with binfmt support and you need to have a rootfs set up.

On Fedora FEX can be installed with `sudo dnf install fex-emu` and a RootFS can be set up with `FEXRootFSFetcher`.

After setting up FEX-Emu you can simply launch your game and it will use FEX automatically if its a native or x86_64 Proton game.
