# Arduino ESP8266 filesystem uploader \[!\[Build Status\]\(https://travis-ci.org/esp8266/arduino-esp8266fs

Arduino plugin which packs sketch data folder into SPIFFS filesystem image, and uploads the image to ESP8266 flash memory.  
 Tested with the following Arduino IDE versions: 1.6.5-r2, 1.6.6

## Installation <a id="installation"></a>

* Make sure you use one of the supported versions of Arduino IDE and have ESP8266 core installed.
* Download the tool archive from [releases page](https://github.com/esp8266/arduino-esp8266fs-plugin/releases/latest).
* In your Arduino sketchbook directory, create `tools` directory if it doesn't exist yet. You can find the location of your sketchbook directory in the Arduino IDE at **File &gt; Preferences &gt; Sketchbook location**.
* Unpack the tool into `tools` directory \(the path will look like `<sketchbook directory>/tools/ESP8266FS/tool/esp8266fs.jar)`.
* Restart Arduino IDE.

## Usage <a id="usage"></a>

* Open a sketch \(or create a new one and save it\).
* Go to sketch directory \(choose Sketch &gt; Show Sketch Folder\).
* Create a directory named `data` and any files you want in the file system there.
* Make sure you have selected a board, port, and closed Serial Monitor.
* Select _Tools &gt; ESP8266 Sketch Data Upload_ menu item. This should start uploading the files into ESP8266 flash file system. When done, IDE status bar will display SPIFFS Image Uploaded message. Might take a few minutes for large file system sizes.

## Credits and license <a id="credits-and-license"></a>

* Copyright \(c\) 2015 Hristo Gochkov \(ficeto at ficeto dot com\)
* Licensed under GPL v2 \([text](LICENSE)\)
* Maintained by Ivan Grokhotkov \(ivan at esp8266 dot com\)

## Issues and suggestions <a id="issues-and-suggestions"></a>

File issues here on github, or ask your questions on the [esp8266.com forum](http://esp8266.com/arduino).

