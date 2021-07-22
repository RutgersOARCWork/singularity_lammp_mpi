# Creating singularity image for LAMMPS

## On Amarel

Become sudo and run the following commands:  

```
~$ module load singularity/3.6.4 mvapich2/2.2
~$ singularity build lammps_mvapich_v1.sif lammps_mvapich_v1.def  
```


## On Caliburn

Become sudo and run the following commands:  

```
~$ module load singularity/3.6.4 mvapich/2.2-gcc-4.8.5
~$ singularity build lammps_mvapich_v1.sif lammps_mvapich_v1.def  
```

If you are just using this yourself, you can change the ownership:   

```
~$ chown $USER:users lammps_mvapich_v1.sif
```

Or, you can change the permissions and make available globally

```
~$ chmod 755 lammps_mvapich_v1.sif
```

You can then submit the job using `sbatch`:  
```
~$ sbatch lammps_mvapich_caliburn.script
```
