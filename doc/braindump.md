
NoFlo & fabmodules
==================

Goals
----------------
1. Enable building user interfaces for fabmodules using web technology
2. Enable integrating fabmodules into larger automated workflows with other SW,
including inputting custom CAD models, documentation/publishing
3. Enable writing machine output modules in NoFlo/JS
4. Enable writing toolpath generation modules in NoFlo/JS


Each fab-module is generally a separate program, that takes
input and output file paths and a set of parameters as arguments.
It then transforms the input into the output.
Multiple stages are done using multiple programs.

Using a NoFlo node.js component for each program,
one can expose the parameters and filenames as ports.
The component would launch the program with given parameters,
and send a message with the filename which contains the output.
Operation needs to be async, handle multiple overlapping requests,
and send input filename as group for output.

A component for generating a random file path would be useful,
or componets would do this automatically for their output.
Also for deleting temporary files.

Proof-of-concept
-----------------
* Mill a PCB from .eagle file using Roland Modela MBX-15?



Opening up fabmodules
=====================
Problems:
* No public accessible code repository
* .zip files for older releases not available, URL not versioned
* .zip has code in toplevel instead of inside fabmodules-$version dir
* No public issue tracker
* No public mailing list / discussion forum


People working on fabmodules
--------
- Neil
- Nayda
- Ilan
- Fiore
- Shohei
- Jon
