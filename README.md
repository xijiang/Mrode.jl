# Introduction

This series of notebooks illustrate of Julia usage with examples in
Raphael A. Mrode's book, *Linear Models for the Prediction of Animal
Breeding Values* (2014, 3ed).  We can see how easily it is to use
Julia language to do the simulation and matrix operations on various
models.  A digital version of this book can be downloaded from the
publisher's website for people in NMBU.

Before writing these notebooks, I was trying to encourage people to
use Julia in my department.  I naively thought that to use Julia, it
is better to know some peripherals, like MarkDown, git/github, Visual
Studio code, key pairs and Julia package developing.  It turned out
that these tools are very foreign to many breeders.  Many people lost
clues very quickly.  To setup these thing usually cost hours.  So I
decided to use Mrode's book as a demonstration instead.  This may lead
breeders to the Julia world a bit faster.  I will then distribute the
essential tools across these notebooks.  Those tools, however, will
greatly ease your code development if you know how to use them.

Throughout these notebooks, I try to use as minimal as possible of
tools other than the Julia ecosystem.  Here are all the tools needed.

## Install Julia
You can always download Julia for various systems from [its
website](https://julialang.org/downloads/).  It is also possible to
install Julia through command line.

### Windows
In a `Cmd` prompt:
```dos
winget install julia -s msstore
```

### Linux
```bash
sudo dnf install julia # for Linux with dnf management, e.g, Fedora
sudo apt isntall julia # e.g., Ubuntu
```

Note, command line is very precise, efficient, and powerful.  I hope
you like command lines soon if not now.

If you download from https::/julialang.org, which is usually more up
to date, then I suggest you unpack the files to `/opt/julia`, and make
a soft link to `/opt/julia/latest/bin/julia` in your `~/.local/bin`.

### Mac
To be added later.

## Install Visual Studio code

Please refer https://code.visualstudio.com/docs/setup/setup-overview
for `vscode` installation.  Linux and Windows users will have command
`code` in the default path.  For Mac users, open the command palette
(shortcut `Cmd+shift+p`) and type `shell command`.  You will see two
options `install code command in path` and `uninstall code command
from path`.  Choose `install` to add it in path.

## The four modes of Julia

When you start Julia, it enters its REPL mode, that is,
*run-evaluate-print loop*.  You can use the Julia language here.  The
three other modes are:

- Package mode
  - Press key <span style="color:cyan">`]`</span> at the very
    beginning of a REPL line.  Backspace to return to REPL.
- Shell mode
  - The switch key is `;`.  Here you can use, for example `bash` (for
    Linux and Mac), `DOS`, or `PowerShell` commands.
- Help mode
  - The switch key is `?`.  You can look up help docs of a function.

## Add some packages

In a Julia REPL, press `]` to enter the Package mode.  Type beloe
```julia
add Revise, IJulia, Plots, Distributions, LinearAlgebra
```
to add these packages.

## Startup options
Create a directory `path-to-user/.julia/config`.  Create a file
`startup.jl` in this directory with content:

```julia
using Revise
ENV["EDITOR"]="code"
```

## To obtain the notebooks

If you have had `git` installed, then it is fairly easy to download
all the files:

```bash
cd your-working-direcotry
git clone https://github.com/xijiang/Mrode.jl
cd Mrode.jl
ls   # or dir in DOS
```
You can see all the files are now in this folder.

A better way to view these notebooks is just to browse them at
https://github.com/xijiang/Mrode.jl/notebooks . You can then type the
commands or sentences one by one in you own REPL.

<!--
## Let's begin
```julia
using IJulia
jupyterlab()
```

Note: Usually the Jupyter lab will be automatically loaded in your
default browser, e.g., `Firefox`.  First time user, however, might
have to do below:
```bash
jupyter-notebook list
```
Copy and paste the link with a token into your browser's address bar.
This web service is usually of address https://localhost:8888/lab .

You will see all the files in the current directory in the left pane
of the `jupyterlab`.  Let's open file `ch-01.ipynb` and start the
journey. 
-->
