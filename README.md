# P-Star Examples

This repository contains example code for the [P-Star 25K50 Micro][pstar25m] and
[P-Star 45K50 Mini SV][pstar45msv].
To use these examples, you will need a P-Star, a [Micro-USB
cable](https://www.pololu.com/product/2073), and a computer running Windows,
Linux, or Mac OS X.

The examples in this repository can be
compiled using either the [MPLAB XPress IDE][xpressinfo], an online IDE from
Microchip that does not require any software installation, or the [MPLAB X
IDE][x], a more powerful IDE that is installed on your computer.

Each example comes with a `README.md` file that explains what it does and how to
use it.


## Compiling examples with the MPLAB XPress IDE

<!-- These examples are available on the [MPLAB Xpress Code Examples][examples] page.
In the "Board" column of that page, select "P-Star 25K50" to display all the
examples for the P-Star 25K50.  (Some of those examples might be from other
sources.)  Click the "Open" button next to an example to open that example in
the online IDE. -->

<!-- If you cannot find the example you are looking for on the Examples page, you
might have to upload it to the online IDE yourself. -->

First, download this repository as a ZIP file.  Extract the folder containing
the example you want to run, and make a new ZIP file that just contains that
folder.  Next, start the MPLAB XPress IDE by opening [this link][xpressrun].  In
the IDE's "File" menu, select "Import Project" and upload the new ZIP file.

Once you have succeeded in opening the project in the MPLAB XPress IDE, you
should see some source code on the right side of your browser window, and you
should see the "Project" pane on the left side, which shows all the source and
header files in the project.

Open the "File" menu and select "Project Properties".  In the "Device" field,
enter either "PIC18F25K50" or "PIC18F45K50" depending on which microcontroller
is on your P-Star, and then click "Ok".

Click the "Make and Program Device" button (the button with a green arrow
pointing down).  This will cause the IDE to compile the program and then
download it to your computer as a HEX file.

Once you have the HEX file, you can program it onto your P-Star as described in
the "Programming using p-load" section of the [P-Star user's guide][guide].

For more information about using the MPLAB XPress IDE, see Microchip's [main
page for the MPLAB XPress IDE][xpressinfo].


## Compiling examples with the MPLAB X IDE

These examples can be compiled using the [MPLAB X IDE][x] and the [XC8
compiler][xc8], which must both be installed on your computer.

Download this repository as a ZIP file and extract it.  Each folder with a
name ending in `.X` is an MPLAB X project.  In the MPLAB X IDE, open the "File"
menu, select "Open Project...", select the folder for the project you want to
run, and then click "Open Project".

Once you have opened the project in the MPLAB X IDE, you should see it listed in
the "Project" pane on the left side of the IDE, which shows all the source and
headers files in the project.

Right-click on the project and select "Set as Main Project".

From the "Production" menu, set the project configuration to either
"P-Star_25K50" or "P-Star_45K50", depending on what type of P-Star you are
using.

From the "Production" menu, select "Build Project".  The IDE will compile the source
code into a HEX file.  You can find the HEX file and the other outputs of the
compiler in the project folder under the "dist" subdirectory.


[pstar25m]: https://www.pololu.com/product/3150
[pstar45msv]: https://www.pololu.com/product/3156
[xpressinfo]: http://www.microchip.com/mplab/mplab-xpress
[xpressrun]: https://mplabxpress.microchip.com/mplabcloud/ide
[x]: http://www.microchip.com/mplab/mplab-x-ide
[xc8]: http://www.microchip.com/xc8
[examples]: https://mplabxpress.microchip.com/mplabcloud/example
[guide]: https://www.pololu.com/docs/0J62
