# gbstag-lib : Java library for GBS-files (Game Boy Sound)
<img src="gameboy.png" alt="Game Boy" align="right">

A Java library for reading gbs files and reading / manipulating the tags.

GBS-files are sound files containing ripped chiptune music from Game Boy and
Game Boy Colour games. GBS stands for Game Boy Sound System.


## Features
* :heavy_check_mark: 100% Java (Java 8) :coffee:
* :heavy_check_mark: Supports UTF-8 encoding in the tags!
* Implements `Comparable` for sorting out of the box!

## How to use it

###Opening a gbs file
```java

Gbs gbsfile = new GbsFile("/tmp/supermarioland.gbs");
GbsTag tag = gbsfile.getTag();


System.out.println("Version number: " + tag.getVersionNumber());
System.out.println("This gbs file contains: " + tag.getNumberOfSongs() + " songs");
System.out.println("The first one is no. " + tag.getFirstSong());
System.out.println("Author:\t" + tag.getAuthor());
System.out.println("Title:\t" + tag.getTitle());
System.out.println("Copyright:\t" + tag.getCopyright())";
```

###Saving a gbs file
```java
gbsfile.save();
```

###Setting tag values
```java
Gbs gbsfile = new GbsFile("/tmp/supermarioland.gbs");
GbsTag tag = gbsfile.getTag();

tag.setAuthor("Koji Kondo");
tag.setCopyright("2000 Nintendo");
tag.setTitle("Wario Land 5");
```

## Development
For command-line or GUI programs see [gbstag](https://www.github.com/ullenius/gbstag) and [jbstag](https://www.github.com/ullenius/jbstag)


## Changelog

## Licence
LGPL 2.1

### Libraries and copyright
* Image by [Flappiefh](https://fr.wikipedia.org/wiki/Utilisateur:Flappiefh) (2013) from Wikimedia Commons. [Creative Commons Attribution-Share-Alike 3.0 Unported licence](https://creativecommons.org/licenses/by-sa/3.0/deed.en).
