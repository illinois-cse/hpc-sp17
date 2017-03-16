## High-Performance Computing Workshops
##### [Computational Science and Engineering](http://cse.illinois.edu/)

### Foreword

This workshop series will introduce you to basic concepts in High-Performance Computing.  If you need to use a cluster, this is a great way to get up to speed on how things work and why.

Any Unix-based machine has everything we need for the workshop. If you plan to use your personal laptop that runs Windows, you should install a terminal emulator, such as [MobaXterm](http://mobaxterm.mobatek.net/).


### Location

All workshops will be held in the EWS computer laboratory, [L520](http://ada.fs.illinois.edu/0210PLANB.html) [Digital Computer Laboratory](http://ada.fs.illinois.edu/0210.html).

**There is no sign-up for this series—walk-ins are welcome and encouraged!**

L520 DCL can be a little tricky to find if you haven't been there before. It's located in the basement, and can be accessed by going down the main staircase in DCL and turning right.

<p><img src="./img/map-l440.png" alt=""></p>

### Topics

#### Introduction to the Command Line

**Feb. 16, 11:00 a.m.–1:00 p.m.**

<p style="margin: 0px !important;">The <a href ="http://top500.org"><font style="font-weight: bold;">TOP500 Project</font></a>: The <a href ="http://top500.org/list/2016/11/"><font style="font-weight: bold;">list</font></a> of top 500 Supercomputers</p>
<!-- <h3 style="border: 0px; padding: 0px;">Linux command line</h3> -->
<p>
<b>Lesson notes:</b> <a href="./lessons/bash/single_page.html"><font style="font-weight:bold;">Single page</font></a> or
<a href="./lessons/bash/bash_multi.html">
	<font style="font-weight:bold;">Multi-page</font>
</a>
<br>
Exercises:
<a href="./lessons/bash/ex1.html"><font style="font-weight: bold;">#1</font></a>,
<a href="./lessons/bash/ex2.html"><font style="font-weight: bold;">#2</font></a>,
<a href="./lessons/bash/ex3.html"><font style="font-weight: bold;">#3</font></a>,
<a href="./lessons/bash/ex4.html"><font style="font-weight: bold;">#4</font></a>,
<a href="./lessons/bash/ex5.html"><font style="font-weight: bold;">#5</font></a>,
<a href="./lessons/bash/ex6.html"><font style="font-weight: bold;">#6</font></a>
</p>


#### Basics of Cluster Computing

**Feb. 23, 11:00 a.m.–1:00 p.m.**

Featuring Campus Cluster
<br>
<b>Lesson notes:</b> <a href="./lessons/scicomp/single_page.html"><font style="font-weight:bold;">Single page</font></a>

#### Scientific Computing on a Cluster

**Mar. 2, 11:00 a.m.–1:00 p.m.**

Featuring Campus Cluster
<br>
<b>Lesson notes:</b> <a href="./lessons/cc/cc_main.html"><font style="font-weight:bold;">Single page</font></a>

#### Threaded Parallel Computing for Engineers

**Mar. 9, 11:00 a.m.–1:00 p.m.**

This lesson on OpenMP (and the next on MPI) are available in an ipython notebook.  To view the lesson using one of the EWS machines, execute the following commands in the terminal.

```
module load gcc
source /class/cs101/etc/venv/cse/bin/activate /class/cs101/etc/venv/cse/
cd ~/Documents
mkdir hpc-sp17
cd hpc-sp17
wget -O omp-c.ipynb https://github.com/uiuc-cse/hpc-sp17/blob/master/lessons/openmp/omp-c.ipynb?raw=true
jupyter notebook omp-c.ipynb
```
A static view of the notebook is also available:
<br>
<a href="http://nbviewer.jupyter.org/github/uiuc-cse/hpc-sp17/blob/master/lessons/openmp/omp-c.ipynb"><font style="font-weight:bold;">Static View</font></a>

If you are running on your own computer and *already have OpenMP and the jupyter notebook installed*, simply navigating to your desired folder and using the last two lines is sufficient.  If you are on Windows, note that the wget command will not work, but you should be able to type the link into a browser and copy all of the text into a file named `omp-c.ipynb`.

##### OpenMP on OS X
If you are using a personal laptop computer running OS X operating system, you have to install GNU GCC without multilib support. The reason behind this is that clang — the default compiler on a Mac computer — does not support OpenMP. Moreover, gcc is just a symbolic link to clang. The easiest way to install GNU GCC is to use [Homebrew](https://brew.sh/):

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor  ; # fix as many errors/warnings as possible
brew install gcc --without-multilib
```

#### Distributed Parallel Computing for Engineers

**Mar. 16, 11:00 a.m.–1:00 p.m.**

The [Message-Passing Interface](http://www.mcs.anl.gov/research/projects/mpi/) is the *de facto* standard for all large-scale distributed-memory cluster computing. We will examine the basics of this standard in C (and can touch on C++ and Fortran), as well as discuss some numerical coding applications and considerations. Programming experience with C or C++ is assumed.

To view the lesson using one of the EWS machines, execute the following commands in the terminal
```
module load mpich2
source /class/cs101/etc/venv/cse/bin/activate /class/cs101/etc/venv/cse/
cd ~/Documents
mkdir hpc-sp17
cd hpc-sp17
wget -O mpi-c.ipynb https://github.com/uiuc-cse/hpc-sp17/blob/master/lessons/mpi/mpi-c.ipynb?raw=true
jupyter notebook mpi-c.ipynb
```
If you prefer to use openmpi instead of mpich2, you can can change that in the first line.  A static view of the notebook is also available:
<br>
<a href="http://nbviewer.jupyter.org/github/uiuc-cse/hpc-sp17/blob/master/lessons/mpi/mpi-c.ipynb"><font style="font-weight:bold;">Static View</font></a>

##### MPI on OS X:
If you are using a personal laptop computer running OS X operating system, you have to install an mpi compiler. The easiest way to get it on a Mac is to use [Homebrew](https://brew.sh/):

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor  ; # fix as many errors/warnings as possible
brew install gcc --without-multilib
```