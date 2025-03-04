Users working on **TU HPC** need to transfer files between their local systems and the HPC cluster. **Globus is not available**, so users must use standard **secure file transfer methods** like `scp`, `rsync`, and `sftp` for **safe and efficient data transfer**.

## 1. Secure File Transfer Using SCP
The `scp` (Secure Copy Protocol) command allows users to copy files **securely over SSH**.

### **Uploading a File to HPC**
From your local machine, use:
```bash
scp myfile.txt username@tu-hpc-ip:/home/username/
```
This copies `myfile.txt` from your local system to your **home directory** on TU HPC.

### **Downloading a File from HPC**
```bash
scp username@tu-hpc-ip:/home/username/myfile.txt ./
```
This downloads `myfile.txt` from the HPC system to your local system.

### **Transferring Entire Directories**
```bash
scp -r myfolder username@tu-hpc-ip:/home/username/
```
The `-r` flag copies entire directories recursively.

## 2. Efficient File Transfer with Rsync
For **resumable and optimized** file transfers, `rsync` is recommended.

### **Uploading a Directory with Rsync**
```bash
rsync -avz myfolder username@tu-hpc-ip:/home/username/
```
The `-a` (archive), `-v` (verbose), and `-z` (compression) flags ensure efficient transfer.

### **Downloading Files Using Rsync**
```bash
rsync -avz username@tu-hpc-ip:/home/username/myfolder ./
```
If a transfer is interrupted, simply rerun the same command to resume from where it left off.

## 3. Interactive File Transfer with SFTP
For interactive file transfers, use `sftp`:
```bash
sftp username@tu-hpc-ip
```
Once connected, use:
- `put myfile.txt` (Upload file to HPC)
- `get myfile.txt` (Download file from HPC)
- `ls` (List remote files)
- `bye` (Exit SFTP session)

## 4. Large File Transfers & Storage Guidelines
- **Use Rsync** for large datasets to avoid re-transfers of unchanged files.
- Store files in **appropriate directories** (`/home/username/` for personal data, `/mnt/storage0/` for temporary large-scale computations).
- **Do not store unnecessary files** in `/home/`, as space is limited.

## 5. Automating File Transfers
To automate regular file transfers, add your SSH key for passwordless authentication and create a cron job:
```bash
crontab -e
```
Example cron job to sync a folder daily at midnight:
```bash
0 0 * * * rsync -avz /local/folder username@tu-hpc-ip:/home/username/
```

## 6. Troubleshooting File Transfers
- If `scp` or `rsync` is slow, try adding `-e "ssh -C"` for compression:
```bash
scp -C myfile.txt username@tu-hpc-ip:/home/username/
```
- If the connection fails, ensure your **SSH keys** are correctly set up.
- Check available space using:
```bash
df -h
```

> _Efficient and secure file transfer for HPC workflows!_ 🚀
