Automatically exported from code.google.com/p/graffle2svg

# Graffle2SVG #

## Summary ##

Application to convert .graffle files to .svg. This allows .graffle files to be viewed by users on Windows/Linux/BSD, where Omnigraffle is not available.

(note the conversion is one-way - this application does not convert .svg files back to omnigraffle)


## Installation - Windows Binaries ##

**If you have access to svn, using the version in trunk is recommended(see below).** (Windows binaries are made very infrequently and may lag behind trunk)

  * Download the windows binary zip file from the downloads page.
  * Extract it to a directory on your machine.
  * From the command line, run the command:

```
graffle2svg.exe graffle_file_in.graffle svg_file_out.svg
```

to convert a file graffle\_file\_in.graffle to svg\_file\_out.svg.

(or run `graffle2svg.exe --help` for full usage instructions)

  * If you get a message complaining about msvcr71.dll then download the "Microsoft Visual C++ 2008 redistributable package" from microsoft.com.

  * The "graffle2svgview" application included in the standard python package is not included in the windows binaries.

  * I do not have easy access to any windows computers to test on - binaries were created on Vista, but should work on other releases.

## Installation from SVN ##

(Commands given are on Linux, but should be similar on Windows)

Note: On some distributions you will have to install setuptools first - on Ubuntu this is sudo apt-get install python-setuptools

```
# Check out the project
svn checkout http://graffle2svg.googlecode.com/svn/trunk/ graffle2svg-read-only
# change to the new directory
cd graffle2svg-read-only
# install Graffle2SVG
sudo python setup.py install
```


It should now be installed.

## Converting a Graffle file ##

Two commands should have been installed - **graffle2svg** and **graffle2svgview**

graffle2svg will convert a file to an svg.

e.g.

```
graffle2svg myfile.graffle myfile.svg
```

(run with the --help argument for more information)

graffle2svgview will first convert a graffle file to a temporary .svg file, and then try to open it with your standard svg viewer - effectively acting like a viewer for graffle files.

e.g.

```
graffle2svgview myfile.graffle
```

## Project Goals ##

The primary goal when creating this project was to allow Linux/Windows users to view technical documentation received in the OmniGraffle .graffle format from Mac users.

Pixel-perfect conversion has not been a specific goal, although patches are welcome.

This application does not attempt to replicate the functionality of the OmniGraffle application.

## Project Status ##

The majority of objects and transformations are converted correctly - however text currently displays noticeably differently, due to a very simple RTF.

graffle2svg will also not handle .graffle files which are actually gzip'd directories including images yet.

## Language ##

Graffle2SVG is written in pure Python it should not have any other dependencies.

## License ##

BSD - feel free to use build on this work (patches are welcome)

### Notes ###
Omnigraffle is a trademark of The Omni Group.
Apple, Mac, and Macintosh are copyright Apple Computer, Inc.
Other names and marks mentioned herein may be trademarks of their respective companies.
