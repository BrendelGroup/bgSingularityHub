# bgSingularityHub
... a portal to our collection of [Apptainer/Singularity](https://apptainer.org/) definition and image files.

Usage assumes that you have [Apptainer/Singularity](https://apptainer.org/) installed on your system.
Check whether there is package built for your system and install with a package manager.
Otherwise, follow the instructions to [install Singularity from source code](https://apptainer.org/user-docs/master/quick_start.html#quick-installation-steps).


## Scope
We are a computational genomics group and support containers for software in
this realm.
Typically, the containers bundle multiple packages of diverse programs that are
frequently used in combination in a project.
In our own work, we seek to bundle everything that should be referenced in the
methods description of our scientific papers, thus ensuring complete technical
reproducibility of the computational work.
For a list of all available containers see [CATALOG](./CATALOG.md).

## Usage
Typical usage is illustrated below: setting up a workdir, acquiring the
desired image file, defining an alias to execute commands, and testing the
setup:

```
mkdir workdir
cd workdir
wget https://brendelgroup.org/SingularityHub/SNPat.sif 
alias rws='singularity exec -e -B ${PWD}  ${PWD}/SNPat.sif'
rws ls /opt
rws biscuit
```

## Contact

Please direct all comments and suggestions to
[Volker Brendel](<mailto:vbrendel@indiana.edu>)
at [Indiana University](http://brendelgroup.org/).
