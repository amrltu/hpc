
## Storage Tiers & Configuration
The TU HPC storage infrastructure is divided into **multiple storage tiers**, each designed for specific use cases:


### **1. Software Storage**
- **Location:** `/dev/sdb1`
- **Capacity:** 470GB
- **Purpose:** Storing installed software, modules, and system libraries.
- **Access:** Read access for all users, write access for administrators.

### **2. Scratch Storage (High-Speed Temporary Storage)**
- **Location:** `/mnt/storage0`
- **Capacity:** 1.9TB
- **Purpose:** High-speed temporary storage for running computations.
- **Policy:**
  - **Non-persistent:** Data may be **deleted after job completion**.
  - Users must **regularly move important data** to home or project storage.
  
### **3. Home Directory (User Personal Storage)**
- **Location:** `/home`
- **Capacity:** 1.8TB
- **Purpose:** User-specific data, research scripts, personal files.
- **Quota:** Users have a **designated storage limit** to ensure fair use.
- **Backup:** Take your own backup.

### **4. Memory File System (Temporary In-Memory Storage)**
- **Location:** `tmpfs`
- **Capacity:** 126GB
- **Purpose:** High-speed memory-based temporary storage.
- **Use Cases:** Best for **temporary caching and intermediate data processing**.

## Data Management Policies
### **Storage Usage Guidelines**
- **Scratch Storage (`/mnt/storage0`)** should be used for active computations only, which can be also assessed inside (`/home/<user-name>/storage0`).
- **Long-term storage** should be maintained in the **home directory (`/home`)**.
- **Users must monitor their storage usage** and clean up unnecessary files.

### **Backup & Data Security**
- **Home directories** are not regularly backed up.
- **Scratch storage is NOT backed up** – users should save important data elsewhere.
- Users are responsible for **managing their research data securely**.

### **Access & Permissions**
- **Software storage** (`/software`) is managed by administrators.
- **User files** in `/home` are private but can be shared with appropriate permissions.
- **Group storage options** available for collaborative research projects.

## Future Storage Expansion
TU HPC is continuously upgrading its storage infrastructure to support:

- **Larger storage volumes** for big data research.
- **Faster access speeds** for computationally intensive workloads.
- **Enhanced data redundancy and recovery mechanisms**.

For details on managing your data efficiently, visit the [Data Management Guide](../data_management/best_practices.md).

> _Optimized storage solutions for high-performance computing!_ 🚀