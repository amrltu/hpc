After gaining access to the **HPC system at Tribhuvan University**, users can submit jobs using the **SLURM job scheduler**. This guide explains how to run your first job, monitor its status, and optimize job submissions.

## 1. Logging into the HPC System
Before running jobs, connect to the TU HPC system via SSH:
```bash
ssh username@tu-hpc-ip
```
Ensure you are in your **home directory** or an appropriate project folder before submitting jobs.

## 2. Creating a SLURM Job Script
A job script tells the **SLURM scheduler** how to allocate resources and execute your program. Create a job script (e.g., `job.slurm`) using a text editor:
```bash
nano job.slurm
```
Add the following SLURM directives to specify job parameters:
```bash
#!/bin/bash
#SBATCH --job-name=test_job  # Job name
#SBATCH --output=output.txt  # Output file
#SBATCH --error=error.log    # Error file
#SBATCH --ntasks=1           # Number of tasks
#SBATCH --cpus-per-task=4    # Number of CPU cores per task
#SBATCH --time=01:00:00      # Time limit (hh:mm:ss)
#SBATCH --partition=normal   # Specify partition (e.g., normal, protein, fplo)

module load python/3.10.12   # Load required module
python my_script.py          # Run Python script
```
Save and exit (`CTRL + X`, then `Y` and `ENTER`).

## 3. Submitting the Job
Submit the job to the SLURM scheduler using:
```bash
sbatch job.slurm
```
This will add your job to the queue, and it will execute once resources are available.

## 4. Monitoring Job Status
To check the status of your submitted jobs, use:
```bash
squeue -u $USER
```
To view detailed job information:
```bash
scontrol show job <job_id>
```
To cancel a job:
```bash
scancel <job_id>
```

## 5. Checking Job Output
Once the job is completed, check the output and error files:
```bash
cat output.txt  # View job output
cat error.log   # View error messages (if any)
```

## 6. Optimizing Job Submissions
- Use **appropriate resource allocation** (CPU, memory, and time) to avoid long queue times.
- Run **test jobs** with small datasets before scaling up computations.
- Use **job dependencies** if running multiple interdependent tasks:
```bash
sbatch --dependency=afterok:<job_id> job2.slurm
```
- Consider using **parallel computing** (MPI, OpenMP) for efficiency.

## 7. Example: Running a GPU Job
For GPU-based workloads, modify the script as follows:
```bash
#!/bin/bash
#SBATCH --job-name=gpu_test
#SBATCH --output=gpu_output.txt
#SBATCH --gres=gpu:1        # Request 1 GPU
#SBATCH --partition=protein # Use GPU-enabled partition

module load cuda/11.2
./gpu_program

```
Submit it using:

```bash
sbatch gpu_job.slurm
```

> _Start computing efficiently on TU HPC!_ 🚀
