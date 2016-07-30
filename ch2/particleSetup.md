# Particle Core Setup

> We want to setup the particle core via usb.

### 1. Plug in your usb cable to your computer and the particle core.

### 2. Run particle-cli setup
```
particle setup
```

### 3. Enter your email address and password, this will create an account on particle.io.

### 4. Detect your wifi, you should have a handout that contains the wifi info, use it to send your particle core the wifi information.

You should see the core light go from blinking blue to breathing cyan:

http://docs.particle.io/core/connect/

If you get any errors please let one of the mentors know.

### 5. Flash the core

> You will need to have dfu-util installed to load firmware to a usb connected device.
- OSX dfu-util
with homebrew:
`brew install dfu-util`
- Linux
- windows
https://community.particle.io/t/tutorial-installing-dfu-driver-on-windows-24-feb-2015/3518
> Once your particle core is connected via wifi, we need to flash the core with the voodoospark cpp file

### 6. Checkout voodoospark

```
git clone  https://github.com/voodootikigod/voodoospark.git
cd voodoospark
```

### 7. Flashing the voodoospark firmware

Before flashing the firmware you will need to get your particle flashing yellow so that it can be detected
To do this:
  - Press on both buttons
  - release the reset button while still pressing on the mode button
  - when the particle starts blinking yellow, you can release the mode button and it is now ready to flash

```
particle flash --usb firmware/voodoospark.cpp --force
```

### 8. Get your Device ID and Access Token

> To get your device id simply Run

```
particle list
```

> To get your access token

In you home directory there should be a folder called `.particle` and in that folder a file called `particle.config.json` - in that file should be your access token.
