# Forked from https://github.com/andysworkshop/avr-stl

## Description

After trying a few different AVR STL implementations i settled on this one as it seemed to work well for my needs and not use excessive memory when using things like std::vector

In this fork i have converted it into a standalone Arduino Library so that the code does not need to be mixed with the existing Arduino library code by copying into the Arduino installation.

To achieve this i have had to move the source files out of the "include" sub folder and create an additional header file to simplify the inclusion of the library into a project. I also needed to add a source file from the Arduino installation (from Arduino v1.8.5).

New files:
AvrSTL.h
pnew.h

Files copied from the Arduino installation:
avr/pgmspace.h
This was required to make it compile as a standalone library

## Usage

Clone the project into your Arduino/libraries folder into a folder named AvrSTL

git clone https://github.com/chrisckc/avr-stl.git AvrSTL

Include the library in your project and add the header file:

```
#include <AvrSTL.h>
```

Include the template you want to use after the header inclusion, for example:

```
#include <AvrSTL.h>
#include <vector>
using std::vector;
```

# Original Readme.md
# The C++ Standard Template Library for the Arduino

This is the source code that accompanies my [blog article](http://andybrown.me.uk/2011/01/15/the-standard-template-library-stl-for-avr-with-c-streams/) regarding porting the SGI C++ STL to the Arduino. Please read the article for full details.
