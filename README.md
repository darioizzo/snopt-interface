snopt-interfaces
================

Version 2.1:

New calls to snInit/snSpec added that allow the user to define the Fortran
file unit numbers to be used with the print file, summary file, and specs file.

* Works with SNOPT 7.7+

* In C: snInitX, setPrintfileX, setSpecsfileX have additional integer arguments
   for Fortran unit numbers

* In C++: Added overloaded initialize, setPrintFile, setSpecsfile to accept
  Fortran unit numbers

* Internally, renamed f_sninit, f_snspec Fortran subroutines to f_sninitf, f_snspecf
  and changed to call sninitf, snspecf (without Fortran unit numbers and new in SNOPT 7.7).
  f_sninit and f_snspec now call snInit and snSpec with Fortran unit number

-----------------

Please see

   http://ccom.ucsd.edu/~optimizers/usage/c

   http://ccom.ucsd.edu/~optimizers/usage/cpp

for more information on how to link to the libraries and use the C/C++
interface.
