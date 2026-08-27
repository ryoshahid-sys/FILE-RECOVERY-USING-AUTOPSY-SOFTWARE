# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:

Recovered Deleted File List and Details



<img width="641" height="380" alt="WhatsApp Image 2026-08-26 at 5 55 44 PM" src="https://github.com/user-attachments/assets/2d5b8766-aed2-4f1e-8e17-cd8262a09e9f" />
<img width="1600" height="844" alt="WhatsApp Image 2026-08-26 at 5 56 52 PM" src="https://github.com/user-attachments/assets/b5e5c03e-1ffb-4c7f-9151-c93179ba6157" />
<img width="1072" height="673" alt="WhatsApp Image 2026-08-26 at 5 55 55 PM" src="https://github.com/user-attachments/assets/50e2a567-e80a-4f7c-a8e6-2872a5ec42c4" />
<img width="1077" height="660" alt="WhatsApp Image 2026-08-26 at 5 56 05 PM" src="https://github.com/user-attachments/assets/f0c5274b-c0ec-4279-95a1-218920d9dc1f" />
<img width="1600" height="849" alt="WhatsApp Image 2026-08-26 at 6 32 30 PM" src="https://github.com/user-attachments/assets/c58c8ee3-e987-4ac8-b9ee-9d73f2cb7725" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
