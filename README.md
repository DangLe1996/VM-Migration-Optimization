# VM-Migration-Optimization
Optimizer engine for scheduling of VM migration

The purpose of this software is to generate a migraation schedule with the smallest makespan, ie. the finish time of all VM migration. The imput of this software is as follow: 

For each Virtual Machine (VM): 
- The source server (current) 
- The destination server (final) 
- The migration time expected 
- Required CPU 
- Required Memory

For each Server (SV): 
- The CPU and Memory capacity

Given the inputs above, the program will try to generate a migarting schedule, in which each VM is migrated to their final SV. The constraints of this problem is that each VM need to reserve the same CPU and Memory configuration on their current and final SV during the migration. Thus in order for a VM to start migrating, it needs to check if there is enough CPU and memory in the final SV and respect the capacity. 

To use this program, user is expected to have CPLEX 12.8 version on their environment. 

To run this program, the steps are as follows: 
1. Download this directory, which include the .exe file and sample datas. 
2. Locate the cplex1280.dll in CPLEX 12.8 directory and copy to the same folder that include the .exe file. 
3. Execute the .exe file and enter the directory to input data file
