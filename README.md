# m17n-db-bn-national-jatiya

## Bengali input method for National Jatiya layout developed by Bangladesh Computer Council

## About this layout:

Layout taken from

https://github.com/OpenBangla/OpenBangla-Keyboard/blob/master/data/National_Jatiya.json

and ported to m17n-db, merging in differences /usr/share/X11/xkb/symbols/bd as far
as possible, giving priority to National_Jatiya.json in case of a conflict.

One of the conflicts is that National_Jatiya.json has ZWNJ on ` and
AltGr+` and ZWJ on ~ and AltGr+~ whereas /usr/share/X11/xkb/symbols/bd
produces the ASCII characters ` and ~ on these keys.

See also:

https://en.wikipedia.org/wiki/Bengali_input_methods#/media/File:KB-Bengali-Jatiyo.svg

The layout picture from Wikipedia shows a few characters on AltGr which do exist
neither in National_Jatiya.json nor /usr/share/X11/xkb/symbols/bd.

## Mapping

See the picture from Wikipedia or the contents of the bn-national-jatiya.mim file.

## Dependencies

You will need to install

* ibus-typing-booster or ibus-m17n or both.
* Any Unicode font supporting Bengali https://en.wikipedia.org/wiki/Bengali_alphabet

## Installation

``` bash
$ mkdir -p ~/.m17n.d/
$ cp bn-national-jatiya.mim ~/.m17n.d/
$ ibus restart
```

If ibus-m17n is installed ibus should list the newly added input method:

``` bash
$ ibus  list-engine | grep  -i national-jatiya
  m17n:bn:national-jatiya - national-jatiya (m17n)
```

(Note: If only ibus-typing-booster but not ibus-m17n is installed, the
“national-jatiya” input method will not be listed in the output of
`ibus list-engine`)


## Adding ibus-typing-booster and “bn-national-jatiya” to your desktop:

You need to first add ibus-typing-booster to your desktop.

See the chapter “Adding ibus-typing-booster to your desktop”
in the ibus-typing-booster online documentation:

https://mike-fabian.github.io/ibus-typing-booster/docs/user/

Then you need to open the setup tool of ibus-typing-booster and add
the “bn-national-jatiya” input method in the tab for “Dictionaries and
input methods”.  you should be able to add a “bn-national-jatiya”
Detailed instructions for this are in the chapter “Basic setup for
your language” in the ibus-typing-booster online documentation:

https://mike-fabian.github.io/ibus-typing-booster/docs/user/

## Adding the ibus-m17n input method to your desktop:

### If you are  using Gnome3:

Open the regional settings in the gnome-control-center. Either from
the gnome panel by clicking on the icon showing a wrench and a
screwdriver. Then the gnome-control-center opens. Click on the flag
to go to the regional settings. You can also open the regional settings
directly by doing this on the command line:

``` bash
$ gnome-control-center region
```

In the regional settings dialog, click on the “+” button at the lower
left corner of the dialog to add an input method. In the search dialog
which opens, click on the three vertical dots at the bottom.  Enter
"jatiya" into the search field. Click on “Bangla”.  Select
“Bangla (national-jatiya (m17n))” and click on the “Add” button.

### If you are not using Gnome3:

Start ibus-setup and add the “national-jatiya (m17n)” input method (Search
for “Bangla”). Don’t use ibus-setup if you are using Gnome3, it
does not work for Gnome3!
