# m17n-db-bn-national-jatiya

## Bangla Jatiyo Keyboard (National, Bengali: জাতীয়) Keyboard layout developed by Bangladesh Computer Council

## About this layout:

See:

https://en.wikipedia.org/wiki/Bengali_input_methods#Bangla_Jatiyo

Layout taken from

https://github.com/OpenBangla/OpenBangla-Keyboard/blob/master/data/National_Jatiya.json

and ported to m17n-db

## Mapping

See the description at the top of the bn-national-jatiya.mim file.

## Dependencies

You will need to install

* ibus-m17n
* Any Unicode font supporting Bengali https://en.wikipedia.org/wiki/Bengali_alphabet

## Installation

``` bash
$ mkdir -p ~/.m17n.d/
$ cp bn-national-jatiya.mim ~/.m17n.d/
$ ibus restart
```

Now ibus should list the newly added input method:

``` bash
$ ibus  list-engine | grep  -i national-jatiya
  m17n:bn:national-jatiya - national-jatiya (m17n)
```

## Adding the input method to your desktop:

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
