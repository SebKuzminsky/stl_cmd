stl_cmd
=======

The goal of each stl_cmd is to provide a simple command line interface for manipulating binary STL files. stl_cmd aims to be easy to set up, fast and geared towards teaching basic terminal usage and programming skills in the 3D printing space.

Getting started
---------------

    git clone https://github.com/frknsweetapps/stl_cmd.git
    cd stl_cmd
    make

STL Commands
------------

This list is rather short for now, but hopefully will grow over time.

### stl_header

    stl_header [-s <header>] [-o <output file>] <input file>

Prints or sets the data in the header section of a binary STL file. The header section is rarely used, but can store a small amount of data (80 characters). Copyright info or a very brief description are some possibilities.

### stl_merge

    stl_merge -o <output file> <input file1> <input file2>

Combines two binary STL files into a single one.

### stl_transform

    stl_transform [[ <transformation> ] ...] <input file> <output file>

Performs any number of transformations in the order listed on the command line. Transformations include:

    -rx <angle> - rotates <angle> degrees about the x-axis
    -ry <angle> - rotates <angle> degrees about the y-axis
    -rz <angle> - rotates <angle> degrees about the z-axis
    -s <s> - uniformly scales x, y and z by <s> (cannot be 0)
    -sx <x> - scales by <x> in x (cannot be 0)
    -sy <y> - scales by <y> in y (cannot be 0)
    -sz <z> - scales by <z> in z (cannot be 0)
    -tx <x> - translates <x> units in x
    -ty <y> - translates <y> units in y
    -tz <z> - translates <z> units in z

Future commands
---------------

### stl_cube 

    Generate an STL file with a single cube in it.

### stl_sphere 

    Generate an STL file with a single sphere in it.

### stl_cylinder 

    Generate an STL file with a single cylinder in it.

### stl_cone 

    Generate an STL file with a single cone in it.

Teaching
--------

The goal of this project is to be a resource for teaching terminal usage and some basic programming concepts in the 3D printing space. Imagine an assignment which involves building a brick wall. Students would need to use a combination of stl_cube, stl_transform and stl_merge. The commands could be combined in a bash or <insert favorite scripting language> script with for and while loops, could accept input and use conditionals to affect the behavior of the wall. 

As more commands are added more creative assignments are possible. I hope to grow the suite of commands included in stl_cmd with that goal in mind.


Copyright 2014 Freakin' Sweet Apps, LLC (stl_cmd@freakinsweetapps.com)