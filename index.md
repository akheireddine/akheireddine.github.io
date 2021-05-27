
PhD student at [LRDE](https://www.lrde.epita.fr/wiki/Home) and [LIP6](https://www.lip6.fr), [MoVe](https://www.lip6.fr/MoVe) team.

Contact : akheireddine[at]lrde.epita.fr

# Information
**BMC-tool** git repository: [here](https://gitlab.lrde.epita.fr/akheireddine/bmctool).

# Test replication for CP21

## Clone BMC-tool repository 
>
```
git clone https://gitlab.lrde.epita.fr/akheireddine/bmctool
```

## Analysis mode 
### Compile
>
```
sh compile_log_mode.sh
```

### PLOT class classification for one instance

Figures will be saved in 'res_log' directory

>
```
sh plot_class_classification.sh <filename.dimacs> <output_points.csv> [time-limit] [max-memory]
```

### PLOT class classification for a set of instances
>
```
sh plot_class_classification_avg.sh <dirname> <output_points.csv>
```

### PLOT Pareto front 
input_points.csv: is computed with the above script file (plot_class_classification or plot_class_classification_avg)
>
```
sh plot_pareto_front <input_points.csv> <output_solution.csv>
```

## Experimental mode
### Compile
>
```
sh compile_exp_mode.sh
```

### Execution
Run solving with a time limit of 6000 seconds and 12Go memory limit using one of the proposed strategy: 
  * 0: state-of-the art SAT procedure
  * 1: Linear programming heuristic
  * 2: Structural BMC information

>
```
./bmctool -tool=p -c=1 -s=maple -ns=1 -sat-heuristic=<value:0,1,2> -t=6000 -max-memory=12000 <filename.dimacs>
```


## Conversion of SMV file to DIMACS format
Must specify the bound value k :
>
```
./bmctool -tool=c -k=<bound> -conv=1 <filename.smv>
```



# Teaching

 * Programamtion C L1.
 * Théorie des langages rationnels L2.

