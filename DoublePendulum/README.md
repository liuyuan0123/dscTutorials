DoublePendulum

============================

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Run: MAIN.m to produce a simulation

Edit: Set_Parameters.m to adjust various parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


This collection of files can be used to do the following things:

1) Derive the equations of motion (EoM) of a forced double pendulum

1a) Write the EoM to a matlab function
1b) Write the EoM to an optimized C++ function 

2) Run a simulation of the double pendulum

3) Demonstrate the MEX interface for calling a C++ dynamics function

4) Show one (somewhat complicated) way to pass an arbitrary parameter struct through a MEX interface to several different C++ functions


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Running MAIN.m will used ode45 to run a simulation of a double pendulum, using the matlab version of the dynamics function. 

You can make it use the C++ version of the dynamics function by setting P.misc.CppFlag=true in the function Set_Parameters.m.

The dynamics function supports a torque applied at each joint and an arbitrary force applied at each joint. These are all set to zero in MAIN.m to make the demo simple. 

The way that the parameters are passed to C++ is rather complicated. A detailed explanation is given by typing:  help Write_Parameter_File  at the command line.
