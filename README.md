# Raspberry Pi Solutions
How you can use my software for Raspberry Pi

I try to make my software platform independent as good as I can. That means, the source code can be compiled for different hardware and operating systems by using a cross compiler or one that can run and work on the target system. You should find the IDE for all of that at lazarus-ide.org and a suitable compiler at freepascal.org. I recommend to start with lazarus-ide.org, because it already contains a compiler for several systems or a guide, how to install it. If you are not a programmer and don't want to be one, start with the binaries, as follows. If that would not work, you can continue fitch the hints about compiling yourself without or with programming knowledge. Because Lazarus is easy to use, you should be able to compile without programming knowledge, if your system is, what the compiler expects.

Use compiled Binaries
---------------------
Sometimes a project has a guide, how to install the app to your system. If not, or if it does not answer all of your qustions, use the following hints.
View, whether a repository contains a directory lib/arm-linux. If it is of an application project, this contains an executable binary file. In many cases it is the only file that you have to copy to your Raspberry Pi. Care for that your copy is executable! If it is a GUI app, run it in an X terminal. If it stops with fault or error messages, care for solutions after these hints. In most cases you should not need programming or language knowledge. 

Compile with or without Object Pascal knowledge
-----------------------------------------------
If there is no binary, or you cannot make it work after the previous guide, compiling the project to the target device could help. It can happen, that you cannot execute all necessary steps on your target device. Then the next easy solution might be, to compile on a device with more RAM (>=1 GB?) with compatible CPU and the same OS version and copy the binary result to your target device with less RAM (i.. 0.5 GB). Raspbian has the packages "fpc", "fpc-source", and "lazarus". They can be installed after the usual way of package installation for Raspbian. If you want to use another Linux distribution package, names might differ or packages might not exist. You can also try to compile on Raspbian and execute on another distribution. Success might happen or not.
The IDE can be started with the command "startlazarus" or "lazarus". The first start might ask you some questions or show settings. You can agree with everything that is not a fault or error message. In case you are in doubt, you can agree, too. With some luck you will not have problems.
To compile an application project, open the .lpi file from the repository's root directory as project in the IDE. When there are missing packages during that, cancel the opening! You have to install them in Lazarus. You should find a repository with the package name in my GitHub. Else ask me! The easiest way is to fetch that repository, open the package file from the Package menu of the IDE, then select from the Package form the usage to install it. This recompiles Lazarus. After my experience the procedure requires a device with at least 1 GB RAM from which is as much as possible free (no unnecessary background processes). I use a Raspbian Lite without X and run Lazarus via a SSH connection that uses the X server of the SSH host.
If it is a GUI app, click the run button (arrow) or choose the related command from the main menu. If the compile is successfully, the app runs immediately, and you can try it. To run an application, that requires special hardware (periphery), this must be available and configured equal to the target system, where you want to use the binary finally. Else you cannot run it successfully, but if the compile was successfully, you find the executable in the subdirectory lib/arm-linux or in the root directory of the repository. To compile without a run is also the suggested way to get a binary of a non-GUI app.
Compiling a package might also require additional packages. You have to fetch such packeges as described for the package you want to compile. Then open that additional package. Then go back to the package and compile it.

Everything, that you have to do, has to be done only one time, when your Lazarus is fresh and new. When you will have done it on your development kit one time, you can use it for future compilations, too, because most settings and packages are used for many different projects of me you might use.

Solutions for Object Pascal programmers
---------------------------------------
If you already know Lazarus and how to use it, the procedures I described before should be clear for you. Additionally you can solve problems, that require debugging the source code. Alternatively, you might prefer to cross-compile because you know, how to do it. Unfortunately, beginners cannot do it, because easy guides that are found in Internet are so old, that they don't work with newest versions of Lazarus or Free Pascal, or they are incomplete or inaccurate, so that begginners might not be able to follow them without problems. There seems to be the same problem with the few available books. Therefore you are invited to help me update this guide with things you know or found out. 

Send me messages, links, or pull requests to take part in this project!

Have fun!

Andreas
