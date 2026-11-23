# **Storage – Complete Interview Questions & Answers**

# **Section 1 – Storage Fundamentals**

### **Q1. What is storage, and why do we need storage in servers and enterprise environments?**

**Answer:**

Storage is a component used to store and retrieve data in a computer system or server.

It provides permanent or non-volatile storage for operating systems, applications, databases and user data.

The first storage device was invented by IBM, according to my notes.

**Why do we need storage?**

1. To store operating systems.
2. To store application data.
3. To store databases and files.
4. To maintain business-critical information.
5. To access data whenever required.
6. To provide data availability and protection.

In enterprise environments, storage is important because multiple servers and applications need reliable access to large amounts of data.

**Examples of storage devices:**

- HDD.
- SSD.
- Pendrive.
- Memory card.
- JBOD.
- Storage Array.

### **Q2. What are the different storage capacity units? Explain KB, MB, GB, TB, PB and EB.**

**Answer:**

Storage capacity is measured using different units.

According to my notes, the conversion is:

| Unit | Conversion |
| ---- | ---------- |
| 1 KB | 1024 Bytes |
| 1 MB | 1024 KB    |
| 1 GB | 1024 MB    |
| 1 TB | 1024 GB    |
| 1 PB | 1024 TB    |
| 1 EB | 1024 PB    |

These units are used to measure the capacity of storage devices.

For example:

- A pendrive may have 32 GB capacity.
- An SSD may have 512 GB capacity.
- An enterprise storage array may have several TB or PB of capacity.

*Technical clarification:* These are binary-based conversions. Strictly, the corresponding units are KiB, MiB, GiB, TiB, PiB and EiB. Manufacturers commonly display drive capacities using decimal units.

### **Q3. What is the difference between Primary Storage and Secondary Storage?**

**Answer:**

**Primary Storage:**

Primary storage is the storage directly available to the computer system for its immediate operations.

It includes memory and storage components available within the system.

Examples mentioned in my notes:

- RAM.
- Internal HDD.
- Boot drive.
- Internal storage.

**Secondary Storage:**

Secondary storage is storage connected externally to a laptop or server for additional storage capacity.

Examples:

- External HDD.
- JBOD.
- EBOD.
- Storage Array.

**Difference:**

| Primary Storage                           | Secondary Storage                                       |
| ----------------------------------------- | ------------------------------------------------------- |
| Available within the system               | Connected externally                                    |
| Used for system operations and storage    | Used for additional storage capacity                    |
| Examples include RAM and internal storage | Examples include external drives and storage enclosures |

*Technical clarification:* RAM is technically volatile primary memory, whereas an internal HDD or SSD is secondary/non-volatile storage. The notes group them under primary storage based on physical availability; these are different classifications.

### **Q4. What is the difference between Local Storage and Remote Storage?**

**Answer:**

**Local Storage:**

Local storage refers to storage space available directly within a computer or server or connected locally to it.

Examples:

- Internal HDD.
- Internal SSD.
- DAS.
- Pendrive.
- Locally connected JBOD.

**Remote Storage:**

Remote storage refers to storage space that we can access through a network or external storage infrastructure.

Examples:

- Cloud storage.
- SAN.
- NAS.

**Difference:**

| Local Storage                    | Remote Storage                                            |
| -------------------------------- | --------------------------------------------------------- |
| Available directly to the system | Accessed through a network                                |
| Usually connected locally        | Connected through network infrastructure                  |
| Simple to implement              | Requires network and storage configuration                |
| Generally lower latency          | Performance depends on network and storage infrastructure |
| Example: DAS                     | Example: SAN and NAS                                      |

### **Q5. What are DAS, SAN and NAS? Explain their architecture and differences.**

**Answer:**

There are three major storage topologies:

1. DAS – Direct Attached Storage.
2. SAN – Storage Area Network.
3. NAS – Network Attached Storage.

**1. DAS – Direct Attached Storage**

DAS stands for Direct Attached Storage.

In DAS, we connect storage directly to the server using storage cables or interfaces.

The storage is dedicated to the connected server and is not shared across servers through a storage network by default.

Examples:

- Internal HDD.
- Internal SSD.
- External JBOD.

Architecture:

```
+------------------+
|      Server      |
+------------------+
         |
    SAS/SATA/NVMe
         |
+------------------+
|     Storage      |
+------------------+
```

Advantages:

- Faster local access in suitable configurations.
- Easy to implement.
- Simple maintenance.

Disadvantages:

- No shared storage by default.
- Limited storage sharing.
- No centralized storage infrastructure.

**2. SAN – Storage Area Network**

SAN stands for Storage Area Network.

It connects multiple servers to centralized storage through a dedicated storage network.

SAN supports block-level storage.

Common protocols:

- Fibre Channel.
- iSCSI.
- NVMe-oF.

Architecture:

```
+----------+  +----------+  +----------+
| Server 1 |  | Server 2 |  | Server 3 |
+----------+  +----------+  +----------+
      \             |             /
       \            |            /
        +----------------------+
        |     SAN Switches     |
        +----------------------+
                  |
           +-------------+
           | Storage     |
           | Array       |
           +-------------+
```

Advantages:

- Shared storage.
- Centralized storage management.
- Multipathing.
- High availability.
- Redundancy.
- Supports multiple servers accessing storage.

**3. NAS – Network Attached Storage**

NAS stands for Network Attached Storage.

It is a storage system connected to a network and provides file-level storage to multiple clients.

Common protocols:

- NFS.
- CIFS/SMB.

Architecture:

```
+----------+  +----------+  +----------+
| Server 1 |  | Server 2 |  | Server 3 |
+----------+  +----------+  +----------+
       \           |           /
        +---------------------+
        |    Ethernet Switch  |
        +---------------------+
                   |
             +-----------+
             |    NAS    |
             +-----------+
```

**Difference between DAS, SAN and NAS:**

| Feature      | DAS                     | SAN                                          | NAS                                 |
| ------------ | ----------------------- | -------------------------------------------- | ----------------------------------- |
| Full form    | Direct Attached Storage | Storage Area Network                         | Network Attached Storage            |
| Storage type | Block                   | Block                                        | File                                |
| Connectivity | Direct connection       | Storage network                              | Ethernet network                    |
| Sharing      | Usually dedicated       | Shared across servers                        | Shared across clients               |
| Protocols    | SAS, SATA, NVMe         | FC, iSCSI, NVMe-oF                           | NFS, CIFS/SMB                       |
| Performance  | Generally low latency   | High performance, depending on configuration | Depends on network and NAS workload |
| Complexity   | Simple                  | More complex                                 | Comparatively simple                |

### **Q6. What is the difference between Block-Level Storage and File-Level Storage?**

**Answer:**

**Block-Level Storage:**

In block-level storage, we present raw storage space to a server in the form of logical blocks.

The server can create partitions, filesystems and volumes on that storage.

Examples:

- DAS.
- SAN.

**File-Level Storage:**

In file-level storage, we provide storage through a filesystem over the network.

Users and systems access files and directories instead of directly managing the underlying storage blocks.

Examples:

- NAS.
- NFS.
- CIFS/SMB.

**Difference:**

| Block-Level Storage                         | File-Level Storage                               |
| ------------------------------------------- | ------------------------------------------------ |
| Provides raw storage blocks                 | Provides files and directories                   |
| Filesystem is generally created by the host | Filesystem is managed by the file-storage system |
| Used for databases and VM datastores        | Used for shared files and folders                |
| Examples: DAS and SAN                       | Example: NAS                                     |
| Protocols include iSCSI and FC              | Protocols include NFS and CIFS                   |

# **Section 2 – HDD, SSD and Internal Architecture**

### **Q7. What are the different types of storage devices? Explain HDD, SSD, JBOD and Storage Array.**

**Answer:**

According to my notes, the different types of storage devices are:

1. HDD.
2. SSD.
3. JBOD.
4. Storage Array/EBOD.

**1. HDD – Hard Disk Drive:**

HDD is a mechanical storage device that uses rotating platters to store data.

It uses mechanical components such as platters, spindle, read/write head and actuator.

**2. SSD – Solid State Drive:**

SSD is a storage device that uses flash memory to store data.

It does not have moving mechanical components like HDD.

**3. JBOD – Just a Bunch of Disks:**

JBOD is a storage enclosure that contains multiple drives.

It provides additional storage capacity to a server.

The operating system can discover individual drives when the enclosure and controller expose them as separate devices.

**4. Storage Array:**

A Storage Array is an enterprise storage system that contains multiple drives, controllers or I/O modules and storage management features.

It provides features such as:

- RAID.
- Volumes.
- LUNs.
- Multipathing.
- Snapshots.
- Replication.
- High Availability.

### **Q8. What is HDD? Explain its internal components and working architecture.**

**Answer:**

HDD stands for Hard Disk Drive.

It is a mechanical storage device used to store data on rotating magnetic platters.

It works using mechanical components.

**Main HDD components:**

1. **Platter:** Circular magnetic disk where the actual data is stored.
2. **Spindle:** Motor that rotates the platters.
3. **Read/Write Head:** Used to read data from and write data to the platter.
4. **Actuator Arm:** Moves the read/write head to the required location.
5. **Actuator:** Controls the movement of the actuator arm.

**Working of HDD:**

1. The spindle rotates the platters.
2. The actuator moves the read/write head to the required location.
3. The read/write head accesses the required sectors.
4. Data is read from or written to the magnetic platters.
5. The HDD controller communicates with the host and manages the read/write operations.

**Architecture:**

```
+----------------------+
|        Host          |
+----------------------+
           |
+----------------------+
|     HDD Controller   |
+----------------------+
           |
+----------------------+
|    Actuator Arm      |
|    Read/Write Head   |
+----------------------+
           |
+----------------------+
|   Rotating Platters  |
+----------------------+
```

### **Q9. What are Sectors and Blocks in HDD? How is data stored in an HDD?**

**Answer:**

In HDD, data is stored on magnetic platters.

The platters are divided into tracks and sectors.

**Sector:**

A sector is a small storage unit on a disk.

It is used to store data.

**Block:**

A block is a group of sectors treated as a logical data unit.

The host generally accesses storage through logical blocks.

**Example:**

Suppose a disk has a block size of 4 KB.

The operating system accesses data in logical block units according to the device and filesystem configuration.

**Data storage process:**

1. The host sends a read or write command.
2. The HDD controller processes the command.
3. The actuator moves the read/write head.
4. The head accesses the required disk location.
5. Data is read or written on the platter.

### **Q10. What is SSD? Explain its internal architecture and components such as DRAM, SSD Controller and NAND Flash.**

**Answer:**

SSD stands for Solid State Drive.

It is a storage device that uses NAND Flash memory to store data.

Unlike HDD, SSD does not use rotating platters or mechanical read/write heads.

**Main components of SSD:**

1. DRAM.
2. SSD Controller.
3. NAND Flash Memory.

**1. DRAM:**

DRAM is used as cache memory in SSDs.

It can store metadata and mapping information used by the SSD controller.

**2. SSD Controller:**

The SSD controller manages SSD operations.

It is responsible for:

- Data access.
- Read/write operations.
- NAND communication.
- Wear Leveling.
- Garbage Collection.
- Error Correction.
- Flash Translation Layer.

**3. NAND Flash Memory:**

NAND flash is the non-volatile storage medium used to store user data.

It contains cells used to store information.

**SSD Data Flow:**

```
        HOST
          |
          v
   SSD Controller
          |
          v
       DRAM
       Cache
          |
          v
      NAND Flash
   +--------------+
   |  Channels    |
   |  Dies        |
   |  Blocks      |
   |  Pages       |
   |  Cells       |
   +--------------+
```

**Working process:**

1. Host sends write data to the SSD.
2. SSD controller receives the data.
3. Data may be temporarily stored in DRAM cache, if available and used by the implementation.
4. The controller programs data into NAND Flash memory.
5. Data is stored in NAND cells organized into pages and blocks.

### **Q11. What are the different types of NAND Flash Memory? Explain SLC, MLC, TLC and QLC.**

**Answer:**

There are different NAND Flash memory types based on the number of bits stored in each memory cell.

The major types are:

1. SLC.
2. MLC.
3. TLC.
4. QLC.

**1. SLC – Single-Level Cell:**

SLC stores 1 bit per cell.

Advantages:

- Better performance.
- Higher endurance.
- More reliable compared with higher-bit-per-cell NAND.

Disadvantages:

- Higher cost.
- Lower storage density.

**2. MLC – Multi-Level Cell:**

MLC stores 2 bits per cell.

Advantages:

- Higher capacity compared with SLC.
- Lower cost per bit than SLC.

Disadvantages:

\- Lower endurance and performance compared with SLC.

**3. TLC – Triple-Level Cell:**

TLC stores 3 bits per cell.

Advantages:

- Higher storage density.
- Lower cost compared with SLC and MLC.

Disadvantages:

\- Lower endurance compared with SLC and MLC.

**4. QLC – Quad-Level Cell:**

QLC stores 4 bits per cell.

Advantages:

- Higher storage density.
- Lower cost per bit.

Disadvantages:

\- Lower endurance compared with SLC, MLC and TLC.

| NAND Type | Bits per Cell |
| --------- | ------------- |
| SLC       | 1             |
| MLC       | 2             |
| TLC       | 3             |
| QLC       | 4             |

### **Q12. What is the difference between HDD and SSD?**

**Answer:**

| Feature              | HDD                                  | SSD                                                  |
| -------------------- | ------------------------------------ | ---------------------------------------------------- |
| Full form            | Hard Disk Drive                      | Solid State Drive                                    |
| Storage technology   | Magnetic platters                    | NAND Flash                                           |
| Components           | Mechanical components                | Electronic components                                |
| Read/write mechanism | Mechanical head                      | Flash memory                                         |
| Speed                | Slower                               | Faster                                               |
| Reliability          | Mechanical wear and failure possible | No moving mechanical components                      |
| Cost                 | Generally cheaper per GB             | Generally more expensive per GB                      |
| Noise                | Can produce mechanical noise         | Silent operation                                     |
| Power consumption    | Generally higher                     | Generally lower                                      |
| Form factor          | Commonly 3.5-inch and 2.5-inch       | 2.5-inch, M.2, U.2 and enterprise EDSFF form factors |

**Conclusion:**

HDD is suitable for cost-effective high-capacity storage, whereas SSD provides faster data access and better performance for workloads requiring low latency.

### **Q13. What are the different form factors of SSDs? Explain their common usage.**

**Answer:**

SSD form factors define the physical shape, size and connection interface of the drive.

According to my notes, common SSD form factors include:

1. 2.5-inch.
2. M.2.
3. U.2.
4. U.3.
5. E1.S.
6. E2.S.
7. E3.S.
8. E1.L.
9. E3.L.

**1. 2.5-inch SSD:**

A standard rectangular drive form factor used in servers and storage systems.

**2. M.2:**

A compact form factor commonly used in laptops and smaller systems.

**3. U.2 and U.3:**

Enterprise drive form factors commonly used in servers and storage systems.

**4. EDSFF Form Factors:**

E1.S, E2.S, E3.S, E1.L and E3.L belong to Enterprise and Data Center SSD Form Factor standards.

They are designed for enterprise storage and data-center environments.

*Interview clarification:* Form factor refers to physical design. It should not be confused with the protocol: for example, an M.2 drive can use SATA or PCIe/NVMe depending on the specific device.

### **Q14. What are the important SSD features such as Wear Leveling, Garbage Collection, Write Amplification, ECC, TRIM/UNMAP and Over-Provisioning?**

**Answer:**

SSD controllers manage multiple internal features to improve performance, reliability and endurance.

**1. Wear Leveling:**

Wear Leveling distributes write and erase operations across NAND blocks.

This avoids excessive wear on particular NAND blocks.

**Advantage:** Improves SSD lifespan.

**2. Garbage Collection:**

Garbage Collection is the process of reclaiming NAND blocks.

NAND pages cannot generally be overwritten directly.

The controller identifies valid and invalid pages, moves valid data when required and erases blocks for reuse.

**Advantage:** Makes erased blocks available for future write operations.

**3. Write Amplification:**

Write Amplification is the ratio between the amount of data written to NAND and the amount of data sent by the host.

Formula:

\\[ WA=\frac{\text{Data written to NAND}}{\text{Data written by Host}} \\]

For example:

If the host writes 100 GB and the SSD internally writes 200 GB to NAND:

\\[ WA=\frac{200}{100}=2 \\]

**4. ECC – Error Correction Code:**

ECC is used to detect and correct data errors in NAND Flash memory.

It helps maintain data integrity.

Examples mentioned in my notes:

- XOR.
- BCH.
- Read-Solomon.

**5. TRIM / UNMAP:**

TRIM/UNMAP commands notify the SSD controller about logical blocks that are no longer required by the operating system.

The controller can use this information for internal space management and garbage collection.

**6. Over-Provisioning:**

Over-Provisioning is the reserved storage capacity maintained by the SSD controller for internal operations.

This space is not exposed as normal user capacity.

It can be used for:

- Garbage Collection.
- Internal data movement.
- Block management.
- Performance optimization.

**7. FTL – Flash Translation Layer:**

FTL maps the host's Logical Block Addresses (LBA) to the physical locations in NAND Flash memory.

It manages logical-to-physical mapping and supports SSD operations such as garbage collection and wear leveling.

# **Section 3 – RAID Architecture and Management**

### **Q15. What is RAID? What are the advantages of using RAID?**

**Answer:**

RAID stands for **Redundant Array of Independent Disks**.

RAID is a technology in which we combine multiple physical drives to create a logical storage unit called a RAID Group.

We use RAID to improve storage performance, provide redundancy and protect data against drive failures, depending on the RAID level.

**Advantages of RAID:**

1. **Performance:** RAID 0 and other striped RAID configurations improve performance by distributing data across multiple drives.
2. **Redundancy:** RAID 1, RAID 5 and RAID 6 provide data protection through mirroring or parity.
3. **Fault Tolerance:** Some RAID levels can continue operating even when one or more drives fail.
4. **Capacity Management:** Multiple physical drives can be combined into logical storage.
5. **Availability:** Redundant RAID configurations help maintain data availability during drive failures.

### **Q16. What are the different RAID techniques? Explain Striping, Mirroring and Parity.**

**Answer:**

There are three major RAID techniques.

**1. Striping:**

Striping is the process of distributing data across multiple drives in a RAID Group.

For example, if we have three drives, data can be distributed across all three drives.

```
        Host
         |
    +----+----+
    |    |    |
   D1   D2   D3
   A1   A2   A3
   B1   B2   B3
   C1   C2   C3
```

The main advantage of striping is improved performance.

RAID 0 uses striping.

**2. Mirroring:**

Mirroring means writing the same data to multiple drives.

For example, if we write data to Drive 1, the same data is also written to Drive 2.

```
       Host
         |
      +--+--+
      |     |
     D1    D2
     A1    A1
     B1    B1
     C1    C1
```

The main advantage of mirroring is redundancy.

RAID 1 uses mirroring.

**3. Parity:**

Parity is calculated using the XOR operation.

It is used to reconstruct missing data when a drive fails.

RAID 5 and RAID 6 use parity-based protection.

### **Q17. What is Parity? How do we calculate parity using the XOR operation?**

**Answer:**

Parity is additional information calculated from data stored on drives.

It is used to reconstruct data when a drive fails.

In RAID, parity is commonly calculated using the XOR operation.

**XOR Truth Table:**

| Input A | Input B | Output |
| ------- | ------- | ------ |
| 0       | 0       | 0      |
| 0       | 1       | 1      |
| 1       | 0       | 1      |
| 1       | 1       | 0      |

The XOR operation produces:

- 0 when both bits are the same.
- 1 when both bits are different.

**Example:**

Consider two data blocks:

```
D1 = 1001
D2 = 0101
```

Parity calculation:

```
D1 = 1001
D2 = 0101
     ----
P  = 1100
```

Therefore:

\\[ P = D1 \oplus D2 \\]

If Drive 1 fails, we can reconstruct its data using the remaining data and parity.

\\[ D1 = P \oplus D2 \\]

```
P  = 1100
D2 = 0101
     ----
D1 = 1001
```

This is how XOR parity helps in RAID data reconstruction.

**Types of Parity:**

1. Dedicated Parity: All parity information is stored on a dedicated parity drive.
2. Distributed Parity: Parity information is distributed across multiple drives.

Distributed parity is used in RAID 5 and RAID 6 configurations.

### **Q18. Explain RAID 0 and RAID 1 with architecture, minimum drive requirements, performance, capacity and fault tolerance.**

**Answer:**

**1. RAID 0 – Striping**

RAID 0 follows the striping technique.

Data is distributed across multiple drives.

**Architecture:**

```
           Host
             |
       +-----+-----+
       |     |     |
      D1    D2    D3
      A1    A2    A3
      B1    B2    B3
```

Characteristics:

- Minimum drives: 1 according to the notes; practically RAID 0 is normally configured with at least 2 drives.
- Supports multiple drives.
- No redundancy.
- Fault tolerance: 0.
- Performance: Better than RAID 1 in the notes.
- If one drive fails, the complete RAID 0 array becomes unavailable.

**Capacity formula:**

\\[ \text{RAID 0 Capacity}=N\times S \\]

Where:

- \\(N\\) = Number of drives.
- \\(S\\) = Capacity contributed by each drive.

For equal-size drives:

```
3 drives × 100 GB = 300 GB
```

**2. RAID 1 – Mirroring**

RAID 1 follows the mirroring technique.

The same data is written to two drives.

**Architecture:**

```
           Host
             |
         +---+---+
         |       |
        D1      D2
        A1      A1
        B1      B1
        C1      C1
```

Characteristics:

- Minimum drives: 2.
- Data is mirrored between drives.
- Fault tolerance: 1 drive in a two-drive mirror.
- Provides redundancy.
- Usable capacity: 50% with two equal-capacity drives.
- Write operations must maintain both copies.

**Capacity formula for mirrored pairs:**

\\[ \text{RAID 1 Capacity}=\frac{N}{2}\times S \\]

Example:

```
2 drives × 100 GB
Usable capacity = 100 GB
```

**Difference:**

| RAID 0                             | RAID 1                                            |
| ---------------------------------- | ------------------------------------------------- |
| Striping                           | Mirroring                                         |
| Minimum 2 drives normally          | Minimum 2 drives                                  |
| No redundancy                      | Provides redundancy                               |
| Fault tolerance 0                  | Tolerates one drive failure in a two-drive mirror |
| Higher performance                 | Mirrored protection                               |
| Capacity uses combined drive space | 50% usable capacity with two equal drives         |

### **Q19. Explain RAID 5 and RAID 6 with architecture, minimum drive requirements, performance, capacity and fault tolerance.**

**Answer:**

**1. RAID 5 – Block-Level Striping with Distributed Parity**

RAID 5 follows block-level striping with distributed parity.

Data and parity are distributed across all drives.

**Characteristics:**

- Minimum drives: 3.
- Supports multiple drives, with maximum count depending on controller/vendor.
- Uses distributed parity.
- Fault tolerance: 1 drive failure.
- Provides data redundancy.
- Write performance has parity-calculation overhead.

**Architecture:**

```
        Host
         |
   +-----+-----+-----+
   |     |     |     |
  D1    D2    D3    D4
  A1    B1    P1    C1
  A2    P2    B2    C2
  P3    A3    B3    C3
```

**Capacity formula:**

\\[ \text{RAID 5 Capacity}=(N-1)\times S \\]

Example:

Four drives of 100 GB each:

\\[ (4-1)\times100=300\text{ GB} \\]

**2. RAID 6 – Block-Level Striping with Dual Distributed Parity**

RAID 6 follows block-level striping with two distributed parity calculations.

It uses two parity blocks for each stripe.

**Characteristics:**

- Minimum drives: 4.
- Supports more drives depending on controller/vendor.
- Uses dual distributed parity.
- Fault tolerance: 2 simultaneous drive failures.
- More redundancy than RAID 5.
- Write performance is generally lower than RAID 5 because of additional parity processing.

**Architecture:**

```
         Host
          |
   +------+------+------+------+
   |      |      |      |      |
  D1     D2     D3     D4
  A1     B1     P1     Q1
  A2     P2     Q2     B2
  P3     Q3     A3     B3
```

Here:

- P = First parity.
- Q = Second parity.

**Capacity formula:**

\\[ \text{RAID 6 Capacity}=(N-2)\times S \\]

Example:

Four drives of 100 GB each:

\\[ (4-2)\times100=200\text{ GB} \\]

**Difference:**

| Feature           | RAID 5           | RAID 6                     |
| ----------------- | ---------------- | -------------------------- |
| Minimum drives    | 3                | 4                          |
| Parity            | Single parity    | Dual parity                |
| Fault tolerance   | 1 drive          | 2 drives                   |
| Usable capacity   | (N-1) × S        | (N-2) × S                  |
| Redundancy        | Lower            | Higher                     |
| Write performance | Generally better | Additional parity overhead |

### **Q20. Explain nested RAID levels such as RAID 10, RAID 01, RAID 50 and RAID 60.**

**Answer:**

Nested RAID combines two RAID levels to provide a combination of performance and redundancy.

The nested RAID levels mentioned in my notes are RAID 10, RAID 01, RAID 50 and RAID 60.

**1. RAID 10 – RAID 1 + RAID 0**

RAID 10 combines mirroring and striping.

First, we create mirrored pairs and then stripe data across those pairs.

Characteristics:

- Minimum drives: 4.
- Provides both performance and redundancy.
- Can withstand drive failures provided they do not eliminate both drives in the same mirror pair.
- RAID 10 provides high performance and redundancy.

**2. RAID 01 – RAID 0 + RAID 1**

RAID 01 creates striped RAID sets and then mirrors those sets.

Characteristics:

- Minimum drives: 4.
- Provides striping and mirroring.
- Can tolerate a failure in one mirrored side, but failures in both sides can cause data loss.
- Its fault tolerance characteristics differ from RAID 10.

**3. RAID 50 – RAID 5 + RAID 0**

RAID 50 combines RAID 5 and RAID 0.

Multiple RAID 5 groups are created, and data is striped across these groups.

Characteristics:

- Minimum drives: 6.
- Provides distributed parity.
- Better performance than a single RAID 5 group in many workloads.
- Each RAID 5 subgroup can tolerate one drive failure.

**4. RAID 60 – RAID 6 + RAID 0**

RAID 60 combines RAID 6 and RAID 0.

Multiple RAID 6 groups are created and striped.

Characteristics:

- Minimum drives: 8.
- Provides dual parity within each RAID 6 group.
- Better redundancy than RAID 50.
- Each RAID 6 subgroup can tolerate two drive failures.

### **Q21. Compare different RAID levels based on performance, redundancy and fault tolerance. Which RAID level provides better performance and which provides better redundancy?**

**Answer:**

Different RAID levels provide different combinations of performance, capacity and redundancy.

| RAID Level | Technique                                         | Minimum Drives | Fault Tolerance                 |
| ---------- | ------------------------------------------------- | -------------- | ------------------------------- |
| RAID 0     | Striping                                          | 2 normally     | 0                               |
| RAID 1     | Mirroring                                         | 2              | 1 per two-drive mirror          |
| RAID 3     | Byte-level striping with dedicated parity         | 3              | 1                               |
| RAID 4     | Block-level striping with dedicated parity        | 3              | 1                               |
| RAID 5     | Block-level striping with distributed parity      | 3              | 1                               |
| RAID 6     | Block-level striping with dual distributed parity | 4              | 2                               |
| RAID 10    | RAID 1 + RAID 0                                   | 4              | Depends on failed mirror pairs  |
| RAID 01    | RAID 0 + RAID 1                                   | 4              | Depends on mirrored stripe sets |
| RAID 50    | RAID 5 + RAID 0                                   | 6              | 1 per RAID 5 group              |
| RAID 60    | RAID 6 + RAID 0                                   | 8              | 2 per RAID 6 group              |

**Which RAID level provides better performance?**

RAID 0 generally provides the highest raw performance for suitable workloads because it distributes data across multiple drives without parity calculation or mirroring overhead.

RAID 10 is often preferred when both high performance and redundancy are required.

**Which RAID level provides better redundancy?**

RAID 6 provides greater drive-failure tolerance than RAID 5 because it can tolerate two simultaneous drive failures.

RAID 60 also provides dual-parity protection within each RAID 6 subgroup.

**Interview conclusion:**

- RAID 0 – Performance without redundancy.
- RAID 1 – Mirroring and redundancy.
- RAID 5 – Single-drive fault tolerance.
- RAID 6 – Two-drive fault tolerance.
- RAID 10 – Performance with mirroring-based redundancy.

### **Q22. How do you calculate the total available RAID capacity when the connected drives have different capacities? Explain with an example using 500 GB, 200 GB and 1 TB drives.**

**Answer:**

When drives have different capacities, we generally calculate RAID capacity using the smallest participating drive capacity for traditional RAID layouts.

Given:

```
Drive 1 = 500 GB
Drive 2 = 200 GB
Drive 3 = 1 TB = 1000 GB
```

The smallest drive capacity is 200 GB.

**1. RAID 0:**

Formula:

\\[ \text{Capacity}=N\times S \\]

Where:

- N = 3 drives.
- S = 200 GB.

\\[ 3\times200=600\text{ GB} \\]

Therefore, usable capacity is approximately 600 GB when the array uses equal-sized extents from each drive.

**2. RAID 5:**

Formula:

\\[ \text{Capacity}=(N-1)\times S \\]

\\[ =(3-1)\times200 \\]

\\[ =400\text{ GB} \\]

Therefore, usable capacity is approximately 400 GB.

| RAID Level | Usable Capacity |
| ---------- | --------------- |
| RAID 0     | 600 GB          |
| RAID 5     | 400 GB          |

The remaining capacity on the larger drives may be unused in that RAID group.

### **Q23. What are the different RAID states? Explain Initialization, Online, Degraded, Offline and Rebuilding/Reconstruction.**

**Answer:**

According to my notes, RAID has five major states.

**1. Initialization:**

When we create a RAID Group, the state initially goes to Initialization.

During initialization, the controller prepares the physical drives and logical RAID structure.

Depending on RAID type and controller, read/write availability may be limited or affected during initialization.

**2. Online:**

After initialization is completed, the RAID Group enters the Online state.

In this state, we can perform normal read and write operations.

**3. Degraded:**

When a drive fails within the fault-tolerance limit of the RAID level, the RAID Group enters the Degraded state.

The RAID Group can continue read and write operations because the controller uses remaining data and parity or mirrored copies.

Examples:

- One drive failure in RAID 5.
- One drive failure in RAID 6.

**4. Offline:**

If the number of failed drives exceeds the RAID level's fault-tolerance limit, the RAID Group may enter the Offline state.

Normal access to the RAID Group becomes unavailable.

Examples:

- One failed drive in RAID 0.
- Two failed drives in RAID 5.

**5. Rebuilding/Reconstruction:**

After replacing a failed drive with a working drive, the controller starts rebuilding the RAID Group.

It reconstructs missing data using the remaining data and parity or mirrored data.

After successful rebuilding, the RAID Group returns to a normal protected state.

### **Q24. What happens when a drive fails in a RAID group? Can we perform read and write operations in degraded states?**

**Answer:**

When a drive fails in a RAID Group, the effect depends on the RAID level.

**Example 1 – RAID 5:**

RAID 5 can tolerate one drive failure.

When one drive fails:

1. The controller identifies the failed drive.
2. RAID Group enters Degraded state.
3. The controller reconstructs missing data using parity and remaining data.
4. Read and write operations can continue.
5. Performance may decrease because additional calculations are required.

**Example 2 – RAID 6:**

RAID 6 can tolerate two drive failures.

It can continue operating after two drive failures, provided they are within the supported fault tolerance.

**Example 3 – RAID 0:**

RAID 0 has no redundancy.

If any drive fails, the complete RAID Group becomes unavailable.

**Can we run IOPS in degraded state?**

Yes. In RAID configurations that remain operational within their fault-tolerance limit, we can continue running read and write workloads and measure IOPS.

However, performance may decrease because the controller has to reconstruct or calculate missing data.

### **Q25. What is RAID Rebuilding? How does it work, and why does performance decrease during rebuilding?**

**Answer:**

RAID rebuilding is the process of reconstructing missing data onto a replacement drive after a drive failure.

**Working process:**

1. The controller detects a failed drive.
2. The RAID Group enters Degraded state.
3. We replace the failed drive with a suitable working drive.
4. The controller starts the rebuilding process.
5. It reads the remaining data and parity information.
6. It reconstructs the missing data.
7. It writes the reconstructed data to the replacement drive.
8. After completion, the RAID Group returns to its normal protected state.

**Why does performance decrease?**

During rebuilding, the controller performs additional operations:

- Reads data from the remaining drives.
- Calculates missing data.
- Reads and writes additional blocks.
- Handles normal host I/O simultaneously.

This creates additional workload on the drives and controller.

Therefore, performance may decrease during rebuilding.

**Validation approach:**

As a storage tester, I would:

1. Create a RAID Group.
2. Run a baseline performance test.
3. Remove or fail one drive.
4. Verify the Degraded state.
5. Run the workload again.
6. Replace the failed drive.
7. Monitor rebuild progress.
8. Compare performance during rebuilding and after rebuilding.
9. Verify that the RAID Group returns to a healthy state.

### **Q26. What is a Hot Spare? Explain Local Hot Spare and Global Hot Spare.**

**Answer:**

A Hot Spare is a spare drive assigned to a RAID environment.

When a drive fails, the spare drive can automatically become part of the RAID rebuild process.

The controller uses it as a replacement destination for rebuilding missing data.

**Types of Hot Spare:**

**1. Local Hot Spare:**

A Local Hot Spare is assigned to a particular RAID Group.

It is intended to protect that specific RAID Group.

**2. Global Hot Spare:**

A Global Hot Spare is assigned to a group of eligible RAID Groups.

It can be used by any compatible RAID Group when a drive failure occurs.

**Difference:**

| Local Hot Spare                   | Global Hot Spare                                |
| --------------------------------- | ----------------------------------------------- |
| Assigned to a specific RAID Group | Assigned for use across eligible RAID Groups    |
| Limited to that group             | Can protect multiple groups                     |
| Used for a specific RAID Group    | Used by an eligible group when a failure occurs |

**Example:**

Suppose we have three RAID Groups.

If we assign one local hot spare to each RAID Group, each group has its own spare.

If we assign a global hot spare, that spare can be used by an eligible RAID Group when a drive failure occurs.

### **Q27. What is Consistency Check in RAID? Why do we perform it?**

**Answer:**

Consistency Check is a background RAID controller operation used to verify data and parity consistency within a RAID Group.

It helps identify parity inconsistencies and data inconsistencies.

**Why do we perform Consistency Check?**

1. To verify RAID data consistency.
2. To verify parity consistency.
3. To identify inconsistencies within the RAID Group.
4. To maintain RAID data integrity.

**Types of Consistency Check:**

1. Verify Only.
2. Verify and Fix.

**1. Verify Only:**

The controller checks RAID consistency and reports detected inconsistencies without repairing them.

**2. Verify and Fix:**

The controller checks the RAID Group and attempts to correct inconsistencies.

**Tools mentioned in my notes:**

- StorCLI.
- Gen10 management tools.
- MegaCLI.

### **Q28. What are Patrol Read and ECC? How do they help in identifying and correcting storage errors?**

**Answer:**

**1. Patrol Read:**

Patrol Read is a background operation performed by a RAID controller.

It scans physical drives to identify weak or problematic sectors and media errors.

It helps detect drive problems before they affect normal data access.

**Working:**

1. RAID controller scans sectors on physical drives.
2. It identifies weak or problematic sectors.
3. When supported and possible, it attempts to recover or remap affected data.
4. It reports drive-related errors.

**2. ECC – Error Correction Code:**

ECC is used to detect and correct errors in stored data.

It helps ensure that data remains accurate and reliable.

**Examples:**

- XOR.
- BCH.
- Reed-Solomon.

**Difference:**

| Patrol Read                                  | ECC                                      |
| -------------------------------------------- | ---------------------------------------- |
| RAID controller background operation         | Error-detection and correction technique |
| Scans physical drives                        | Detects and corrects errors in data      |
| Helps identify weak sectors and media errors | Helps maintain data integrity            |

# **Section 4 – Storage Performance Fundamentals**

### **Q29. What are Block Size, Queue Depth, IOPS, Throughput and Latency?**

**Answer:**

These are important storage performance parameters.

**1. Block Size:**

Block size is the amount of data transferred in a single I/O operation.

It is the storage space or data unit that the system reads or writes.

Examples:

- 4 KB.
- 8 KB.
- 64 KB.

**2. Queue Depth:**

Queue depth is the number of outstanding I/O commands that a storage controller or HBA can hold at a time.

It is measured as a number of commands.

Higher queue depth allows more I/O commands to be outstanding simultaneously, subject to device and workload limitations.

**3. IOPS – Input/Output Operations Per Second:**

IOPS indicates how many read/write operations a storage device can perform in one second.

It is measured in numbers.

Higher IOPS generally indicates better performance for the workload being measured.

**4. Throughput:**

Throughput is the amount of data transferred between the host and storage device per unit of time.

It is commonly measured in MB/s or GB/s.

Higher throughput generally indicates better performance for bandwidth-oriented workloads.

**5. Latency:**

Latency is the time taken by an I/O command to complete.

It is measured in milliseconds or microseconds.

Lower latency indicates faster response time.

### **Q30. What is the difference between Sequential I/O and Random I/O?**

**Answer:**

There are two major types of I/O operations.

**1. Sequential I/O:**

Sequential I/O is the process of reading or writing data in consecutive blocks.

For example, reading a large file from beginning to end.

It is generally used to evaluate throughput.

**Example:**

```
Block 1 → Block 2 → Block 3 → Block 4
```

**2. Random I/O:**

Random I/O is the process of reading or writing data at different, non-consecutive block locations.

For example, reading database records from different locations.

It is commonly used to evaluate IOPS and latency.

**Example:**

```
Block 10 → Block 2 → Block 25 → Block 7
```

| Sequential I/O                       | Random I/O                                     |
| ------------------------------------ | ---------------------------------------------- |
| Consecutive block access             | Non-consecutive block access                   |
| Generally used to measure throughput | Commonly used to measure IOPS and latency      |
| Suitable for large data transfers    | Suitable for workloads with scattered accesses |

### **Q31. What are the factors that affect storage performance?**

**Answer:**

According to my notes, the main factors affecting storage performance are:

1. **Block Size:** Different block sizes affect the amount of data transferred per I/O.
2. **Type of I/O:** Sequential and random operations have different performance characteristics.
3. **Queue Depth:** Controls the number of outstanding I/O requests.
4. **Drive Type:** HDD, SSD, SAS, SATA and NVMe have different performance characteristics.
5. **RAID Level:** Different RAID levels introduce different overheads and performance characteristics.
6. **Controller Performance:** The storage controller can become a bottleneck.
7. **Host Resources:** CPU and memory can affect I/O processing.
8. **Workload:** Read/write ratio and workload patterns influence performance.

### **Q32. What is the relationship between Block Size, Queue Depth, IOPS, Throughput and Latency?**

**Answer:**

These parameters are interconnected.

**1. Block Size and Throughput:**

Larger block sizes generally transfer more data per I/O operation.

For a given IOPS rate, larger block sizes can produce higher throughput.

**2. Queue Depth and IOPS:**

Increasing queue depth can increase IOPS until the device or system reaches its saturation point.

Beyond saturation, additional queue depth may increase latency without improving throughput.

**3. IOPS and Throughput:**

A simplified relationship is:

\\[ \text{Throughput}=\text{IOPS}\times\text{Block Size} \\]

For example:

If a storage device performs 10,000 IOPS using 4 KB blocks:

\\[ 10000\times4\text{ KB}=40000\text{ KB/s} \\]

Approximately 40 MB/s using decimal measurement conventions.

**4. Latency and Queue Depth:**

As queue depth increases, the number of outstanding requests increases.

If the storage system becomes saturated, latency may increase.

**Interview conclusion:**

- Higher IOPS generally means more operations per second.
- Higher throughput means more data transferred per second.
- Lower latency means faster response.
- Block size and queue depth strongly influence storage performance.

### **Q33. What are the different tools used for storage performance testing? Explain FIO, IOMeter and their testing parameters.**

**Answer:**

There are different tools used for storage performance testing.

According to my notes:

| Environment | Performance Tools        |
| ----------- | ------------------------ |
| Windows     | IOMeter, CrystalDiskMark |
| Linux       | FIO, Vdbench, Iozone     |
| ESXi        | HCI Bench                |

**1. FIO – Flexible I/O Tester:**

FIO is a storage performance testing tool used to generate read/write workloads.

We can execute FIO in Linux to test:

- SSDs.
- HDDs.
- RAID Volumes.
- Storage devices.

**Important FIO parameters:**

| Parameter    | Purpose                  |
| ------------ | ------------------------ |
| `--name`     | Test job name            |
| `--filename` | Target file or device    |
| `--rw`       | Read/write workload type |
| `--bs`       | Block size               |
| `--iodepth`  | I/O queue depth          |
| `--runtime`  | Test duration            |
| `--numjobs`  | Number of jobs           |
| `--ioengine` | I/O engine               |

**Example FIO command:**

```
fio --name=sample_test \
--filename=/mnt/testfile \
--rw=randwrite \
--bs=4k \
--iodepth=16 \
--runtime=60 \
--numjobs=1 \
--ioengine=libaio \
--direct=1
```

This example generates a random write workload with 4 KB block size for 60 seconds.

**2. IOMeter:**

IOMeter is a performance testing tool commonly used in Windows environments.

It allows us to generate different types of storage I/O workloads.

**Steps to execute IOMeter:**

1. Open IOMeter.
2. Select the disk target.
3. Configure the specifications or select an existing test pattern.
4. Add the required I/O pattern.
5. Configure runtime and test description.
6. Start the test.
7. Collect performance results.

**Metrics collected:**

- Total IOPS.
- Total throughput.
- Average response time.
- CPU utilization.
- I/O error count.

**Why do we perform performance testing?**

1. To benchmark the storage device.
2. To verify drive stability and reliability.
3. To compare actual performance with vendor specifications.
4. To identify performance bottlenecks.
5. To validate storage performance under different workloads.

# **Section 5 – Storage Hardware and Architecture**

### **Q34. What is HBA? What is its role in connecting a server with storage?**

**Answer:**

HBA stands for Host Bus Adapter.

It is a hardware adapter used to establish communication between a server and external storage devices.

We normally install an HBA in a PCIe slot on the server motherboard.

**Main responsibilities:**

1. Establish communication between server and storage.
2. Send storage commands from the host to the target.
3. Receive responses and data from storage.
4. Connect to storage through supported interfaces such as SAS and Fibre Channel.

**Architecture:**

```
+----------------+
|     Server     |
+----------------+
        |
      PCIe
        |
+----------------+
|      HBA       |
+----------------+
        |
      Cable
        |
+----------------+
| Storage Array  |
+----------------+
```

### **Q35. What is the difference between HBA and RAID Controller?**

**Answer:**

Both HBA and RAID Controller are used to establish communication between a server and storage devices.

However, they have different purposes.

**HBA:**

An HBA is used to connect the server with storage and provide access to connected drives.

**RAID Controller:**

A RAID Controller also connects the server to storage, but it provides RAID functionality by combining multiple physical drives into logical RAID groups and virtual drives.

**Difference:**

| HBA                                      | RAID Controller                                   |
| ---------------------------------------- | ------------------------------------------------- |
| Connects server and storage              | Connects server and storage                       |
| Provides access to drives                | Provides access to drives with RAID functionality |
| Normally exposes individual drives       | Can create RAID groups and virtual drives         |
| Used when host-side RAID is not required | Used when hardware RAID is required               |

### **Q36. What is PCI and PCIe? Explain the different PCIe generations, link speeds and lane configurations.**

**Answer:**

**PCI:**

PCI stands for Peripheral Component Interconnect.

It is used to connect peripheral devices to the CPU or system through the motherboard.

Examples:

- Network Cards.
- Storage Controllers.
- Sound Cards.
- Other peripheral devices.

**PCI-X:**

PCI-X is an extended version of conventional PCI.

It provides higher bandwidth compared with traditional PCI and was used in older server environments.

**PCIe:**

PCIe stands for Peripheral Component Interconnect Express.

It is a high-speed serial communication interface used to connect devices to the CPU or platform.

Examples:

- NVMe SSD.
- HBA.
- RAID Controller.
- Network Card.
- GPU.

**Difference between PCI-X and PCIe:**

| PCI-X                     | PCIe                   |
| ------------------------- | ---------------------- |
| Parallel bus architecture | Serial architecture    |
| Older technology          | Modern technology      |
| Limited scalability       | Highly scalable        |
| Used in legacy servers    | Used in modern servers |

**PCIe Lane:**

A PCIe lane contains two differential signal pairs:

- One pair for transmitting data.
- One pair for receiving data.

Therefore, PCIe supports full-duplex communication.

Common lane configurations:

- x1.
- x4.
- x8.
- x16.

For example:

- x1 is commonly used by network or small peripheral cards.
- x4 is commonly used by NVMe SSDs.
- x8 can be used by HBAs and RAID controllers.
- x16 is commonly used by GPUs.

**PCIe Generations:**

According to my notes, the different generations are:

| Generation | Link Speed | Approx. Bandwidth per Lane, Each Direction |
| ---------- | ---------- | ------------------------------------------ |
| PCIe Gen 1 | 2.5 GT/s   | 250 MB/s                                   |
| PCIe Gen 2 | 5 GT/s     | 500 MB/s                                   |
| PCIe Gen 3 | 8 GT/s     | 985 MB/s                                   |
| PCIe Gen 4 | 16 GT/s    | 1.97 GB/s                                  |
| PCIe Gen 5 | 32 GT/s    | 3.94 GB/s                                  |
| PCIe Gen 6 | 64 GT/s    | 7.88 GB/s                                  |

**Important:** These are approximate per-lane bandwidths after encoding overhead and are not the total bandwidth of an x4 or x16 link.

For example, PCIe Gen 5 x4 provides approximately four times the per-lane bandwidth.

### **Q37. What are Backplane and Expander? Explain their architecture and uses.**

**Answer:**

**Backplane:**

A backplane is a hardware board that connects drive slots to the storage controller or HBA.

It allows us to insert multiple drives into a server or storage enclosure without connecting a separate cable from every drive directly to the controller.

**Uses of Backplane:**

1. Connects multiple drives to the HBA or RAID Controller.
2. Provides power and signal connectivity.
3. Supports drive insertion and removal in supported hot-swap configurations.
4. Simplifies server storage connectivity.

**Expander:**

A SAS Expander is a component that works like a switch in the SAS storage architecture.

It allows us to connect multiple SAS devices through fewer upstream connections.

It expands the number of available drive connections.

**Types of Expanders:**

1. Fan-out Expander.
2. Edge Expander.

**Architecture:**

```
+------------------+
|      Server      |
+------------------+
         |
        HBA
         |
     Backplane
         |
      Expander
      /   |   \
    D1    D2   D3
```

**Difference:**

| Backplane                                    | Expander                                     |
| -------------------------------------------- | -------------------------------------------- |
| Connects drive slots to storage connectivity | Expands connectivity to multiple SAS devices |
| Provides physical connectivity               | Provides SAS device connectivity and routing |
| Used in server and storage enclosures        | Used in SAS storage systems and enclosures   |

### **Q38. What is the difference between JBOD and Storage Array?**

**Answer:**

**JBOD:**

JBOD stands for Just a Bunch of Disks.

It is a storage enclosure containing multiple drives.

JBOD is not necessarily an intelligent storage device.

It provides additional storage capacity to the server.

The drives can be exposed individually to the operating system through the connected controller.

**Storage Array:**

A Storage Array is an enterprise storage system containing multiple drives and intelligent storage components.

It includes:

- Controllers or I/O modules.
- Drives.
- Backplane.
- CPU.
- Memory.
- BMC.
- CPLD.
- Power Supply Units.
- Expanders.

It provides advanced features such as RAID, volumes, LUNs, multipathing, snapshots and replication.

**Difference:**

| JBOD                                      | Storage Array                              |
| ----------------------------------------- | ------------------------------------------ |
| Just a Bunch of Disks                     | Intelligent storage system                 |
| Mainly provides additional drive capacity | Provides storage management features       |
| Usually exposes individual drives         | Can create RAID groups and logical volumes |
| Requires a suitable HBA or controller     | Has internal storage controllers           |
| Limited storage management features       | Provides advanced storage functionality    |
| Comparatively simple                      | More complex                               |

### **Q39. Explain the architecture of an Enterprise Storage Array and its major components.**

**Answer:**

An Enterprise Storage Array is a storage system used to provide centralized storage to multiple servers.

It contains multiple hardware and software components.

**Main components:**

**1. Drives:**

The storage array contains multiple HDDs or SSDs to store user data.

**2. Backplane:**

The backplane connects the drives to the storage controllers or expanders.

**3. I/O Modules / Controllers:**

Controllers manage communication between host servers and storage drives.

They handle storage operations, data transfer and RAID functionality.

**4. CPU and RAM:**

CPU and RAM are used for storage-system processing, cache and management operations.

**5. BMC:**

The Baseboard Management Controller provides hardware management and monitoring functionality.

**6. CPLD:**

Complex Programmable Logic Device is used for hardware control and management functions.

**7. Expander:**

The expander connects multiple drives to the storage controller through SAS connectivity.

**8. PSU:**

Power Supply Units provide electrical power to storage components.

**9. Network Ports:**

Network interfaces provide host connectivity and storage communication.

**Architecture:**

```
            +-------------------+
            |    Host Servers   |
            +-------------------+
                     |
              FC / iSCSI / NVMe
                     |
          +----------------------+
          |   Storage Controller |
          |       Node A         |
          +----------------------+
                     |
             +---------------+
             |   Backplane   |
             +---------------+
                     |
          +----------------------+
          |    HDDs / SSDs       |
          +----------------------+
                     |
              Controller Node B
                     |
          +----------------------+
          |   Redundant Paths    |
          +----------------------+
```

**Important Storage Array Features:**

1. Multipathing.
2. HA clustering.
3. Failover and failback.
4. Remote management.
5. RAID and volume creation.
6. Snapshots.
7. Remote Copy.
8. Replication.
9. Deduplication.
10. LUN Mapping.
11. LUN Masking.
12. Zoning.

### **Q40. What are Active-Active and Active-Passive storage controllers? Explain their working and differences.**

**Answer:**

There are two common storage controller configurations:

1. Active-Active.
2. Active-Passive.

**1. Active-Active Configuration:**

In Active-Active configuration, both storage controller nodes are active and can process I/O operations.

Both controllers can handle host requests simultaneously, depending on the array architecture and volume ownership.

**Working:**

1. Both controllers are active.
2. Host I/O requests can be processed through both controllers.
3. Workloads can be distributed across available paths.
4. If one controller fails, the other controller continues serving accessible storage.

**Advantages:**

- High throughput.
- Better resource utilization.
- Multiple active paths.

**Disadvantage:**

\- More complex hardware and failure management.

**2. Active-Passive Configuration:**

In Active-Passive configuration, one controller acts as the active controller and the other remains in standby or passive mode for the relevant resources.

**Working:**

1. The Active controller handles I/O operations.
2. The Passive controller remains available for failover.
3. If the Active controller fails, the Passive controller takes over.
4. When the original controller returns, the system may perform failback depending on the configuration.

**Advantages:**

- Provides controller redundancy.
- Supports failover.
- Helps maintain storage availability.

**Difference:**

| Active-Active                                       | Active-Passive                                                                  |
| --------------------------------------------------- | ------------------------------------------------------------------------------- |
| Both controllers process I/O                        | One controller handles I/O and the other is standby for the protected resources |
| Higher potential throughput                         | Workload normally uses one active controller                                    |
| Both controllers are active                         | One active and one passive                                                      |
| Supports controller failover                        | Supports controller failover                                                    |
| Both controllers can provide service simultaneously | Passive controller takes over after failure                                     |

# **Section 6 – Storage Protocols**

### **Q41. What is SCSI? Explain CDB (Command Descriptor Block) and list commonly used SCSI commands.**

**Answer:**

SCSI stands for Small Computer System Interface.

It is a storage communication protocol used between the host and target storage devices.

SCSI uses commands to perform operations such as reading, writing, querying device information and managing storage devices.

**CDB – Command Descriptor Block:**

A CDB is the command structure used to communicate with a SCSI target.

It contains information such as:

- Operation code.
- Logical Block Address.
- Transfer length.
- Command-specific information.
- Control fields.

The host sends the CDB to the target, and the target executes the requested operation.

**Common SCSI Commands:**

| Command                    | Purpose                                                     |
| -------------------------- | ----------------------------------------------------------- |
| READ                       | Reads data from the drive                                   |
| WRITE                      | Writes data to the drive                                    |
| INQUIRY                    | Retrieves device information                                |
| TEST UNIT READY            | Checks whether the device is ready                          |
| READ CAPACITY              | Retrieves device capacity                                   |
| FORMAT UNIT                | Formats the storage device                                  |
| UNMAP                      | Notifies storage that logical blocks are no longer required |
| SANITIZE                   | Performs supported data sanitization                        |
| SEND DIAGNOSTIC            | Sends diagnostic requests                                   |
| RECEIVE DIAGNOSTIC RESULTS | Retrieves diagnostic information                            |
| REQUEST SENSE              | Retrieves error and status information                      |

### **Q42. What are Write Buffer and Request Sense commands? What are their purposes?**

**Answer:**

**1. WRITE BUFFER:**

WRITE BUFFER is a SCSI command used to transfer data to a device's buffer.

One important use is firmware download to supported storage devices.

We use it as part of firmware update procedures when the drive supports this operation.

**2. READ BUFFER:**

READ BUFFER is used to retrieve buffer data or supported device information.

It can be used to read firmware-related information depending on the device implementation.

**3. REQUEST SENSE:**

REQUEST SENSE is used to retrieve sense information from a SCSI device.

When a SCSI command fails, the host can issue REQUEST SENSE to understand the failure condition.

**Difference:**

| Command       | Purpose                                                            |
| ------------- | ------------------------------------------------------------------ |
| WRITE BUFFER  | Transfers data to device buffer; can be used for firmware download |
| READ BUFFER   | Reads supported buffer information                                 |
| REQUEST SENSE | Retrieves error and status information                             |

### **Q43. What is ATA? Explain ATA commands and their usage.**

**Answer:**

ATA stands for Advanced Technology Attachment.

It is a storage interface standard used to connect storage devices to computers.

ATA is also associated with IDE (Integrated Drive Electronics).

It supports commands used to control storage devices and perform read/write operations.

**ATA Commands:**

Common commands include:

1. READ SECTOR.
2. WRITE SECTOR.
3. IDENTIFY DEVICE.
4. FLUSH CACHE.
5. SMART commands.
6. DEVICE RESET.
7. SECURITY ERASE.

**Purpose of ATA Commands:**

- Read data from the drive.
- Write data to the drive.
- Identify drive information.
- Flush cached data to non-volatile media.
- Retrieve health information.
- Reset the device.
- Perform supported security erase operations.

### **Q44. Explain SATA architecture, including its layers and data transfer process.**

**Answer:**

SATA stands for Serial Advanced Technology Attachment.

It is a serial storage interface used to connect storage devices such as HDDs and SSDs to a host.

According to my notes:

- SATA supports up to 6 Gbps.
- It is a serial communication protocol.
- It supports a single command queue in the NCQ mechanism, with up to 32 commands.

**SATA Architecture:**

SATA contains the following layers:

1. Application Layer.
2. Transport Layer.
3. Link Layer.
4. Physical Layer.

**1. Application Layer:**

Receives commands from the host and sends them to the transport layer.

**2. Transport Layer:**

Constructs the required frames and transfers them to the link layer.

**3. Link Layer:**

Handles frame integrity and encoding/decoding functions.

**4. Physical Layer:**

Establishes the physical connection between the host and the SATA device.

**Important SATA frame information:**

- SOF – Start of Frame.
- EOF – End of Frame.
- CRC – Cyclic Redundancy Check.

**Data Transfer Process:**

```
        Host
          |
   Application Layer
          |
   Transport Layer
          |
      Link Layer
          |
    Physical Layer
          |
      SATA Cable
          |
   Physical Layer
          |
      Link Layer
          |
   Transport Layer
          |
  Application Layer
          |
     SATA Device
```

The host sends a command through the application layer. The command travels through the transport and link layers and then through the physical interface to the target storage device.

The target processes the command and returns the response.

### **Q45. Explain SAS architecture, including its layers, ports, PHYs and expanders.**

**Answer:**

SAS stands for Serial Attached SCSI.

It is a storage communication protocol used mainly in enterprise servers and storage systems.

It supports high-performance communication between hosts and storage devices.

**SAS Architecture:**

SAS contains the following layers:

1. Application Layer.
2. Transport Layer.
3. Port Layer.
4. Link Layer.
5. PHY Layer.
6. Physical Layer.

**1. Application Layer:**

Receives commands from the host and processes the appropriate protocol.

Three important protocols are:

- SSP – Serial SCSI Protocol.
- STP – Serial ATA Tunneling Protocol.
- SMP – Serial Management Protocol.

**2. Transport Layer:**

Receives commands from the application layer and constructs the required frames.

**3. Port Layer:**

Identifies the destination port to which data must be transferred.

**4. Link Layer:**

Manages link communication, primitives and frame handling.

**5. PHY Layer:**

Performs functions such as encoding, decoding and link-level communication.

**6. Physical Layer:**

Provides the actual physical connection.

**Important SAS Components:**

- Initiator.
- Target.
- SAS PHY.
- Narrow Port.
- Wide Port.
- Expander.
- Backplane.

**SAS Ports:**

A Narrow Port contains one PHY.

A Wide Port contains multiple PHYs grouped into one port.

**Expanders:**

Expanders allow multiple SAS devices to connect through fewer upstream connections.

There are two types:

1. Fan-out Expander.
2. Edge Expander.

**Architecture:**

```
       Host / Initiator
              |
             HBA
              |
           Expander
          /   |   \
        HDD  SSD  SSD
        Targets
```

### **Q46. What is the difference between SAS and SATA?**

**Answer:**

SAS stands for Serial Attached SCSI.

SATA stands for Serial Advanced Technology Attachment.

Both are storage interfaces, but they are used in different environments.

| Feature                 | SAS                               | SATA                                                      |
| ----------------------- | --------------------------------- | --------------------------------------------------------- |
| Full form               | Serial Attached SCSI              | Serial Advanced Technology Attachment                     |
| Main usage              | Enterprise storage                | Desktop and cost-effective storage                        |
| Command set             | SCSI                              | ATA                                                       |
| Standard speed in notes | Up to 12 Gbps                     | Up to 6 Gbps                                              |
| Port architecture       | Supports dual-port devices        | Usually single-port                                       |
| Expanders               | Supports SAS expanders            | Does not directly use SAS expanders                       |
| Queue support           | SCSI command queueing             | NCQ, up to 32 commands                                    |
| Drive identification    | WWN                               | ATA device identification/serial information              |
| Reliability             | Designed for enterprise workloads | Commonly used in desktop and general-purpose environments |
| Cable length in notes   | Up to 10 metres                   | Approximately 1 metre                                     |

**SAS Advantages:**

- Higher performance in supported configurations.
- Dual-port connectivity.
- Support for multiple devices through expanders.
- Enterprise-oriented features.

**SATA Advantages:**

- Lower cost.
- Suitable for desktop and general-purpose storage.
- Simpler connectivity.

### **Q47. What are SAS Primitives? Explain commonly used primitives.**

**Answer:**

SAS primitives are low-level signals or ordered control sequences used to establish and manage communication between SAS devices.

They help identify device state and manage link operations.

Common SAS primitives mentioned in my notes include:

| Primitive | Purpose                      |
| --------- | ---------------------------- |
| SOF       | Start of Frame               |
| EOF       | End of Frame                 |
| CRC       | Cyclic Redundancy Check      |
| COMINIT   | Initialization signal        |
| ALIGN     | Alignment primitive          |
| IDLE      | Idle communication state     |
| COMWAKE   | Wake-up signal               |
| COMSAS    | SAS communication sequence   |
| XRDY      | Transmit-ready primitive     |
| RRDY      | Receiver-ready primitive     |
| COMRESET  | Reset communication sequence |

These primitives help establish and maintain communication between SAS initiators and targets.

### **Q48. What is the difference between iSCSI and Fibre Channel (FC)?**

**Answer:**

**iSCSI:**

iSCSI stands for Internet Small Computer System Interface.

It is a storage protocol that carries SCSI commands over TCP/IP networks.

It is used to connect servers to remote block storage using Ethernet infrastructure.

**Fibre Channel:**

FC stands for Fibre Channel.

It is a high-speed storage networking technology used to connect servers and storage arrays through a dedicated SAN fabric.

It supports SCSI-based storage communication and other storage protocols.

**Difference:**

| iSCSI                                                          | Fibre Channel                                  |
| -------------------------------------------------------------- | ---------------------------------------------- |
| Runs over TCP/IP                                               | Runs over Fibre Channel fabric                 |
| Uses Ethernet infrastructure                                   | Uses FC switches and FC HBAs                   |
| Uses IP addresses for connectivity                             | Uses WWNs for identification                   |
| Generally lower infrastructure cost                            | Generally higher dedicated infrastructure cost |
| Storage traffic shares Ethernet infrastructure unless isolated | Dedicated storage fabric is commonly used      |
| Uses iSCSI Initiator and Target                                | Uses FC HBA and FC Target Ports                |

### **Q49. Explain Fibre Channel architecture, FC layers and different FC port types.**

**Answer:**

Fibre Channel is a high-speed storage networking technology used to connect servers with storage arrays.

It is commonly used in SAN environments.

**FC Architecture:**

```
+-------------+
|   Server    |
+-------------+
      |
    FC HBA
      |
      v
+-------------+
| FC Switch   |
+-------------+
      |
      v
+-------------+
|Storage Array|
+-------------+
```

**Fibre Channel Layers:**

**FC-4 – Protocol Mapping Layer:**

Maps upper-level protocols such as SCSI and NVMe-oF to Fibre Channel.

**FC-3 – Common Services Layer:**

Provides common service functionality.

**FC-2 – Framing and Flow Control Layer:**

Handles FC frames, sequencing and communication services.

**FC-1 – Encoding and Signaling Layer:**

Handles encoding and transmission-related functions.

**FC-0 – Physical Layer:**

Provides the physical connectivity.

**Types of Fibre Channel Ports:**

1. N-Port – Node Port, commonly available on server HBA ports.
2. F-Port – Fabric Port, used on FC switches.
3. E-Port – Expansion Port, used for switch-to-switch connections.
4. P-Port – Private port, as described in my notes.
5. L-Port – Loop-related port.

**Important identifiers:**

- WWN – World Wide Name.
- WWPN – World Wide Port Name.

WWN identifies a device or port in the Fibre Channel environment.

### **Q50. Explain iSCSI architecture, including Initiator, Target, Discovery, Session Establishment and Data Transfer.**

**Answer:**

iSCSI stands for Internet Small Computer System Interface.

It carries SCSI commands over TCP/IP networks.

**Main components:**

1. Initiator – Client-side component that sends storage commands.
2. Target – Storage-side component that receives and processes commands.
3. Network – Connects initiator and target.
4. LUN – Logical unit presented to the host.

**Architecture:**

```
+-----------------+
|      Host       |
| iSCSI Initiator |
+-----------------+
         |
      TCP/IP
         |
+-----------------+
| Ethernet Switch |
+-----------------+
         |
      TCP/IP
         |
+-----------------+
| iSCSI Target    |
|  Storage Array  |
+-----------------+
         |
        LUN
```

**iSCSI Discovery Process:**

1. Configure or identify the iSCSI initiator on the host.
2. Identify the target IP address.
3. Discover available targets.
4. Select the required target.
5. Establish the iSCSI connection.
6. Verify connectivity between host and target.
7. Create the required storage volume or LUN.
8. Map the volume to the host.
9. Rescan storage on the host to discover the LUN.

**Session Establishment:**

After discovery, the initiator logs in to the target.

The initiator and target establish a session over TCP/IP.

**Data Transfer:**

1. Application generates a storage request.
2. The host sends a SCSI command.
3. iSCSI encapsulates the command into an iSCSI PDU.
4. The PDU travels over the TCP/IP network.
5. The target processes the request.
6. Data or response is returned to the host.

**Example Linux Commands:**

To discover targets:

```
iscsiadm -m discovery -t sendtargets -p <target-ip>
```

To log in to a target:

```
iscsiadm -m node -T <target-iqn> -p <target-ip> --login
```

To check sessions:

```
iscsiadm -m session
```

To log out:

```
iscsiadm -m node -T <target-iqn> -p <target-ip> --logout
```

### **Q51. What is the difference between FCoE, iSCSI and Fibre Channel?**

**Answer:**

**FCoE – Fibre Channel over Ethernet:**

FCoE carries Fibre Channel frames over Ethernet networks.

It allows Fibre Channel storage traffic to use Ethernet infrastructure.

**iSCSI:**

iSCSI carries SCSI commands over TCP/IP networks.

It is commonly used to connect servers and storage arrays over Ethernet.

**Fibre Channel:**

Fibre Channel is a dedicated storage networking technology used to build SAN environments.

**Difference:**

| FCoE                                   | iSCSI                                    | Fibre Channel               |
| -------------------------------------- | ---------------------------------------- | --------------------------- |
| Fibre Channel over Ethernet            | SCSI over TCP/IP                         | Native FC fabric            |
| Uses Ethernet infrastructure           | Uses TCP/IP Ethernet network             | Uses Fibre Channel switches |
| Encapsulates FC frames in Ethernet     | Encapsulates SCSI commands in iSCSI PDUs | Uses FC frames              |
| Uses FC-related identifiers            | Uses IP and IQN                          | Uses WWN/WWPN               |
| Used in converged network environments | Used for IP-based SANs                   | Used for dedicated SANs     |

### **Q52. What is NVMe over Fabrics (NVMe-oF)? How does it differ from traditional iSCSI storage, and how does RDMA work?**

**Answer:**

NVMe-oF stands for NVMe over Fabrics.

It is a protocol that allows NVMe commands to be transferred between a host and a remote NVMe storage device over a network fabric.

It provides remote access to NVMe storage.

**Common NVMe-oF transports:**

- RDMA.
- Fibre Channel.
- TCP.

**Architecture:**

```
+------------------+
|   Host Server    |
|  NVMe Initiator  |
+------------------+
          |
       Network
          |
+------------------+
|   NVMe Target    |
| Remote NVMe SSD  |
+------------------+
```

**Difference between NVMe-oF and iSCSI:**

| NVMe-oF                                           | iSCSI                                 |
| ------------------------------------------------- | ------------------------------------- |
| Uses NVMe protocol                                | Uses SCSI command set                 |
| Designed for NVMe storage                         | Uses SCSI storage devices and targets |
| Supports multiple queue pairs                     | Uses SCSI command processing          |
| Can use RDMA, TCP and FC transports               | Runs over TCP/IP                      |
| Provides NVMe-oriented low-latency storage access | Uses network-based SCSI communication |

**How RDMA Works:**

RDMA stands for Remote Direct Memory Access.

It allows one system to access memory on another system with reduced CPU involvement.

**Working process:**

1. Host and target are connected through a network using RDMA-capable NICs.
2. The source system prepares a memory buffer.
3. RDMA operations transfer data directly between the registered memory regions of the two systems.
4. Data transfer requires less CPU intervention than conventional network data copying.
5. This reduces processing overhead and can improve performance.

**Advantages of RDMA:**

- Lower CPU utilization.
- Low latency.
- High throughput.
- Efficient data transfer.

# **Section 7 – NVMe Architecture and Management**

### **Q53. What is NVMe? Explain its architecture and how data transfers from the host to the target SSD.**

**Answer:**

NVMe stands for Non-Volatile Memory Express.

It is a high-performance storage protocol designed for non-volatile memory devices such as SSDs.

NVMe uses PCIe lanes to establish a high-speed connection between the host and the SSD.

It is faster than traditional SATA- and SAS-based storage protocols because it uses PCIe and supports multiple queues and parallel command processing.

**NVMe Architecture:**

```
+---------------------------+
|       Host Server         |
|                           |
|       Application         |
+---------------------------+
             |
        NVMe Driver
             |
+---------------------------+
|     Submission Queue      |
+---------------------------+
             |
         Doorbell
             |
+---------------------------+
|      NVMe Controller      |
+---------------------------+
             |
       NAND Flash Memory
             |
+---------------------------+
|     Completion Queue     |
+---------------------------+
             |
           Host
```

**Main Components:**

1. Host.
2. NVMe Driver.
3. Submission Queue.
4. Completion Queue.
5. NVMe Controller.
6. NAND Flash Memory.

**Data Transfer Process:**

1. The application sends an I/O request to the operating system.
2. The NVMe driver prepares an NVMe command.
3. The command is placed in the Submission Queue (SQ).
4. The host updates the controller's Doorbell Register to notify it about the new command.
5. The NVMe controller fetches the command from the Submission Queue.
6. The controller processes the command and accesses NAND Flash.
7. The controller places the command completion information in the Completion Queue (CQ).
8. The controller generates an interrupt or the host polls for completion.
9. The host reads the completion status and completes the I/O request.

For actual data movement, the controller uses DMA mechanisms and memory references supplied by the host.

**Important:** NVMe supports separate queues for Admin commands and I/O commands.

### **Q54. What is the difference between NVMe, SAS and SATA?**

**Answer:**

NVMe, SAS and SATA are storage protocols used to communicate with storage devices.

| Feature             | NVMe                                       | SAS                         | SATA                                  |
| ------------------- | ------------------------------------------ | --------------------------- | ------------------------------------- |
| Full form           | Non-Volatile Memory Express                | Serial Attached SCSI        | Serial Advanced Technology Attachment |
| Interface           | PCIe                                       | SAS interface               | SATA interface                        |
| Command protocol    | NVMe                                       | SCSI                        | ATA                                   |
| Main usage          | High-performance SSDs                      | Enterprise storage          | Desktop and general storage           |
| Performance         | Highest in the comparison in my notes      | High                        | Moderate                              |
| Queue architecture  | Multiple queue pairs                       | SCSI command queueing       | NCQ                                   |
| Queue capacity      | Up to 65,535 I/O queues according to notes | Controller/device dependent | Up to 32 outstanding NCQ commands     |
| Drive type          | SSD                                        | HDD and SSD                 | HDD and SSD                           |
| Latency             | Very low                                   | Higher than NVMe            | Higher than NVMe                      |
| Parallel processing | High parallelism                           | Supported                   | More limited                          |

**Why is NVMe faster?**

1. It uses PCIe.
2. It supports multiple queues.
3. It supports parallel command processing.
4. It is designed for flash-based storage.
5. It avoids some of the overhead associated with older storage protocols.

### **Q55. Explain NVMe Queue Architecture, Submission Queues, Completion Queues and Queue Depth. What is the maximum queue capacity mentioned in your notes?**

**Answer:**

NVMe uses a queue-based architecture to process storage commands.

There are two main types of queues:

1. Submission Queue (SQ).
2. Completion Queue (CQ).

**1. Submission Queue:**

The Submission Queue is used by the host to place NVMe commands that need to be executed by the controller.

**2. Completion Queue:**

The Completion Queue is used by the NVMe controller to place completion information after executing the commands.

**3. Queue Pair:**

A Submission Queue and a Completion Queue work together as a queue pair.

**NVMe Queue Architecture:**

```
+-----------------------+
|         Host          |
+-----------------------+
            |
            v
+-----------------------+
|   Submission Queue    |
|       Command 1        |
|       Command 2        |
|       Command 3        |
+-----------------------+
            |
         Doorbell
            |
            v
+-----------------------+
|    NVMe Controller    |
+-----------------------+
            |
            v
+-----------------------+
|      NAND Flash       |
+-----------------------+
            |
            v
+-----------------------+
|    Completion Queue   |
|       Status 1        |
|       Status 2        |
|       Status 3        |
+-----------------------+
            |
         Interrupt
            |
            v
+-----------------------+
|         Host          |
+-----------------------+
```

**Queue Types:**

NVMe maintains separate queues for:

**Admin Commands:**

- Admin Submission Queue.
- Admin Completion Queue.

**I/O Commands:**

- I/O Submission Queue.
- I/O Completion Queue.

**How NVMe works using queues:**

1. The host places a command in the Submission Queue.
2. The host informs the controller using the Doorbell mechanism.
3. The controller fetches and executes the command.
4. The controller writes completion status into the Completion Queue.
5. The host retrieves the completion information.

**Maximum Queue Capacity:**

According to my notes:

- NVMe supports a maximum of 65,535 I/O queues.
- Each queue can hold up to 65,535 commands, as stated in the notes.

Actual queue count and queue depth depend on the controller's capabilities and configuration.

### **Q56. What are NVMe Admin Commands and I/O Commands? Explain their purposes with examples.**

**Answer:**

There are two major types of NVMe commands:

1. Admin Commands.
2. I/O Commands.

**1. Admin Commands:**

Admin commands are used to manage and configure the NVMe controller and its resources.

They perform administrative operations.

Examples:

| Admin Command               | Purpose                                          |
| --------------------------- | ------------------------------------------------ |
| Create I/O Submission Queue | Creates an I/O Submission Queue                  |
| Delete I/O Submission Queue | Deletes an I/O Submission Queue                  |
| Create I/O Completion Queue | Creates an I/O Completion Queue                  |
| Delete I/O Completion Queue | Deletes an I/O Completion Queue                  |
| Identify                    | Retrieves controller or namespace information    |
| Get Log Page                | Retrieves log information                        |
| Abort                       | Attempts to abort a previously submitted command |
| Get Features                | Retrieves supported feature values               |
| Set Features                | Configures device features                       |
| Firmware Download           | Downloads firmware image                         |
| Firmware Commit             | Commits or activates firmware                    |

**2. I/O Commands:**

I/O commands are used to perform actual read/write and data-management operations.

Examples:

| I/O Command  | Purpose                                                   |
| ------------ | --------------------------------------------------------- |
| Read         | Reads data from SSD                                       |
| Write        | Writes data to SSD                                        |
| Flush        | Requests persistent completion of previously written data |
| Write Zeroes | Writes zeros to a logical block range                     |
| Compare      | Compares host data with device data                       |
| Format       | Formats a namespace                                       |

**Difference:**

| Admin Commands                   | I/O Commands             |
| -------------------------------- | ------------------------ |
| Used for device management       | Used for data operations |
| Manage controller and namespaces | Read/write storage data  |
| Use Admin Queue Pair             | Use I/O Queue Pairs      |

### **Q57. What is an NVMe Namespace? How do we create, attach, detach and identify namespaces?**

**Answer:**

An NVMe Namespace is a logical storage space provided by an NVMe controller.

It represents a quantity of non-volatile memory that can be formatted into logical blocks and accessed by a host.

Each namespace is identified using a Namespace ID (NSID).

**Example:**

Suppose an NVMe SSD has a total capacity of 1 TB.

We can divide it into three namespaces:

```
NVMe SSD – 1 TB
       |
   Controller
       |
 +-----+------+ 
 |     |      |
NS1   NS2    NS3
500GB 300GB  200GB
```

**Operations on Namespace:**

1. Create Namespace.
2. Attach Namespace.
3. Detach Namespace.
4. Identify Namespace.

**To list namespaces:**

```
nvme list
```

**To identify a namespace:**

```
nvme id-ns /dev/nvme0n1
```

**To create a namespace:**

```
nvme create-ns /dev/nvme0 --nsze=1000000 --ncap=1000000 --flbas=0
```

**To attach a namespace:**

```
nvme attach-ns /dev/nvme0 --namespace-id=1 --controllers=0
```

**To detach a namespace:**

```
nvme detach-ns /dev/nvme0 --namespace-id=1 --controllers=0
```

These operations require appropriate controller support and permissions.

### **Q58. What are the important NVMe commands such as Read, Write, Flush, Write Zeroes, Compare, Format and Firmware commands?**

**Answer:**

NVMe supports various commands to perform data operations and manage the SSD.

**1. Read:**

Used to read data from NAND Flash through the NVMe controller.

**2. Write:**

Used to write data to the SSD.

**3. Flush:**

Used to request that data previously written to the controller's volatile cache be made persistent in non-volatile storage.

**4. Write Zeroes:**

Used to write zeros to a specified logical block range.

**5. Compare:**

Used to compare supplied data with the data stored in the namespace.

**6. Format NVM:**

Used to format the namespace with a supported logical block format.

**7. Firmware Download:**

Used to download a firmware image to the NVMe controller.

**8. Firmware Commit:**

Used to commit or activate the downloaded firmware image according to the selected action.

### **Q59. How do we update NVMe SSD firmware? Explain Firmware Download, Firmware Commit and Activation.**

**Answer:**

NVMe firmware update is performed in three major stages:

1. Firmware Download.
2. Firmware Activation.
3. Firmware Commit.

**Step 1 – Check Existing Firmware Version:**

```
nvme id-ctrl /dev/nvme0
```

We identify the current firmware revision.

**Step 2 – Download Firmware:**

First, obtain the correct firmware binary from the drive vendor.

Then:

```
nvme fw-download /dev/nvme0 --fw=/path/firmware.bin
```

This downloads the firmware image to the controller.

**Step 3 – Firmware Commit:**

```
nvme fw-commit /dev/nvme0 --slot=1 --action=1
```

This commits the downloaded firmware into the selected firmware slot with the chosen activation action.

**Commit Actions:**

According to my notes:

| Action | Meaning                              |
| ------ | ------------------------------------ |
| 0      | Replace image only; no activation    |
| 1      | Activate at next reset               |
| 2      | Activate immediately, when supported |
| 3      | Activate at next reset               |
| 6      | Replace and activate at next reset   |

The supported action depends on the controller.

**Step 4 – Reboot or Reset:**

Perform the required controller reset or system reboot to activate the firmware.

**Step 5 – Verify Firmware Version:**

```
nvme id-ctrl /dev/nvme0
```

Verify that the firmware version is updated.

**Step 6 – Perform Validation:**

1. Check the device is detected.
2. Verify the new firmware version.
3. Check health information.
4. Check kernel logs.
5. Perform basic read/write testing.
6. Verify that all expected functions work.

**Important:** Firmware updates must use the correct vendor image and supported slot/activation actions. They should be performed according to the device vendor's release instructions.

### **Q60. What is the difference between NVMe SSDs connected directly through PCIe and NVMe-oF storage connected through a network?**

**Answer:**

There are two ways to access NVMe storage.

**1. Direct-Attached NVMe:**

In direct-attached NVMe, the SSD is connected directly to the server through PCIe.

```
+-------------+
|    Server   |
+-------------+
       |
     PCIe
       |
+-------------+
|  NVMe SSD   |
+-------------+
```

The host communicates directly with the NVMe controller using the PCIe interface.

**2. NVMe-oF:**

In NVMe over Fabrics, the NVMe storage device is connected remotely through a network fabric.

```
+-------------+
| Host Server |
+-------------+
       |
    NIC/HBA
       |
  Storage Network
       |
+-------------+
| NVMe Target |
+-------------+
```

It uses an NVMe transport such as RDMA, TCP or Fibre Channel.

**Difference:**

| Direct NVMe                 | NVMe-oF                              |
| --------------------------- | ------------------------------------ |
| Direct PCIe connection      | Network-based connection             |
| Local SSD                   | Remote NVMe storage                  |
| Uses PCIe lanes             | Uses network fabric                  |
| No storage network required | Requires network connectivity        |
| Direct local access         | Shared remote access can be provided |
| Very low transport latency  | Additional network transport latency |

# **Section 8 – Storage Provisioning and Management**

### **Q61. What is a RAID Group, Volume and LUN? Explain their relationship in a Storage Array.**

**Answer:**

These are important logical storage components in an enterprise storage array.

**1. RAID Group:**

A RAID Group is a group of physical drives configured using a particular RAID level.

It provides a usable storage pool with the selected RAID protection.

**2. Volume:**

A Volume is a logical storage space created from the available RAID Group capacity.

It represents a portion of storage capacity that can be presented to a host.

**3. LUN – Logical Unit Number:**

A LUN is an identifier used to identify a logical storage unit presented to a host.

The host uses the LUN to access the storage volume.

**Relationship:**

```
Physical Drives
      |
      v
   RAID Group
      |
      v
    Volume
      |
      v
     LUN
      |
      v
    Host
```

Example:

We have four 1 TB drives.

We create a RAID Group using RAID 5.

From this RAID Group, we create a 2 TB volume.

We assign a LUN ID and map the volume to a server.

Now the server can discover and access that LUN.

### **Q62. What is LUN Mapping and LUN Masking? Explain the difference.**

**Answer:**

**1. LUN Mapping:**

LUN Mapping is the process of assigning a storage volume or LUN to a particular host.

It allows the host to discover and access the assigned storage.

**2. LUN Masking:**

LUN Masking is the process of controlling which hosts are allowed to see and access a particular LUN.

It prevents unauthorized hosts from discovering or accessing the LUN.

**Difference:**

| LUN Mapping                    | LUN Masking                        |
| ------------------------------ | ---------------------------------- |
| Assigns a LUN to a host        | Controls LUN visibility and access |
| Associates storage with a host | Restricts access to selected hosts |
| Used for storage presentation  | Used for access control            |

**Example:**

Suppose we have three servers:

- Server 1.
- Server 2.
- Server 3.

We create a LUN and map it to Server 1.

Using LUN Masking, we ensure only Server 1 is allowed to see that LUN.

### **Q63. Explain the complete steps to create a RAID Group, Volume, Host Group and LUN Mapping.**

**Answer:**

In an enterprise storage array, we perform storage provisioning in the following order.

**Step 1 – Drive Discovery:**

Identify the available physical drives connected to the storage array.

Check:

- Drive status.
- Drive capacity.
- Drive type.
- Firmware version.
- Drive health.

**Step 2 – Create RAID Group:**

1. Log in to the storage management interface.
2. Select the available drives.
3. Choose the required RAID level.
4. Configure the block size and other supported parameters.
5. Create the RAID Group.

**Step 3 – Create Volume:**

1. Select the RAID Group.
2. Enter the volume name.
3. Specify the required capacity.
4. Create the volume.

**Step 4 – Create Host Group:**

1. Navigate to Host Management.
2. Create a Host Group.
3. Add the required server.
4. Add the HBA WWPN or iSCSI initiator identifier, depending on the protocol.

**Step 5 – LUN Mapping:**

1. Select the volume.
2. Select the target host or host group.
3. Assign a LUN ID.
4. Enable the required access permissions.
5. Apply the mapping.

**Step 6 – LUN Masking:**

Ensure that only the intended host or host group is permitted to access the LUN.

**Step 7 – Host Discovery:**

On the Linux server, rescan the storage paths.

For example:

```
lsblk
lsscsi
```

Then verify that the LUN appears correctly.

**Step 8 – Multipath Validation:**

If multiple storage paths are configured:

1. Verify all paths.
2. Check multipath service status.
3. Verify the LUN is accessible through the expected paths.

### **Q64. What is Zoning? Explain Soft Zoning and Hard Zoning.**

**Answer:**

Zoning is the process of dividing a SAN fabric into multiple zones.

Only devices belonging to the same permitted zone can communicate with each other.

It is used to control communication between server HBAs and storage ports.

**Types of Zoning:**

**1. Soft Zoning:**

Soft zoning uses World Wide Names (WWNs) to define permitted communication between devices.

Devices are included in zones based on their WWN identities.

**2. Hard Zoning:**

Hard zoning is enforced by the SAN switch hardware.

It restricts communication according to switch-port or supported hardware-enforced zoning rules.

**Difference:**

| Soft Zoning                                       | Hard Zoning                                      |
| ------------------------------------------------- | ------------------------------------------------ |
| Logical zoning                                    | Hardware-enforced zoning                         |
| Based on device WWN membership                    | Commonly enforced using switch port membership   |
| Controls permitted fabric communication logically | Enforces restrictions within the switch hardware |

**Example:**

Suppose we have:

- Server HBA WWPN.
- Storage target WWPN.

We create a zone containing the intended initiator and target, then activate the zoneset.

This allows only the intended storage connectivity.

### **Q65. What are the debugging steps if a LUN is not detected on the server?**

**Answer:**

If a LUN is not detected on the server, I follow a systematic troubleshooting approach.

**Step 1 – Check Storage Array:**

Verify:

- RAID Group status.
- Volume status.
- LUN creation.
- Host mapping.
- LUN masking.

**Step 2 – Check Host Group:**

Verify that the correct server is added to the host group.

Check the HBA WWPN or iSCSI initiator identity.

**Step 3 – Check Zoning:**

Verify that SAN zoning is configured correctly.

Ensure the server HBA can communicate with the storage target port.

**Step 4 – Check Physical Connectivity:**

Check:

- HBA status.
- Cable connectivity.
- Switch port status.
- Storage target port status.

**Step 5 – Check Linux Discovery:**

For SCSI-based storage:

```
lsscsi
```

For block devices:

```
lsblk
```

Perform an appropriate SCSI rescan if required.

**Step 6 – Check Multipath:**

If multipathing is configured:

```
multipath -ll
```

Verify that the expected paths are visible and operational.

**Step 7 – Check Logs:**

```
dmesg
journalctl
```

Look for:

- SCSI errors.
- Path failures.
- Connection errors.
- Device discovery failures.

**Step 8 – Isolate the Failure:**

Identify whether the issue is related to the storage array, SAN switch, HBA, driver, host configuration or operating system.

### **Q66. What are the debugging steps if a drive is not detected in a Storage Array?**

**Answer:**

When a drive is not detected in a storage array, I follow a systematic hardware and software troubleshooting approach.

**Step 1 – Check Physical Slot:**

Verify that the drive is properly inserted into the correct slot.

**Step 2 – Check Drive Status:**

Check whether the drive is powered on and whether the LED indicates any fault.

**Step 3 – Check Backplane:**

Verify the backplane connection and confirm that the slot is functioning properly.

**Step 4 – Check Expander:**

If an SAS expander is present, verify its connectivity and status.

**Step 5 – Check HBA or RAID Controller:**

Verify that the storage controller is functioning correctly.

**Step 6 – Cross-Swap Testing:**

1. Remove the suspect drive.
2. Insert another known-good compatible drive into the same slot.
3. Check whether it is detected.

If the known-good drive is also not detected, the issue may be related to the slot, backplane, expander or controller.

If the known-good drive is detected, investigate the original drive.

**Step 7 – Check Firmware and Logs:**

Check drive firmware compatibility and controller logs.

**Step 8 – Identify Root Cause:**

Determine whether the failure is related to:

- Drive.
- Backplane.
- Expander.
- Controller.
- Firmware.
- Cable or physical connection.

### **Q67. Can we map the same LUN to multiple servers? Explain the conditions and precautions.**

**Answer:**

Yes, we can map the same LUN to multiple servers when shared storage access is required.

This is commonly used in clustered environments.

However, we must configure the storage and host access correctly.

**Requirements:**

1. The LUN must be mapped to the required hosts.
2. LUN masking must allow the intended host access.
3. Multipathing must be configured correctly when multiple paths are available.
4. Hosts must use a supported shared-access mechanism.
5. Cluster coordination must be configured if multiple servers are writing to the same data.

**Example:**

Suppose we have two servers connected to a shared Storage Array.

We create one LUN and map it to both servers.

Both servers can discover the LUN.

**Important precaution:**

We should not mount an ordinary non-cluster-aware filesystem read/write on multiple servers simultaneously.

It can cause filesystem corruption.

For shared access, we need an appropriate clustered filesystem or application-level coordination and, where required, SCSI Persistent Reservations and fencing.

### **Q68. What are the different types of backups? Explain their differences.**

**Answer:**

A backup is a copy of data maintained separately so that we can recover information after data loss or failure.

The common backup types are:

**1. Full Backup:**

A Full Backup copies all selected data.

Advantages:

- Complete backup.
- Easy to restore.

Disadvantages:

- Requires more storage capacity.
- Takes more time.

**2. Incremental Backup:**

An Incremental Backup stores only the data changed since the previous backup.

Advantages:

- Requires less storage.
- Faster backup process.

Disadvantages:

\- Recovery may require the last full backup and all required incremental backups.

**3. Differential Backup:**

A Differential Backup stores all data changed since the last full backup.

Advantages:

- Easier restoration than a long incremental chain.
- Faster recovery than restoring many incremental backups.

Disadvantages:

\- Backup size increases as more changes accumulate.

**Difference:**

| Full Backup                | Incremental Backup                   | Differential Backup                    |
| -------------------------- | ------------------------------------ | -------------------------------------- |
| Copies all selected data   | Copies changes since previous backup | Copies changes since last full backup  |
| Larger storage requirement | Smaller backup size                  | Backup size grows over time            |
| Simple restoration         | Requires full plus incremental chain | Requires full plus latest differential |
| Takes longer               | Usually faster                       | Generally grows in backup duration     |

### **Q69. What is a Snapshot? How do we create a snapshot of a volume? How is it different from a backup?**

**Answer:**

A Snapshot is a point-in-time copy or representation of a storage volume.

It captures the state of a volume at a particular time.

We use snapshots to preserve a volume's state before performing operations such as:

- Firmware updates.
- Configuration changes.
- Application upgrades.
- Data modifications.

**Steps to create a Volume Snapshot:**

1. Log in to the storage array management interface.
2. Select the required storage volume.
3. Open the Snapshot Management option.
4. Select Create Snapshot.
5. Provide the snapshot name.
6. Configure the required snapshot settings.
7. Confirm the operation.
8. Verify that the snapshot has been created successfully.

**How many snapshots can be created?**

The supported number depends on the storage array vendor, model, firmware and configuration.

Your notes mention a limit of up to 33 snapshots for the described storage environment. This should not be treated as a universal limit for every storage array.

**Difference between Snapshot and Backup:**

| Snapshot                                     | Backup                                                         |
| -------------------------------------------- | -------------------------------------------------------------- |
| Point-in-time representation of a volume     | Separate copy of data                                          |
| Usually maintained within the storage system | Can be maintained on separate storage or backup infrastructure |
| Fast recovery in supported environments      | Used for broader data recovery                                 |
| May depend on the original volume and array  | Can be independent of the original storage system              |
| Not a complete replacement for backup        | Provides a separate recovery copy                              |

### **Q70. What is Replication? Explain Synchronous and Asynchronous Replication.**

**Answer:**

Replication is the process of copying data from a primary storage system or volume to a secondary storage system or volume.

It is used for data protection, availability and disaster recovery.

There are two main types:

1. Synchronous Replication.
2. Asynchronous Replication.

**1. Synchronous Replication:**

In synchronous replication, data is written to the primary and secondary storage systems before the write operation is acknowledged to the host.

**Working:**

1. Host sends a write request.
2. Primary storage receives the data.
3. Data is transferred to secondary storage.
4. The write is acknowledged after the required synchronous write conditions are satisfied.

**Advantages:**

- Very low data-loss exposure.
- Both copies remain synchronized for acknowledged writes.

**Disadvantages:**

- Higher latency.
- Requires suitable network connectivity and distance.

**2. Asynchronous Replication:**

In asynchronous replication, data is acknowledged at the primary storage before all changes are transferred to the secondary storage.

**Working:**

1. Host sends a write request.
2. Primary storage receives and processes the write.
3. Primary storage acknowledges the write.
4. Data is transferred to secondary storage later.

**Advantages:**

- Faster host response.
- Suitable for longer-distance replication.
- Lower impact on primary write latency.

**Disadvantages:**

\- Some data may be lost if the primary fails before pending changes reach the secondary.

**Difference:**

| Synchronous Replication                                         | Asynchronous Replication                                       |
| --------------------------------------------------------------- | -------------------------------------------------------------- |
| Writes are coordinated with the secondary before acknowledgment | Writes are acknowledged before secondary replication completes |
| Very low data-loss exposure                                     | Some data loss is possible                                     |
| Higher latency                                                  | Lower host-side latency                                        |
| Generally used for shorter-distance replication                 | Can be used for longer-distance replication                    |

### **Q71. What is Remote Copy? How is it useful for Disaster Recovery?**

**Answer:**

Remote Copy is the process of copying data from one storage location to another storage location, usually across geographically separated sites.

It is used to protect business data against disasters.

**Working process:**

1. Primary storage contains the production data.
2. Secondary storage is configured at another location.
3. Data is replicated or copied from primary to secondary.
4. If the primary site fails, the secondary site can be used for recovery according to the disaster-recovery procedure.

**Advantages:**

- Data protection.
- Disaster recovery.
- Business continuity.
- Recovery from site-level failures.

**Example:**

Suppose a company has:

- Primary Data Center in Bangalore.
- Secondary Data Center in Hyderabad.

The production storage array replicates data to the secondary storage array.

If the primary data center becomes unavailable, we can recover services using the secondary site.

### **Q72. What is Data Deduplication and Data Compression? Explain their differences.**

**Answer:**

**Data Deduplication:**

Data Deduplication is the process of identifying duplicate data and storing only one unique copy.

Instead of storing repeated data multiple times, the system maintains references to the unique stored data.

There are two types mentioned in my notes:

1. File-Level Deduplication.
2. Block-Level Deduplication.

**Data Compression:**

Data Compression is the process of reducing the size of data to save storage capacity.

It uses compression techniques to represent the same information using fewer bits or bytes.

**Difference:**

| Deduplication                         | Compression                        |
| ------------------------------------- | ---------------------------------- |
| Removes duplicate data                | Reduces the size of data           |
| Stores unique copies                  | Compresses existing data           |
| Works at file or block level          | Works by encoding data efficiently |
| Saves space by eliminating duplicates | Saves space by reducing data size  |

### **Q73. What is Thin Provisioning and Thick Provisioning? Explain their differences.**

**Answer:**

**Thin Provisioning:**

Thin Provisioning is a storage allocation method in which logical storage capacity is presented to the host, but physical storage space is consumed as data is written.

For example, we can create a 1 TB logical volume while initially consuming much less than 1 TB of physical storage.

Physical space is allocated as required.

**Thick Provisioning:**

Thick Provisioning is a storage allocation method in which the full physical capacity is reserved or allocated when the volume is created.

For example, when we create a 1 TB thick volume, the storage system reserves the full 1 TB capacity.

**Difference:**

| Thin Provisioning                                | Thick Provisioning                    |
| ------------------------------------------------ | ------------------------------------- |
| Physical capacity is consumed as data is written | Physical capacity is reserved upfront |
| Efficient capacity utilization                   | Predictable allocated capacity        |
| Can overcommit logical capacity                  | Usually does not rely on overcommit   |
| Requires careful capacity monitoring             | Capacity is reserved from creation    |

# **Section 9 – Firmware, RAID Utilities and Troubleshooting**

### **Q74. What is Firmware? How do you update firmware on a Drive and HBA? What is the procedure for rollback if the update fails?**

**Answer:**

Firmware is a type of software that runs on hardware components and controls their functionality.

It is embedded into hardware devices.

Examples:

- SSD Firmware.
- HDD Firmware.
- HBA Firmware.
- RAID Controller Firmware.
- BIOS Firmware.
- BMC Firmware.

**Why do we update firmware?**

1. To introduce new features.
2. To fix existing bugs.
3. To improve device performance.
4. To resolve compatibility issues.
5. To improve device stability.

**Firmware Update Procedure:**

**Step 1 – Identify Current Firmware**

Check the existing firmware version of the drive or HBA.

**Step 2 – Download Firmware**

Download the correct firmware image from the vendor.

**Step 3 – Check Compatibility**

Verify that the firmware is compatible with:

- Drive model.
- HBA model.
- Controller.
- Hardware platform.
- Operating system, where applicable.

**Step 4 – Read Release Notes**

Understand what defects are fixed and what changes are introduced in the new firmware.

**Step 5 – Prepare Environment**

Ensure:

- Stable power supply.
- Correct firmware image.
- Required tools.
- Backup of important data.
- No unexpected I/O activity during the update.

**Step 6 – Install Firmware**

Use the vendor-supported firmware update utility.

For NVMe SSDs, the commands covered in my notes are:

```
nvme fw-download /dev/nvme0 --fw=/path/firmware.bin
```

Then:

```
nvme fw-commit /dev/nvme0 --slot=1 --action=1
```

For HBA firmware, use the appropriate vendor-supported HBA firmware utility.

**Step 7 – Activate Firmware**

Perform the required device reset, controller reset or reboot to activate the new firmware.

**Step 8 – Verify Firmware**

Check the firmware version and confirm that the updated version is active.

**Step 9 – Perform Functional Testing**

Verify:

- Drive detection.
- Controller detection.
- Read/write operations.
- Device health.
- Storage connectivity.
- Firmware stability.

**Firmware Rollback Procedure:**

If the new firmware causes an issue:

1. Collect logs and identify the failure.
2. Stop further firmware update attempts.
3. Check whether the previous firmware version is supported for downgrade.
4. Download the previous stable firmware.
5. Use the vendor-supported downgrade or recovery procedure.
6. Activate the previous firmware.
7. Verify the firmware version.
8. Perform functional and regression testing.

**Example:**

Suppose an SSD was working correctly with Firmware Version 1.0.

After upgrading to Version 2.0, the drive is no longer detected.

We investigate the failure, collect logs, and if the firmware is identified as the cause, we roll back to Version 1.0 using the supported recovery procedure.

### **Q75. What is I/O Timeout and I/O Error? What are the possible causes and how do you troubleshoot them?**

**Answer:**

**I/O Timeout:**

An I/O Timeout occurs when a storage command does not complete within the expected timeout period.

The host waits for the response from the storage device, but the response does not arrive within the configured time.

**I/O Error:**

An I/O Error occurs when a read or write operation fails and the host receives an error instead of a successful completion.

**Possible Causes:**

1. Drive failure.
2. HBA failure.
3. RAID Controller issue.
4. Cable or backplane connectivity problem.
5. SAS Expander issue.
6. Firmware problems.
7. Driver-related issues.
8. PCIe or storage-path instability.
9. Storage network failure.
10. Controller overload.

**Troubleshooting Approach:**

**Step 1 – Identify the Failure**

Understand whether the issue is an I/O timeout or an I/O error.

Identify the affected drive, LUN or storage path.

**Step 2 – Check Physical Connectivity**

Verify:

- Power connections.
- Storage cables.
- Backplane.
- HBA.
- Expander.
- Controller ports.

**Step 3 – Check Device Detection**

```
lsblk
```

```
lsscsi
```

For NVMe:

```
nvme list
```

**Step 4 – Check Device Health**

For supported ATA/SATA drives:

```
smartctl -a /dev/sda
```

For NVMe:

```
nvme smart-log /dev/nvme0
```

**Step 5 – Check Logs**

```
dmesg
```

```
journalctl -k
```

Look for:

- I/O errors.
- Device resets.
- Command timeouts.
- Controller errors.
- Link failures.

**Step 6 – Check Multipathing**

If shared storage is used:

```
multipath -ll
```

Verify whether all expected paths are available.

**Step 7 – Isolate the Issue**

Try a known-good drive or slot when appropriate.

Check another path, controller or server if available.

**Step 8 – Identify Root Cause**

Determine whether the issue belongs to:

- Hardware.
- Firmware.
- Driver.
- Operating System.
- Storage Controller.
- Network.
- Configuration.

**Step 9 – Verify the Fix**

After resolving the issue, execute read/write tests and monitor I/O performance to ensure that the problem is resolved.

### **Q76. Explain StorCLI commands and procedures for the following operations: Convert RAID drives to Non-RAID/JBOD, install drive firmware, create Hardware RAID and start RAID Consistency Check.**

**Answer:**

StorCLI is a command-line utility used to manage supported Broadcom/MegaRAID storage controllers.

It is used for operations such as:

- Drive identification.
- RAID Group creation.
- Virtual Drive creation.
- Drive status checking.
- Hot Spare configuration.
- Consistency Check.
- Controller management.

**1. Convert RAID Drives to Non-RAID/JBOD**

First, identify the controller and drives.

```
storcli /c0/eall/sall show
```

Here:

- `/c0` – Controller 0.
- `/eall` – All enclosures.
- `/sall` – All slots.

To convert a supported drive to JBOD mode:

```
storcli /c0/e252/s0 set jbod
```

To convert a JBOD drive back to Unconfigured Good:

```
storcli /c0/e252/s0 set good
```

Here:

- `e252` – Example enclosure ID.
- `s0` – Example drive slot.

**2. Install Drive Firmware**

The general firmware update process is:

1. Identify the connected drives.
2. Check their model and existing firmware versions.
3. Download the correct drive firmware.
4. Verify controller and drive compatibility.
5. Use the vendor-supported firmware update utility.
6. Activate the firmware if required.
7. Verify the new firmware version.
8. Perform functional validation.

For NVMe drives, my notes provide the following firmware commands:

```
nvme fw-download /dev/nvme0 --fw=/path/firmware.bin
```

```
nvme fw-commit /dev/nvme0 --slot=1 --action=1
```

**Important:** The exact StorCLI drive-firmware download syntax is not specified in your notes. It depends on the controller, drive model and supported firmware update method, so I would not use an assumed StorCLI command.

**3. Create Hardware RAID**

First, identify the controller and available drives:

```
storcli /c0/eall/sall show
```

To create RAID 1 using two drives:

```
storcli /c0 add vd type=raid1 drives=252:0,252:1
```

Here:

- `/c0` – Controller 0.
- `type=raid1` – RAID 1 configuration.
- `252:0,252:1` – Example enclosure/slot identifiers.

After creating RAID:

```
storcli /c0/vall show
```

This displays the virtual drives.

**4. Start RAID Consistency Check**

Consistency Check is used to verify RAID data and parity consistency.

Command:

```
storcli /c0/v0 start cc
```

Here:

- `/c0` – Controller 0.
- `/v0` – Virtual Drive 0.
- `start cc` – Starts Consistency Check.

To check the operation status:

```
storcli /c0/v0 show
```

**Important:** Controller numbering, enclosure IDs, slot numbers and supported commands depend on the actual hardware configuration. The above commands are examples; verify the controller and drive mapping before execution.

# **Storage – Final Completion Summary**

## **Important Storage concepts for interview revision**

| Topic              | Key point                                     |
| ------------------ | --------------------------------------------- |
| RAID 0             | Striping without redundancy                   |
| RAID 1             | Mirroring                                     |
| RAID 5             | Distributed single parity                     |
| RAID 6             | Distributed dual parity                       |
| RAID 10            | Mirroring + Striping                          |
| HBA                | Connects server with storage                  |
| RAID Controller    | Manages hardware RAID                         |
| Backplane          | Connects drive slots to storage connectivity  |
| Expander           | Expands SAS connectivity                      |
| SCSI               | Uses CDB commands                             |
| SAS                | Enterprise Serial Attached SCSI               |
| SATA               | Serial Advanced Technology Attachment         |
| NVMe               | PCIe-based storage protocol                   |
| Namespace          | Logical storage space in NVMe                 |
| SQ                 | Submission Queue                              |
| CQ                 | Completion Queue                              |
| iSCSI              | SCSI over TCP/IP                              |
| Fibre Channel      | Dedicated storage networking                  |
| NVMe-oF            | NVMe over network fabrics                     |
| Multipath          | Multiple paths to the same storage target     |
| LUN Mapping        | Assigns storage to a host                     |
| LUN Masking        | Controls LUN visibility and access            |
| Zoning             | Controls communication in SAN fabric          |
| Snapshot           | Point-in-time representation of a volume      |
| Replication        | Copies data between storage systems           |
| Thin Provisioning  | Physical capacity consumed as data is written |
| Thick Provisioning | Physical capacity reserved upfront            |
| Firmware           | Software that controls hardware functionality |

**Storage preparation is complete.**
