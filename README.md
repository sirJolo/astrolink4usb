# indi-astrolink4usb
astrolink4usb INDI driver supports [AstroLink 4 USB device](https://shop.astrojolo.com/astrolink/). AstroLink is now available with an integrated USB3.0 hub. The digital part power supply is galvanically isolated from the analog, and the data stream is opto-isolated as well. Out of the box focuser unipolar, bipolar, and microstepping control, regulated PWM outputs, switchable DC outputs, 5V regulated output,  overcurrent and overvoltage protection, temperature/humidity/sky temperature sensors – all in one box. Advanced panel software with ASCOM multidriver support to control all functions. 

# Installing INDI server and libraries
To start you need to download and install INDI environment. See [INDI page](http://indilib.org/download.html) for details. 

Then AstroLink INDI driver needs to be fetched and installed:

```
git clone https://github.com/astrojolo/astrolink4usb.git
cd astrolink4usb
mkdir build
cd build
cmake ..
make
make install
```

Then indiserver needs to be started with AstroLink drivers:

```
indiserver -v astrolink4usb
```

Now AstroLink can be used with any software that supports INDI drivers, like KStars with Ekos.
