### Split 2


# SPLIT 2 — ENTERPRISE STORAGE, NETWORKING, RAID, FILESYSTEMS, LINUX STORAGE, SERVERS & VIRTUALIZATION

## Objective

Build the complete enterprise-system understanding required to work with storage arrays, storage networks, RAID, filesystems, Linux storage, servers, BMCs and virtualization.

## Recommended Position

Days 31–60 of the 90-day preparation, adjusted by actual mastery.

---

# MODULE 16 — ENTERPRISE STORAGE ARCHITECTURE

## Storage Models

- DAS
- NAS
- SAN
- Storage Arrays
- Storage Controllers
- Cache
- Backplane
- JBOD
- Storage Enclosures
- Scale-Up Storage
- Scale-Out Storage

## Enterprise Components

- Storage Controllers
- Controller Redundancy
- Storage Pools
- Volumes
- LUNs
- Capacity Management
- Storage Presentation

---

# MODULE 17 — STORAGE PROVISIONING

## Topics

- Storage Pools
- Volumes
- LUNs
- Thin Provisioning
- Thick Provisioning
- Capacity Expansion
- Volume Expansion
- LUN Mapping
- LUN Masking

## Validation

- Create
- Modify
- Expand
- Map
- Unmap
- Discover
- Device Rescan
- Verify Capacity
- Verify Host Access

---

# MODULE 18 — ENTERPRISE STORAGE FEATURES

## Topics

- LUN
- Volume
- Aggregate
- Storage Pool
- Thin Provisioning
- Thick Provisioning
- Storage Tiering
- Snapshots
- Clones
- Replication
- Deduplication
- Compression
- Encryption

## Assessment

Design and explain enterprise storage provisioning.

---

# MODULE 19 — STORAGE NETWORKING

## Ethernet

- Ethernet Fundamentals
- TCP/IP Basics
- VLAN
- MTU
- Jumbo Frames

## iSCSI

- iSCSI
- CHAP Authentication

## Fibre Channel

- Fibre Channel
- Fibre Channel Switch
- WWN
- Zoning
- SAN Communication

---

# MODULE 20 — MULTIPATHING

## Topics

- Multipathing Concepts
- Path Discovery
- Path Redundancy
- Path Failover
- Path Recovery
- Active / Standby Behavior
- Multipath Performance Considerations

## Failure Scenarios

- Path Loss
- Multipath Failover
- LUN Unavailable
- Storage Network Problem

---

# MODULE 21 — RAID FUNDAMENTALS

## Topics

- RAID Fundamentals
- RAID Purpose
- Striping
- Mirroring
- Distributed Parity
- Data Protection
- RAID Performance Trade-Offs

## RAID Levels

- RAID 0
- RAID 1
- RAID 5
- RAID 6
- RAID 10
- RAID 50
- RAID 60

---

# MODULE 22 — RAID FAILURE & RECOVERY ENGINEERING

## Topics

- Degraded Mode
- Hot Spare
- RAID Rebuild
- Rebuild Performance
- Failure Analysis
- Failure During Rebuild
- Multiple Failure Scenarios
- Recovery Validation
- Consistency Check
- Background Initialization
- RAID Expansion
- RAID Migration
- RAID Creation
- RAID Deletion

## Performance

- Write Penalty
- Degraded Performance
- Rebuild Impact
- Rebuild Stress

## Project 1 Application

- RAID Creation
- RAID Deletion
- RAID Expansion
- RAID Migration
- RAID Rebuild
- Hot Spare
- Degraded Mode
- Recovery
- Consistency Validation

## Assessment

Solve realistic RAID failure scenarios.

---

# MODULE 23 — ENTERPRISE FILE SYSTEMS

## Topics

- ext4
- XFS
- ZFS Concepts
- NTFS Basics
- FAT32 Basics
- Journaling
- Allocation Methods
- Mount Concepts

---

# MODULE 24 — FILESYSTEM / STORAGE INTERACTION

## Topics

- Filesystem to Block Layer
- Filesystem Metadata
- Allocation
- Journaling
- Mounting
- Storage Presentation
- Filesystem Failure Behavior
- Filesystem Corruption Scenarios
- Recovery

---

# MODULE 25 — LINUX STORAGE STACK

## Topics

- Block Devices
- Partitions
- Filesystems
- Mounts
- LVM
- Device Mapper
- udev
- sysfs
- Storage Discovery
- Linux Block Subsystem
- SCSI Subsystem

---

# MODULE 26 — LINUX STORAGE EVIDENCE

## Commands / Tools

- lsblk
- blkid
- findmnt
- mount
- lsscsi
- dmesg
- journalctl
- systemd / Service State

## Goal

Correlate:

```text
Device
→ Kernel
→ Driver
→ Storage Subsystem
→ Filesystem
→ Workload
```

---

# MODULE 27 — LVM

## Topics

* Physical Volumes (PV)
* Volume Groups (VG)
* Logical Volumes (LV)
* Creating LVM
* Extending Volumes
* Reducing Volumes
* Filesystem Resizing
* Snapshots
* LVM Recovery
* Advanced LVM Concepts

---

# MODULE 28 — SERVER ARCHITECTURE

## Topics

* Rack Servers
* Blade Servers
* Tower Servers
* CPU
* Memory
* NUMA
* ECC Memory
* PCIe
* NIC
* HBA
* BIOS
* UEFI
* BMC

---

# MODULE 29 — BMC / SERVER MANAGEMENT

## Topics

* IPMI
* Redfish
* Telemetry
* Event / SEL
* Dell iDRAC
* HPE iLO

## Cross-Layer Relationships

* Server
* BIOS / UEFI
* BMC
* PCIe
* HBA
* NIC
* Storage

---

# MODULE 30 — VIRTUALIZATION FOR STORAGE ENGINEERS

## Fundamentals

* Virtualization
* Hypervisor
* Virtual Machines
* Virtual Disks
* Datastores
* Storage Presentation
* Virtual-to-Physical Storage Path
* Host vs Guest

## Platforms

* VMware ESXi
* VMware vCenter
* KVM
* Microsoft Hyper-V
* VMFS

## Enterprise Features

* vMotion
* Storage vMotion
* HA
* DRS
* Snapshots
* Pass-Through Concepts

## Troubleshooting

* Host vs Guest Troubleshooting
* VM Storage Latency
* VM Storage Performance
* Host Path Failure
* Virtual Storage Presentation

---

# SPLIT 2 — MASTER ASSESSMENT

Before moving to Split 3:

* [ ] Explain enterprise storage architecture
* [ ] Explain DAS
* [ ] Explain NAS
* [ ] Explain SAN
* [ ] Explain storage controllers
* [ ] Explain storage pools
* [ ] Explain volumes
* [ ] Explain LUNs
* [ ] Explain thin provisioning
* [ ] Explain thick provisioning
* [ ] Explain storage provisioning
* [ ] Explain snapshots / clones / replication
* [ ] Explain Fibre Channel
* [ ] Explain iSCSI
* [ ] Explain zoning
* [ ] Explain multipathing
* [ ] Explain path failure / failover
* [ ] Explain RAID 0 / 1 / 5 / 6 / 10 / 50 / 60
* [ ] Explain RAID degraded mode
* [ ] Explain RAID rebuild
* [ ] Explain hot spare
* [ ] Explain RAID failure scenarios
* [ ] Explain filesystems
* [ ] Explain filesystem / storage interaction
* [ ] Explain Linux storage stack
* [ ] Use Linux storage discovery commands
* [ ] Analyze Linux storage evidence
* [ ] Explain LVM
* [ ] Explain server storage architecture
* [ ] Explain BMC / IPMI / Redfish
* [ ] Explain virtualization storage
* [ ] Explain VM-to-storage communication
* [ ] Troubleshoot representative enterprise storage scenarios
* [ ] Complete Split 2 assessment

```
