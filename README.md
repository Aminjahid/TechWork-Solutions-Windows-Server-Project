# 🖥️ TechWork Solutions GmbH – Windows Server Infrastructure Project

Welcome to the **TechWork Solutions** IT Infrastructure Project! 
This project demonstrates a complete, highly available, and secure Windows Server 2025 enterprise environment built and documented as part of my System Administration portfolio.

---

## 📄 Project Documentation (PDF)
You can view the full step-by-step PDF documentation with all screenshots here:  
👉 **[Download / View Full PDF Documentation](./Aminullah%20Sardari%20-%20Abschlussprojekt-Version2.pdf)**

---

## 🌐 Network Architecture & Topology

===================================================================================
                               TECHWORK.LOCAL DOMAIN
===================================================================================
 [ TW-DC01 ] (192.168.100.10) - Primary Domain Controller
  ├── Roles: AD DS, DNS, DHCP, IIS, RDS, Print Server, WAC
  └── OS: Windows Server 2025

 [ Failover Cluster ] (High Availability)
  ├── Node 1: TW-CL1 (192.168.100.11)
  ├── Node 2: TW-CL2 (192.168.100.12)
  └── Storage: TW-STOR1 (192.168.100.13 - iSCSI Target Server)

 [ Client ]
  └── Workstation: TW-CLIENT01 (192.168.100.50 - Windows 11 Pro)
===================================================================================

**📋 Project Modules & Implemented Topics (13 Themes)**
Domain Setup: Promoted TW-DC01 to Domain Controller for techwork. local.

Directory Structure: Created Organizational Units (OUs) for Departments (HR, IT, Finance) and Users.

DHCP & DNS: Configured Scope (192.168.100.50 - 192.168.100.200), Lease Times, reservations, and Forward/Reverse Lookup Zones.

Created shared directory structure (X:\Freigaben).

Configured NTFS Access Control Lists (ACLs) and Share Permissions based on the Least Privilege Principle for department groups.

Created and linked GPOs (e.g., GPO-Teammwall, Centralized Wallpapers, Security Settings, Network Drive Mapping).

Tested enforcement via gpupdate /force and gpresult /r.

Configured Storage Pools using virtual disks.

Provisioned Resilient Storage Spaces with Mirroring/Parity for fault tolerance.

Enabled BitLocker Drive Encryption on data volumes.

Backed up Recovery Keys securely to Active Directory Domain Services.

Installed the Data Deduplication role on file server volumes.

Optimized storage capacity and analyzed space-saving metrics.

Implemented Quota Management (Hard & Soft Quotas) on user directories.

Configured File Screening to block unauthorized file types (e.g., .exe, .mp3).

Deployed Internet Information Services (IIS) web server role.

Hosted a custom internal company homepage (http://localhost / http://tw-dc01.techwork.local).

Configured Session-based Desktop Deployment and RemoteApp functionality.

Managed user session limits and remote access permissions.

Deployed Print Management role.

Installed network printers and deployed them to clients via Group Policy (GPO).

Installed and configured Windows Admin Center for browser-based, centralized server management.

Integrated remote management for TW-DC01 and cluster nodes.

Installed the Windows Server Backup feature.

Configured automated bare-metal backups and performed successful file-level recovery tests.

Deployed TW-STOR1 as an iSCSI Target Server.

Configured a 2-node failover cluster (TW-CL1 & TW-CL2).

Validated cluster configuration, quorum witness, and tested failover capabilities.

🛠️ Tools & Technologies Used
Operating Systems: Windows Server 2025, Windows 11 Pro

Hypervisor: VMware Workstation Pro

Core Technologies: AD DS, DNS, DHCP, GPO, FSRM, IIS, RDS, iSCSI, Failover Cluster, WAC, PowerShell
