PyRTL
=====

A collection of classes providing simple RTL specification, simulation, tracing, and testing suitable for teaching and research. 
Simplicity, usability, clarity, and extendibility rather than performance or optimization is the overarching goal.

In the package you should find the following files and Directories
* _pyrtl/_  The src directory for the module
* _tests/_    A set of unit tests for pyrtl which you can run with nosetests
* _examples/_ A set of hardware design examples that show the main idea behind pyrtl
* _checkcode_ A script you should run before you check any code into the master or development branches

If you are just getting started with pyrtl it is suggested that you start with the examples first,
to get and sense of the "thinking with pyrtls" required to design hardware in this way.  Then 
dive into the code for the object Block, which is the core data structure at the heart of 
pyrtl and defines its semantics at a high level.   

near-term todo list:
* all user visible assert calls should be replaced with "raise PyrtlError"
* all PyrtlError calls should have useful error message
* all classes should have useful docstrings
* all public functions and methods should have useful docstrings
* should have set of unit tests for main abstractions
* should be PEP8 compliant
* multiple nested blocks should be supported
* add verilog export option to block
* add multiply operation as a primitive

bigger todo projects:
* add area, clockrate, and energy estimations
(Guiding Architectural SRAM Models ICCD 2006 for memories,
Logical Effort for logic blocks and registers)
* add debug mode, where we track call stack for each wirevector initiated (and
where all errors thrown tell you where the wire was instantiated that is causing
the problem)
* add a pass to print out the block as a set of C code that implement the 
hardware block (useful for longer running tests -- like a processor model)
