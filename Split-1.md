
## Split 1


# SPLIT 1 — STORAGE FOUNDATIONS, I/O, MEDIA, PROTOCOLS, PCIe & NVMe

## Objective

Build the technical foundation required to understand how storage I/O works end-to-end, how storage media behaves internally, how storage protocols communicate, and how PCIe/NVMe systems operate and fail.

## Recommended Position

Days 1–30 of the 90-day preparation, adjusted by actual mastery rather than by calendar alone.

---

# MODULE 1 — COMPLETE STORAGE I/O JOURNEY

## Objective

Understand the complete lifecycle of a storage request from application to physical media and back.

## End-to-End Flow

Application
↓
Linux Operating System
↓
File System
↓
Block Layer
↓
Device Driver
↓
Host Controller
↓
Server Hardware
(PCIe / HBA)
↓
Storage Network
(Ethernet / Fibre Channel / iSCSI / NVMe)
↓
Enterprise Storage Controller
↓
RAID / Storage Pool
↓
Storage Device
(HDD / SSD / NVMe SSD)
↓
Physical Storage Media

---

## Write Operation

- Complete Write Flow
- Application Write
- Linux Processing
- File System Processing
- Block Layer
- Device Driver
- Host Controller
- Storage Device
- Device Internal Processing
- Physical Media Operation
- Write Completion
- Response Back to Linux
- Response Back to Application

---

## Read Operation

- Complete Read Flow
- Application Read
- Page Cache Lookup
- Cache Hit
- Cache Miss
- File System
- Block Layer
- Device Driver
- Host Controller
- Storage Device
- Media Read
- DMA
- Memory
- Response Back to Linux
- Response Back to Application

---

## Assessment

Explain the complete write and read journey without notes for:

- SATA
- SAS
- NVMe

---

# MODULE 2 — HDD ENGINEERING

## Topics

- HDD Architecture
- Platters
- Tracks
- Sectors
- Heads
- Mechanical Positioning
- HDD Read Operation
- HDD Write Operation
- HDD Latency Characteristics
- HDD Performance Characteristics
- HDD Failure Behavior
- SATA HDD
- SAS HDD
- Enterprise HDD Behavior
- HDD Validation Considerations

## Mastery

Be able to explain how HDD architecture affects:

- I/O behavior
- Latency
- Throughput
- Failure behavior
- Validation

---

# MODULE 3 — NAND FLASH & SSD FUNDAMENTALS

## Topics

- NAND Fundamentals
- Cell Concepts
- Pages
- Blocks
- Planes
- Dies
- Channels
- Packages
- NAND Program Operation
- NAND Erase Operation
- NAND Program / Erase Limitation
- SSD Architecture

---

# MODULE 4 — SSD INTERNAL ARCHITECTURE

## Topics

- Flash Translation Layer (FTL)
- Logical-to-Physical Mapping
- Mapping Tables
- Out-of-Place Writes
- Garbage Collection
- Wear Leveling
- Bad-Block Management
- TRIM / Deallocate
- Over-Provisioning
- Write Amplification
- Read Disturb
- Media Errors
- Thermal Throttling
- Sustained-Write Behavior
- SSD Endurance

## Background Behavior

- Background Garbage Collection
- Wear-Leveling Behavior
- Internal SSD Housekeeping

---

# MODULE 5 — SSD ERASE & LIFECYCLE BEHAVIOR

## Topics

- Why SSD Erase Is Required
- NAND Erase Limitation
- Page Programming
- Block Erase
- FTL Interaction
- Garbage Collection
- TRIM
- Over-Provisioning
- Write Amplification
- Endurance Impact

## Assessment

Explain why SSDs cannot overwrite NAND in the same way as traditional disk storage.

---

# MODULE 6 — ATA

## Topics

- ATA Architecture
- ATA Commands
- ATA Registers

---

# MODULE 7 — SATA

## Topics

- SATA Architecture
- AHCI
- AHCI Registers
- Command List
- Command Header
- Command Table
- PRDT
- FIS
- Native Command Queuing (NCQ)
- SATA Link Initialization
- SATA Error Handling
- SATA Link Behavior
- SATA Commands

## Validation

- Device Discovery
- Command Behavior
- Link Behavior
- Error Handling
- Recovery Behavior

---

# MODULE 8 — SCSI

## Topics

- SCSI Architecture
- Command Descriptor Block (CDB)
- SCSI Commands
- Status
- Sense Data
- Error Interpretation
- SCSI Diagnostics

---

# MODULE 9 — SAS

## Topics

- SAS Architecture
- Initiator
- Target
- SSP
- STP
- SMP
- Expanders
- Dual Porting
- Wide Ports
- SAS Queues
- SAS Device Communication
- SAS Error Behavior

## Enterprise Scenarios

- Device Discovery
- Expander Topology
- Multipath Connectivity
- Path Failure
- SAS Failure Diagnosis

---

# MODULE 10 — PCIe ARCHITECTURE

## Topics

- PCIe Architecture
- Root Complex
- Endpoint
- PCIe Hierarchy
- Bus / Device / Function (BDF)
- Configuration Space
- BAR
- MMIO
- Memory Space
- PCIe Generations
- Lane Width
- Link Speed
- Negotiated Link Width
- Negotiated Link Speed
- Link Training
- Reset Mechanisms
- Power Management
- Hot-Plug Concepts
- Advanced Error Reporting (AER)

---

# MODULE 11 — PCIe VALIDATION ENGINEERING

## Validation Scenarios

- Device Not Enumerating
- Intermittent Enumeration
- Link Downgrade
- PCIe Error Events
- Device Reset Problems
- Device Works on One Platform but Not Another
- PCIe-Visible but NVMe-Inaccessible Device

## Diagnostics

- PCIe Topology Evidence
- BDF Interpretation
- PCIe Kernel Logs
- AER Evidence
- Correlation with NVMe / Controller State

## Assessment

Given an NVMe failure, determine whether evidence points toward:

- PCIe
- Device
- Firmware
- Driver
- OS
- Configuration
- Workload

---

# MODULE 12 — NVMe ARCHITECTURE

## Topics

- NVMe Architecture
- NVMe Subsystem
- Controller
- Namespace
- Admin Commands
- NVM I/O Commands
- Submission Queues
- Completion Queues
- Queue Pairs
- Doorbell Registers
- Interrupts
- PRP
- Scatter-Gather List (SGL)
- Command Lifecycle
- Controller States

---

# MODULE 13 — NVMe DEVICE MANAGEMENT

## Topics

- Identify
- Get Features
- Set Features
- Namespace Management
- Format
- Reset
- Shutdown
- Power States
- Error Handling
- Controller Recovery

---

# MODULE 14 — NVMe VALIDATION ENGINEERING

## Validation

- Device Discovery
- Namespace Validation
- Command Validation
- Queue Behavior
- Reset Recovery
- Controller Failure
- Timeout Handling
- Device Disappearance
- Interoperability
- Feature Validation

## Enterprise Failure Scenarios

- NVMe Device Missing
- Controller Not Initializing
- Namespace Missing
- I/O Timeout
- Controller Reset Failure
- Device Disappearance During Workload
- Firmware / Driver Interaction Failure

---

# MODULE 15 — NVMe OVER FABRICS

## Topics

- NVMe/TCP
- NVMe/RDMA
- FC-NVMe
- Transport Concepts
- Host-to-Storage Communication
- Transport Failure Considerations

---

# SPLIT 1 — MASTER ASSESSMENT

Before moving to Split 2:

- [ ] Explain complete storage write flow
- [ ] Explain complete storage read flow
- [ ] Compare HDD and SSD behavior
- [ ] Explain NAND architecture
- [ ] Explain SSD internals
- [ ] Explain FTL
- [ ] Explain garbage collection
- [ ] Explain wear leveling
- [ ] Explain TRIM / Deallocate
- [ ] Explain write amplification
- [ ] Explain ATA
- [ ] Explain SATA
- [ ] Explain SCSI
- [ ] Explain SAS
- [ ] Explain PCIe architecture
- [ ] Explain PCIe enumeration
- [ ] Explain BAR / MMIO
- [ ] Explain PCIe link training
- [ ] Explain PCIe AER
- [ ] Explain how PCIe relates to NVMe
- [ ] Explain NVMe controller / namespace
- [ ] Explain Submission Queue / Completion Queue
- [ ] Explain NVMe command lifecycle
- [ ] Explain PRP / SGL
- [ ] Explain NVMe reset / recovery
- [ ] Explain NVMe failure scenarios
- [ ] Explain NVMe-oF basics
- [ ] Troubleshoot at least one representative failure scenario
- [ ] Complete Split 1 assessment
```
