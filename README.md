# N-body simulation using Barnes-Hut
A parallel implementation of the Barnes-Hut tree algorithm for performing N-body simulation.
## Group members
1. Samyak Jain
2. Nihar Dwivedi
## Instructions for running the code:
1. Run the following command to know the number of available threads on your test system-
```
    lscpu
```
2. Run the following commands to compile the project-
```
    cd src
    make
```
3. Execute the compiled executable by runnning it with the given command line arguments -
```
    ./barneshut <thread count> <number of clusters> <number of bodies>
                <number of simulation steps> <theta for quadtree>
                <random seed for initialization> [output file]
```
4. The results of the simulation will be saved in the [output file] that's saved in the same location.
## Documentation
The comeplete project report with the results and outputs can be found in the [project report](https://github.com/SamyakJain19/N-body-simulation-using-Barnes-Hut/blob/master/Documentation/EC526_FinalProject_Report.pdf) in the Documentation folder.
