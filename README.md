<div align="center">
    <a href="https://github.com/Ultrawipf/OpenFFBoard">
        <img width="150" height="150" src="images/openffb_logo.png">
    </a>
	<br>
	<div style="display: flex;">
		<a href="https://discord.gg/gHtnEcP">
            <img src="https://img.shields.io/discord/:XXX_INSERT_ID_HEREXXX.svg">
		</a>
		<a href="https://github.com/Ultrawipf/OpenFFBoard/stargazers">
            <img src="https://img.shields.io/github/stars/Ultrawipf/OpenFFBoard?style=plastic">
		</a>
		<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=B23BD5FGD5CH8&source=url">
            <img src="https://img.shields.io/badge/donate-PayPal-blue.svg">
		</a>
	</div>
	<h1>OpenFFBoard</h1>
	<p>
		The Open FFBoard is an open source force feedback interface with the goal of creating a platform for highly compatible simulation devices.
	</p>	
</div>	


## Disclaimer

This firmware is optimized for the Open FFBoard.
At the moment the software is far from finished. Features may not work completely or contain errors.

## Documentation

More documentation about this project is on the [hackaday.io page](https://hackaday.io/project/163904-open-ffboard).

The hardware designs are found under [OpenFFBoard-hardware](https://github.com/Ultrawipf/OpenFFBoard-hardware).

The GUI for configuration is found at [OpenFFBoard-configurator](https://github.com/Ultrawipf/OpenFFBoard-configurator).

Updates often require matching firmware and GUI versions!

## Extensions

The modular structure means you are free to implement your own main classes.
Take a look into the FFBoardMain and ExampleMain class files in the UserExtensions folder.
Helper functions for parsing CDC commands and accessing the flash are included.

The firmware is class based in a way that for example the whole main class can be changed at runtime and with it for example even the usb device and complete behavior of the firmware.

For FFB the motor drivers, button sources or encoders also have their own interfaces.

A simplified command parser is available and recommended for setting parameters at runtime. (see `CmdParser.h` and `CommandHandler.h` and the example main)

Callbacks like command parsers and timers or external interrupts are also based on virtual classes that can be implemented to add this functionality to any other module. Take a look at `global_callbacks.cpp` for some of them.

## Recommended Motors

This project is still in development. Recommended motors are not guaranteed to work but are well established in the simracing community.

| Name | Picture | Capabilities | Estimated price | Where to buy |
| ---  | ---     |      ---     |       ---       |       ---    |
| 130ST-10010 | | Rated Power: 1000W Rated Voltage: 220V Rated Speed: 1000rpm Rated Torque: 10Nm Peak Torque: 20Nm Torque coefficient: 2.2Nm/A | Please contact Mige directly for a quote. The cost for shipping is significant. Taxes and fees have to be paid. | Search for Mige on Alibaba. It is not recommended to buy 3rd party. |

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Picture</th>
    <th>Capabilities</th>
    <th>Estimated price</th>
    <th>Where to buy</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>130ST-10010<br>Small Mige</td>
    <td></td>
    <td>Rated Power: 1000W<br>Rated Voltage: 220V<br>Rated Speed: 1000rpm<br>Rated Torque: 10Nm<br>Peak Torque: 20Nm<br>Torque coefficient: 2.2Nm/A</td>
    <td>Please contact Mige directly for a quote.<br>The cost for shipping is significant.<br>Taxes and fees have to be paid.</td>
    <td>Search for Mige on Alibaba.<br>It is not recommended to buy 3rd party.</td>
  </tr>
  <tr>
    <td>130ST-15015<br>Big Mige</td>
    <td></td>
    <td>Rated Power: 2300W<br>Rated Voltage: 220V<br>Rated Speed: 1500rpm<br>Rated Torque: 15Nm<br>Peak Torque: 30Nm<br>Torque coefficient: 1.58Nm/A</td>
    <td>Please contact Mige directly for a quote.<br>The cost for shipping is significant.<br>Taxes and fees have to be paid.</td>
    <td>Search for Mige on Alibaba.<br>It is not recommended to buy 3rd party.</td>
  </tr>
  <tr>
    <td>80ST-M04025</td>
    <td></td>
    <td>Rated Power: 1000W<br>Rated Voltage: 220V<br>Rated Speed: 2500rpm<br>Rated Torque: 4Nm<br>Peak Torque: 12Nm<br>Torque coefficient: 0.9Nm/A</td>
    <td>Please contact Mige directly for a quote.<br>The cost for shipping is significant.<br>Taxes and fees have to be paid.</td>
    <td>Search for Mige on Alibaba.<br>It's not recommended to buy 3rd party.</td>
  </tr>
  <tr>
    <td>SEM HR115C6</td>
    <td></td>
    <td>Rated Power: XXW<br>Rated Voltage: 530V<br>Rated Speed: 6000rpm<br>Rated Torque: XNm<br>Peak Torque: 6.8Nm<br>Torque coefficient: XNm/A</td>
    <td>Used from e.g. Ebay</td>
    <td></td>
  </tr>
  <tr>
    <td>34HS59-5004D Stepper</td>
    <td></td>
    <td>Amps/Phse: 5A<br>Voltage: 5V<br>Holding Torque: 13Nm<br>Step Angle: 1.8°</td>
    <td> [stepperonline.com](https://www.omc-stepperonline.com/de/nema-34-schrittmotor-13-0nm-1841oz-in-w-bremse-reibmoment-4-0nm-566oz-in.html) </td>
    <td>~120€ + Shipping (EU)</td>
  </tr>
</tbody>
</table>

**How to contact Mige?**

-Goto Mige on Alibaba: [Alibaba.com/mige](https://hzmgdj.en.alibaba.com/?spm=a2700.wholesale.cordpanyb.2.618c7790hddpKe)

-Login or create an account

-Click on "Contact supplier"

-Type in which servomotor you want, ask for its price including shipping for the motor, cables and the better 10k encoder (if you want the 10k encoder).

Lisa is very helpfull and will answer in no time.

## Tested Encoder

Encoders that can be used with the current development. Some encoders can only be used as SinCos encoders.

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Picture</th>
    <th>PPR/CPR</th>
    <th>Estimated price</th>
    <th>Where to buy</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>CUI AMT103</td>
    <td></td>
    <td>Depends on version.<br>Up to 2048ppr or 8192cpr</td>
    <td> [Digikey.de](https://www.digikey.de/product-detail/de/cui-devices/AMT103-V/102-1308-ND/827016) </td>
    <td>~20€ + Shipping</td>
  </tr>
  <tr>
    <td>AMT132</td>
    <td></td>
    <td>Depends on version.<br>Up to 4096ppr or 16384cpr</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>E6B2CWZ6C</td>
    <td></td>
    <td>XXk</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>AMS5115</td>
    <td></td>
    <td>XXk</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>EQN1325</td>
    <td></td>
    <td>XXk</td>
    <td></td>
    <td></td>
  </tr>
</tbody>
</table>

## FAQ

**When will it be available?**

No idea. Hopefully this year (not in large quantities yet.... So probably mid next year). Prototypes are ordered and have to be tested. First boards go to developers that want to help with the firmware

**How much will it cost?**

From my estimates of parts and manufacturing a full kit should be available under 150€ if no unforseen costs come up. No promises on that though. Might be less or slightly more to cover the costs.

**How much current does the TMC driver provide?**

Its designed for 20A (Most motors are fine with under 10A and plenty strong). With a 1mOhm shunt you can get it up to 30A+

**I want it super cheap and don't need servos. Is that possible without the TMC?**

Yes. For really simple setups a halfbridge DC motor driver and encoder can be connected directly to the FFBoard (STM Interface) instead of using the TMC driver.
This way you can also use some third party motor drivers with PWM inputs.

**How can i donate?**

[Patreon](https://www.patreon.com/gigawipf) or [paypal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=B23BD5FGD5CH8&source=url)

**How can I help**

There needs to be done a lot of testing and debugging. Therfore if you have **c++** experience and/or have a motor (see recommended [motors](https://github.com/Ultrawipf/OpenFFBoard/#motors) to test with join our [discord](https://discord.gg/gHtnEcP).

### Copyright notice:

Some parts of this software may contain source code by ST.
The license applying to these files is found in the header of the file.
For all other parts the LICENSE file applies.
