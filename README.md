### GRBL G-Code Output for Inkscape

This Inkscape extension that allows you to save Inkscape drawings as
G-Code files suitable for plotting using [GRBL ESP32](https://github.com/bdring/Grbl_Esp32) or similar. The last tested version of Inkscape is 0.92.

Code adapted from the unmaintained [Makerbot Unicorn extension](http://github.com/martymcguire/inkscape-unicorn) by [Marty McGuire](http://github.com/martymcguire).

#### What's different?

- Parenthesis comments are now semicolon comments
- ``M300`` commands are now ``G0`` commands
- Other minor tweaks

#### Installation

Copy the contents of `src/` to your Inkscape `extensions/` folder.

Typical locations include:

* OS X - `/Applications/Inkscape.app/Contents/Resources/extensions`
* Linux - `/usr/share/inkscape/extensions`
* Windows - `C:\Program Files\Inkscape\share\extensions`

#### Usage

**Inkscape document units must be set to px** otherwise you will get tracebacks.
* Size and locate your image appropriately:
	* The extension will automatically attempt to center everything
* Convert all text to paths:
	* Select all text objects.
	* Choose **Path | Object to Path**.
* Save as G-Code:
	* **File | Save a Copy**.
	* Select **h4xidraw G-Code (\*.gcode)**.
	* Save your file.
* Plot
	* Upload your `.gcode` file to your SD card using the [GRBL ESP32](https://github.com/bdring/Grbl_Esp32) webUI.
	* Run

Feel free to fork this for your own needs.