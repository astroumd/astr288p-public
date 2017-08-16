# Instructor Background Overview

Students should see their UNIX environment being built up little by
little, hence a phased approach. With as little hiding of details as
possible. For example, we give them some PDF lecture notes, but we
also keep the ODP files. Of course not the answers to the homework. 

We will thus maintain a master git repo (with answers) that the
students never see.  This causes a bit of extra work on the
instructor, and it is also meant that this way you can incrementally
grow the student git repo.  Any mistakes that were fixed in the
student repo will need to be placed back into the master (astroumd)
repo.

1) simple PDF for the first (and maybe 2nd) lecture, with on-screen examples of the shell.
Pretty soon in the 2nd lecture the students will also have to install python (e.g. via
anaconda or miniconda)

2) UNIX intro should contain:

   1) logging in the "URSA" workstations with their "astro" account (not "umd")
   1) using a linux window manager (likely to be gnome3 now), although class does not depend on it
   1) the unix shell, their commands and the .bashrc startup files (cf. Linux vs. Mac)
   1) [optional] the students can also work from their laptop (linux or mac, no windows allowed, unless via putty)
   but in that case they do need to learn about ssh and vnc
       1) mac and linux treat login and interactive shell a bit different (.bashrc vs. .bash-login)
       2) but ...
       3) the BIG advantage of using your own laptop is that you have something working at home, your
       	  'astro' account will eventually disappear as well.
   1) during the semester each lesson should use and build up general unix knowledge (e.g. command of the week)
   
3) PYTHON intro with jupyter notebooks contains:

   1) we let the students install their own miniconda (or anaconda), python version 3 !!! 
   1) this means we will not use virtualenv like methods to share the distro
   1) on the ursa cluster one more thing is important:
      1) local disks vs. /ursa remote disks on URSA can make your miniconda install very slow; use "ssh ursa" and
      	 confirm your work is on a local directory (e.g. df $HOME)
   1) it is good to have a master python (e.g. via the instructor or "astromake") that works, in case students mess up
      1) students should understand how to switch to a different python (i.e. $PATH)
   1) Throughout the class a few "pip install" or "conda install" are needed to add modules, this is done on purpose so they
   see how python works
   1) after an introduction of the basic conmputational and plottin concepts we focus on:
      1) a 4D/3D datacube, reading it as a numpy array and slicing and taking moments. Galaxy Dynamics.
      1) a simple theoretical view of the gas orbits in a cube and how to simulate an observation 
      1) newtonian orbits
      1) fitting methods (again we use the data from the cube to fit a gaussian)
      

4) C or FORTRAN code, with some combination of make, cmake and autoconf.

   1) These are concepts you see all over the ASCL source codes
   2) We use athena, since it's a 1D problem and produces ascii tables that can be plotted in matplotlib
      1) athena has a peculiar model of how it is configured, compiled and used in a simulation
      2) each astronomy code is very peculiar in that sense, and you will have to adjust
   3) there is an athena notebook how to visualize after the unix shell has run some athena examples


5) Homeworks
   1) should be small, but often. In previous years too much time in lecture mode, too little hands on
   2) spring 2017 had 4 homeworks. perhaps still too few.

6) Final student presentation

   1) students browse ASCL.NET, and pick something they are interested in. they show how it's installed, used, and discuss the
      types of data that come out and what you can do with it
