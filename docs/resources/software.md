
The **HPC system at Tribhuvan University** provides a **diverse range of software tools and libraries** to support research in **computational physics, AI, molecular dynamics, and high-performance computing applications**. The software environment is managed using **environment modules**, allowing users to load specific software versions as needed.

## Available Software & Modules
Users can view the available software modules using the following command:
```bash
module avail
```
The following software and tools are currently installed on TU HPC:

### **1. Compilers & Development Tools**
- **Intel Compiler (icc, ifort)**: `intel/2022.2`, `intel/2013`
- **GNU Compiler Collection (GCC)**: `gnu/5.4.0`, `gnu/8.3.0`
- **LLVM Compiler Infrastructure**: `compiler-rt/2022.0.2`
- **CUDA Toolkit**: `cuda/10.2`, `cuda/11.2`
- **OpenCL Development Tools**: `oclfpga/2022.0.2`
- **CMake**: `cmake/3.15.4`

### **2. Mathematical Libraries**
- **FFTW (Fast Fourier Transform)**: `fftw/3.3.10`, `fftw/3.3.10_Intel`
- **LAPACK (Linear Algebra Package)**: `lapack/3.10.0`
- **Intel MKL (Math Kernel Library)**: `mkl/2013`, `mkl/2022.0.2`
- **TBB (Threading Building Blocks)**: `tbb/2021.5.1`

### **3. Scientific & HPC Applications**
- **Quantum Espresso (QE)**: `qe/7.0`, `qe/7.0-gpu`, `qe/7.2`
- **FPLO (Full-Potential Local-Orbital Code)**: `fplo/18.52`
- **GROMACS (Molecular Dynamics)**: `gromacs/2019.6`, `gromacs/2019.6-gpu`
- **NAMD (Molecular Dynamics)**: `namd/2.14`
- **Thermo_pw (Quantum Thermodynamics)**: `thermo_pw/1.7.0`

### **4. Parallel Computing & MPI Implementations**
- **OpenMPI**: `openmpi/4.1.0`, `openmpi/4.1.2_Intel`, `openmpi/2022.2`
- **Intel MPI**: `impi/4.1.3`
- **PMIx (Process Management Interface for Exascale Computing)**: `pmix/2.2.2`

### **5. Python & AI Frameworks**
- **Python**: `python/3.10.12`, `python/3.12.7`
- **Debugger & Profiling Tools**: `debugger/2021.5.0`
- **Data Parallel C++ Toolkit (DPC++)**: `dpct/2022.0.0`
- **Data Parallel Library (DPL)**: `dpl/2021.6.0`

## Using Modules on TU HPC
To use any software, load the corresponding module using:
```bash
module load <module-name>
```
For example, to load Python 3.12.7:
```bash
module load python/3.12.7
```
To check currently loaded modules:
```bash
module list
```
To unload a module:
```bash
module unload <module-name>
```

## Software Installation Requests
If users require additional software, they can request installations by contacting **HPC support**. 

For more information on using software efficiently, visit the [HPC User Guide](../tutorials/guides.md).

> _Optimized software environment for high-performance computing!_ 🚀