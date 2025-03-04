
## HPC Cluster Architecture
TU HPC is structured into multiple **compute nodes**, ensuring scalability and efficiency. The key components of the infrastructure include:

### **1. Compute Nodes**
TU HPC consists of **multiple compute nodes**, categorized into different partitions:

- **Normal Partition:** General-purpose nodes for CPU-based computing.
- **Protein Partition:** Dedicated GPU node for high-performance computing.
- **FPLO Partition:** Nodes configured for specific research applications.

#### **Node Configuration**
- **Total Compute Nodes:** 10
- **CPU Architecture:** x86_64
- **Processor Model:** Intel(R) Xeon(R) CPU E5-2680 v2 @ 2.80GHz
- **Total CPU Cores:** 20 per node (10 cores per socket, 2 sockets per node)
- **Threading:** 1 thread per core
- **NUMA Nodes:** 2 (Ensuring optimized memory access)

### **2. Job Scheduling System**
- **SLURM-based workload manager** for efficient job scheduling and resource allocation.
- Supports **batch and interactive job submission**.
- Users can specify **CPU, GPU, memory, and time requirements** for optimal usage.

### **3. GPU Infrastructure**
- **Dedicated GPU Node:** Available under the **Protein Partition**.
- Supports **CUDA and OpenCL-based parallel computing**.
- Optimized for **deep learning, molecular dynamics, and AI research**.

### **4. Storage & File Systems**
TU HPC provides a **multi-tiered storage system** to support computational research:

- **Root Storage:** `/dev/mapper/centos-root` – 50GB (OS & system files)
- **Software Storage:** `/dev/sdb1` – 470GB (Installed software and modules)
- **Scratch Storage:** `/mnt/storage0` – 1.9TB (High-speed temporary storage)
- **Home Directory:** `/home` – 1.8TB (User personal storage)
- **Memory File System:** `tmpfs` – 126GB (High-speed temporary memory storage)

### **5. Networking & Connectivity**
- **High-speed interconnect** for low-latency data transfer between nodes.
- **Secure SSH access** for remote login.

## Performance & Scalability
The HPC infrastructure at TU is designed to support **high-throughput computing (HTC) and massively parallel processing (MPP)**. It provides:

- **Scalability** to accommodate growing computational demands.
- **Resource optimization** to maximize job efficiency.
- **Flexible configurations** for different research requirements.

## Supported Workloads
The compute infrastructure supports a wide range of research activities, including:

- **Computational Physics & Chemistry**
- **Machine Learning & Deep Learning**
- **Molecular Dynamics Simulations**
- **Weather & Climate Modeling**
- **Structural Engineering & Finite Element Analysis**
- **High-Performance Data Analytics**

## Future Upgrades
TU HPC is continuously expanding with:

- **More GPU nodes** for AI and scientific computing.
- **Increased storage capacity** for big data applications.
- **Enhanced networking and security** to ensure seamless operations.

For more details on how to access and utilize TU HPC resources, visit the [Getting Started Guide](../getting_started/ssh.md).

> _Empowering research with high-performance computing!_ 🚀
