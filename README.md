# Muhammad Azhar – Cloud & Systems Engineer
VPS • Linux • Server Recovery • Backups


## Emergency VPS Data Recovery & Website Backup

**Client:** Confidential  
**Environment:** Linux VPS (CyberPanel / SSH)  
**Timeline:** Emergency recovery before permanent VPS suspension


### Situation
The client’s hosting provider was permanently suspending the VPS, which contained multiple websites and databases. Immediate action was required to secure critical data before the server was permanently suspended, to prevent irreversible loss.


### Challenges
- Limited time window before permanent suspension  
- Large backup files (~16GB) making full download impractical  
- Permission and filesystem restrictions on root directories  
- Active database and website files that could change during backup  
- Need to extract and transfer a **specific critical website** (DesignCosmics.com) safely


### Solution
- Verified and secured **database backup** first  
- Created a **website-specific archive** for DesignCosmics.com instead of downloading the entire 16GB folder  
- Used **rsync** and **tar** for reliable incremental file transfer  
- Managed Linux → Windows file transfer using WSL (Windows Subsystem for Linux)  
- Ensured integrity of all backups before removing server-side copies


### Technical Execution

```bash
# Secure database transfer from VPS to local system
rsync -avzP root@VPS_IP:/root/all_databases_backup.sql ~/VPS_Backups/

# Create a website-specific archive to avoid full backup
tar -czf /root/designcosmics_files_backup.tar.gz -C /home designcosmics.com

# Download website archive safely to local system
rsync -avzP root@VPS_IP:/root/designcosmics_files_backup.tar.gz ~/VPS_DesignCosmics/





