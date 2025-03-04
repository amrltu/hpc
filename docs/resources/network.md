The **High-Performance Computing (HPC) system** at Tribhuvan University is hosted at the **Information Technology Innovation Center (ITIC), Tribhuvan University**. The system ensures **secure, reliable, and high-speed connectivity** for researchers accessing computational resources remotely or within the university network.

## Network Architecture
The TU HPC network infrastructure is built for **efficient data communication** and **secure remote access**. It consists of:

### **1. Hosting & Connectivity**
- The HPC system is **physically hosted at TU ITIC**.
- **Network Address Translation (NAT) is managed by TU ITIC and the TU Registrar Office**.
- Connectivity is **based on a standard Ethernet network**, **not Infiniband**.

### **2. External & Internal Access**
- **Remote Access**: Users connect to the HPC system via **SSH (Secure Shell)**.
- **Internal Network**: Compute nodes communicate over a **local Ethernet network**.

### **3. Data Transfer**
- **Secure file transfer** via SCP, SFTP, and Rsync.
- **Scratch storage for temporary data transfer optimization**.

## Security Measures
TU HPC implements multiple **security policies** to protect user data and system integrity:

### **1. User Authentication & Access Control**
- **Centralized authentication system** to manage user credentials.
- **SSH key-based authentication** for secure remote access.
- **Role-based access control (RBAC)** to restrict administrative privileges.

### **2. Firewall & Network Security**
- **Firewall rules managed by TU ITIC** to restrict unauthorized access.
- **Network traffic monitoring** to detect and mitigate suspicious activity.
- **Isolation of compute nodes** from direct external access for security.

### **3. Data Protection & Compliance**
- **Regular system backups** for critical user data only.
- **Data encryption** for sensitive research projects.
- **User activity logging** for compliance and audit purposes.

## Future Enhancements
TU HPC aims to improve **networking and security infrastructure** by:

- Implementing **VPN-based secure access** for external researchers.
- Expanding **network bandwidth** to support larger datasets and AI workloads.
- Enhancing **intrusion detection systems (IDS) and automated monitoring**.

For more details on accessing the network securely, visit the [Access & Accounts](../access/registration.md) page.

> _Ensuring secure and efficient high-performance computing!_ 🚀
