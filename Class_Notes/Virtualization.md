# **Virtualization – Complete Interview Questions & Answers**


# **Section 1 – Virtualization Fundamentals**

### **Q1. What is virtualization?**

**Answer:**

Virtualization is a software technology that allows us to create virtual versions of physical resources such as servers, operating systems, storage and networks.

It allows us to run multiple virtual machines on a single physical server.

Each virtual machine can have its own operating system and applications while sharing the resources of the physical server.

For example, using VMware ESXi, we can create multiple virtual machines on one physical server and install different operating systems on each VM.

### **Q2. Why do we use virtualization, and how does it allow multiple operating systems to run on a single physical server?**

**Answer:**

We use virtualization to utilize physical server resources efficiently and reduce the requirement for multiple physical servers.

A hypervisor is the virtualization layer that allows us to create and run multiple virtual machines on a single physical server.

The working process is:

1. We have a physical server containing CPU, RAM, storage and network resources.
2. We install a hypervisor such as VMware ESXi on the physical server.
3. The hypervisor creates virtual machines.
4. We allocate virtual CPU, virtual memory, virtual storage and virtual network resources to each VM.
5. We install a Guest OS inside each virtual machine.
6. Each VM runs its own operating system and applications.

All the virtual machines share the resources of the same physical server.

### **Q3. What are the advantages of virtualization?**

**Answer:**

The main advantages of virtualization are:

1. **Effective resource utilization:** We can utilize CPU, memory, storage and network resources efficiently by running multiple VMs on one physical server.
2. **Server consolidation:** Multiple physical workloads can be consolidated onto fewer physical servers.
3. **Reduced maintenance cost:** We need fewer physical servers to maintain.
4. **Reduced power consumption:** Using fewer physical servers reduces power consumption.
5. **Easy maintenance:** We can manage multiple virtual machines from a centralized platform.
6. **Resource flexibility:** We can allocate virtual resources to VMs based on their requirements.
7. **Migration:** We can migrate virtual machines between ESXi hosts for hardware maintenance and load balancing.

### **Q4. What are the disadvantages of virtualization?**

**Answer:**

The main disadvantages are:

1. **Single physical server failure:** If a physical server fails, all VMs running on that server can become unavailable.
2. **Resource contention:** Multiple VMs share physical resources. If one VM consumes excessive CPU, memory or storage resources, other VMs can be affected.
3. **Performance overhead:** Virtualization introduces some overhead compared to running directly on physical hardware.
4. **Management complexity:** Managing multiple ESXi hosts, clusters, datastores and virtual machines requires proper administration.
5. **Licensing and infrastructure cost:** Enterprise virtualization may require additional licensing and infrastructure.

### **Q5. What are the different virtualization technologies and platforms mentioned in your notes?**

**Answer:**

The different virtualization technologies and platforms mentioned in my notes are:

| Company   | Virtualization technology   |
| --------- | --------------------------- |
| VMware    | ESXi                        |
| Microsoft | Hyper-V                     |
| Red Hat   | KVM                         |
| Nutanix   | AHV                         |
| Citrix    | XenServer                   |
| Oracle    | Oracle Cloud Infrastructure |

These platforms provide virtualization capabilities to run multiple virtual machines and applications using physical server resources.

### **Q6. What is the difference between a physical server and a virtual machine?**

**Answer:**

A physical server is an actual hardware system containing physical components such as CPU, RAM, storage, motherboard and network interfaces.

A virtual machine is a software-created machine that runs on top of a physical server using virtualized hardware resources.

| Physical Server                                        | Virtual Machine                           |
| ------------------------------------------------------ | ----------------------------------------- |
| Actual physical hardware                               | Software-based machine                    |
| Contains physical CPU                                  | Uses virtual CPU                          |
| Contains physical RAM                                  | Uses virtual memory                       |
| Uses physical storage                                  | Uses virtual disks                        |
| Has physical network interfaces                        | Uses virtual NICs                         |
| Hardware resources are provided by the physical system | Resources are allocated by the hypervisor |
| Can host multiple virtual machines                     | Runs as a guest on a physical host        |

For example, one physical server with VMware ESXi can host multiple virtual machines, each with a separate Guest OS.

# **Section 2 – Hypervisor and VMware ESXi**

### **Q7. What is a hypervisor?**

**Answer:**

A hypervisor is a virtualization layer that allows us to create, manage and run multiple virtual machines on a single physical server.

It acts as an interface between the physical hardware and virtual machines.

The hypervisor manages and allocates physical resources such as:

- CPU
- RAM
- Storage
- Network

Using a hypervisor, we can run multiple Guest OS instances on a single physical server.

### **Q8. What is the role of a hypervisor in virtualization?**

**Answer:**

The main role of a hypervisor is to manage physical server resources and provide virtual resources to multiple virtual machines.

Its responsibilities include:

1. Creating and managing virtual machines.
2. Allocating virtual CPU and memory.
3. Providing virtual storage to VMs.
4. Managing virtual networking.
5. Isolating virtual machines from each other.
6. Sharing physical hardware resources among multiple VMs.
7. Managing VM operations such as starting, stopping and migration.

For example, VMware ESXi acts as a hypervisor and allows multiple VMs to run on a single physical server.

### **Q9. What are the different types of hypervisors?**

**Answer:**

There are two major types of hypervisors:

1. **Type 1 Hypervisor:** Also called a Bare-Metal Hypervisor.
2. **Type 2 Hypervisor:** Also called a Hosted Hypervisor.

The main difference is where the hypervisor is installed.

- Type 1 runs directly on physical server hardware.
- Type 2 runs on top of an existing host operating system.

### **Q10. Explain the architecture of Type 1 and Type 2 hypervisors with diagrams.**

**Answer:**

**1. Type 1 Hypervisor – Bare-Metal Architecture**

Type 1 hypervisor runs directly on top of physical server hardware without requiring a separate host operating system.

Architecture:

```
+--------------------------+
|       Guest OS 1         |
+--------------------------+
|       Guest OS 2         |
+--------------------------+
|       Guest OS 3         |
+--------------------------+
|    Type 1 Hypervisor     |
+--------------------------+
|    Physical Hardware    |
| CPU | RAM | Storage | NIC|
+--------------------------+
```

Examples:

- VMware ESXi
- Microsoft Hyper-V (bare-metal deployment)
- Citrix XenServer
- Nutanix AHV

**2. Type 2 Hypervisor – Hosted Architecture**

Type 2 hypervisor runs on top of an existing host operating system.

Architecture:

```
+--------------------------+
|       Guest OS 1         |
+--------------------------+
|       Guest OS 2         |
+--------------------------+
|    Type 2 Hypervisor     |
+--------------------------+
|        Host OS           |
+--------------------------+
|    Physical Hardware    |
| CPU | RAM | Storage | NIC|
+--------------------------+
```

Examples:

- VMware Workstation
- Oracle VirtualBox

### **Q11. What is the difference between Type 1 and Type 2 hypervisors?**

**Answer:**

| Feature      | Type 1 Hypervisor                               | Type 2 Hypervisor                    |
| ------------ | ----------------------------------------------- | ------------------------------------ |
| Architecture | Bare-metal                                      | Hosted                               |
| Installation | Directly on hardware                            | On top of Host OS                    |
| Host OS      | Not required as a separate layer                | Required                             |
| Performance  | Generally higher                                | Has additional host OS overhead      |
| Security     | Smaller dependency on a general-purpose host OS | Depends partly on host OS security   |
| Usage        | Enterprise servers and data centers             | Desktop and workstation environments |
| Examples     | ESXi, XenServer, Hyper-V                        | VMware Workstation, VirtualBox       |

### **Q12. Why is Type 1 hypervisor considered more secure, stable and faster?**

**Answer:**

Type 1 hypervisor runs directly on physical server hardware without depending on a separate general-purpose host operating system.

This reduces the additional software layer between the hypervisor and the hardware.

Type 2 hypervisor runs on top of a host operating system, so its operation also depends on the host OS.

Therefore, Type 1 hypervisors are generally preferred for enterprise server environments because they offer better performance isolation and a smaller host OS dependency.

### **Q13. What is a bare-metal server?**

**Answer:**

A bare-metal server is a physical server where a virtualization hypervisor or operating system can be installed directly on the hardware without requiring another host operating system underneath it.

In virtualization, we commonly install VMware ESXi directly on the physical server.

After installing ESXi, we can create multiple virtual machines and run different Guest OS instances.

### **Q14. What is VMware ESXi, and how does it work?**

**Answer:**

VMware ESXi is a Type 1 hypervisor used for enterprise server virtualization.

It is installed directly on physical server hardware.

It allows us to create and manage multiple virtual machines on a single physical server.

**Working process:**

1. We prepare a physical server with CPU, RAM, storage and network resources.
2. We install VMware ESXi directly on the server hardware.
3. ESXi initializes and manages the available hardware resources.
4. We create virtual machines on the ESXi host.
5. We allocate virtual CPU, virtual memory, virtual storage and virtual network resources to each VM.
6. We install Guest OS instances inside the VMs.
7. Each VM runs its applications using the resources allocated by ESXi.

ESXi helps us utilize physical server resources efficiently and manage multiple virtual machines.

# **Section 3 – Virtual Machine Architecture**

### **Q15. What is a Virtual Machine (VM)?**

**Answer:**

A Virtual Machine is a software-based machine that provides an environment to install and run an operating system and applications.

It behaves like a physical computer from the Guest OS perspective.

A VM contains virtual hardware resources such as:

- Virtual CPU
- Virtual Memory
- Virtual Storage
- Virtual Switch connectivity
- Virtual NIC

A physical server shares its hardware resources among multiple VMs through the hypervisor.

For example, using one ESXi host, we can create multiple VMs and install Linux and Windows operating systems on them.

### **Q16. What are the different components of a virtual machine?**

**Answer:**

The main components of a virtual machine are:

1. Guest OS
2. Virtual CPU (vCPU)
3. Virtual Storage
4. Virtual Switch
5. Virtual Memory (RAM)
6. Virtual NIC (Network Interface Card)

### **Q17. Explain Guest OS, Virtual CPU, Virtual Memory, Virtual Storage, Virtual Switch and Virtual NIC.**

**Answer:**

**1. Guest OS:**

Guest OS is the operating system installed inside a virtual machine.

Examples include Windows and Linux.

**2. Virtual CPU (vCPU):**

A virtual CPU is the processing resource allocated to a virtual machine.

The hypervisor schedules the VM's virtual CPU execution on the available physical CPU cores.

**3. Virtual Memory:**

Virtual memory is the RAM resource allocated to a virtual machine.

The VM uses this memory to run its operating system and applications.

**4. Virtual Storage:**

Virtual storage is the storage space presented to the VM, usually in the form of virtual disks.

It stores the Guest OS, applications and user data.

**5. Virtual Switch:**

A virtual switch connects virtual machine network interfaces and provides connectivity to external networks through physical network adapters.

**6. Virtual NIC:**

A Virtual NIC is the network interface assigned to a VM.

It allows the VM to communicate with other VMs and external networks through a virtual switch.

### **Q18. How does a physical server share its resources among multiple virtual machines?**

**Answer:**

A physical server contains hardware resources such as CPU, RAM, storage and network interfaces.

The hypervisor manages these resources and allocates virtual resources to each VM.

For example, consider a physical server with 16 CPU cores and 64 GB RAM.

We can create multiple VMs and allocate virtual CPUs and memory to each one, according to the available resources and workload requirements.

The hypervisor schedules CPU execution, manages memory allocation, provides virtual storage and manages virtual networking.

Thus, multiple virtual machines can run independently while sharing the same physical server resources.

# **Section 4 – Datastore and Storage Management**

### **Q19. What is a datastore?**

**Answer:**

A datastore is a logical storage location used by VMware ESXi to store virtual machine files and other virtualization-related data.

Datastores are formatted using a filesystem such as VMFS.

We use datastores to store and manage VM files, virtual disks and related information.

### **Q20. What type of data is stored in a datastore?**

**Answer:**

A datastore stores different types of virtual machine files.

The main files include:

1. **VMDK:** Stores the virtual machine's virtual disk data.
2. **VMX:** Stores the virtual machine configuration.
3. **NVRAM:** Stores the virtual BIOS/UEFI-related state.
4. **VMSD:** Stores snapshot metadata.
5. **VMSN:** Stores snapshot state information.
6. **VMware log files:** Store virtual machine execution and diagnostic information.
7. **ISO images:** Used to install operating systems or other software.

For example, when we create a VM, its configuration file and virtual disk files are stored in a datastore.

### **Q21. What are the different types of datastores?**

**Answer:**

Datastores can be classified based on where the storage is available.

**1. Local Datastore:**

A local datastore is created using the internal storage connected to an individual ESXi host.

It is generally accessible to that particular host and is not automatically shared with other ESXi hosts.

**2. External or Shared Datastore:**

An external datastore uses storage provided by external storage systems.

Examples include:

- SAN – Storage Area Network.
- NAS – Network Attached Storage.
- iSCSI – Internet Small Computer Systems Interface.

Shared datastores can be accessed by multiple ESXi hosts, provided the storage is presented and configured correctly.

### **Q22. What is the difference between local storage and shared storage in virtualization?**

**Answer:**

| Feature       | Local Storage                                                          | Shared Storage                                               |
| ------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------ |
| Location      | Internal storage of an ESXi host                                       | External storage system                                      |
| Connectivity  | Connected to an individual host                                        | Connected through a shared storage infrastructure            |
| Accessibility | Generally available to one ESXi host                                   | Can be accessed by multiple ESXi hosts                       |
| Migration     | Does not directly support shared-storage-based migration between hosts | Supports host migration when the required conditions are met |
| Examples      | Internal HDD, SSD or NVMe                                              | SAN, NAS and iSCSI storage                                   |

**Example:**

If we have two ESXi hosts and a shared datastore connected to both hosts, virtual machines can use the same datastore.

This helps us perform vMotion because the destination host can access the VM's storage files.

### **Q23. How do we manage multiple ESXi hosts and datastores? What is the role of vCenter/vSphere?**

**Answer:**

We can manage ESXi hosts using the ESXi Host Client, command-line tools and centralized VMware management tools.

**vCenter Server:**

vCenter Server is a centralized management application used to manage multiple ESXi hosts and virtual machines.

Using vCenter, we can:

1. Add and manage multiple ESXi hosts.
2. Create and manage clusters.
3. Manage virtual machines.
4. Manage datastores.
5. Configure HA and DRS.
6. Perform VM migration.
7. Monitor host and VM resources.

**vSphere:**

VMware vSphere is the virtualization platform that includes the components used to run and manage virtualized infrastructure. The vSphere Client provides the graphical interface for management, while vCenter Server provides centralized management.

**Interview clarification:** vSphere and vCenter are not exactly the same. vSphere is the platform, whereas vCenter Server is its centralized management component.

# **Section 5 – Virtual Machine Migration**

### **Q24. What is migration in virtualization?**

**Answer:**

Migration is the process of moving a virtual machine or its storage files from one location to another in a virtualized environment.

In VMware, migration is used to move virtual machines between ESXi hosts or move their files between datastores.

For example, we can migrate a running VM from one ESXi host to another ESXi host without shutting down the VM by using vMotion.

Migration is useful for:

- Load balancing.
- Hardware maintenance.
- Storage maintenance.
- Resource management.
- Reducing service interruption.

### **Q25. What are the different types of migration?**

**Answer:**

There are two classifications of migration covered in my notes.

**Based on VM power state:**

1. **Hot Migration:** Moving a powered-on VM.
2. **Cold Migration:** Moving a powered-off VM.

**Based on the migration operation:**

1. **vMotion:** Migrates a running VM from one ESXi host to another.
2. **Storage vMotion:** Migrates VM storage files from one datastore to another.
3. **XvMotion:** Combines host migration and storage migration.

### **Q26. What is the difference between Hot Migration and Cold Migration?**

**Answer:**

**Hot Migration:**

Hot migration is the process of moving a powered-on virtual machine from one ESXi host to another.

The VM continues running during migration, and the objective is to avoid application downtime.

**Cold Migration:**

Cold migration is the process of moving a powered-off virtual machine from one ESXi host to another.

The VM remains powered off during migration.

| Feature     | Hot Migration                           | Cold Migration              |
| ----------- | --------------------------------------- | --------------------------- |
| VM state    | Powered on                              | Powered off                 |
| Application | Continues running                       | Stopped                     |
| Downtime    | Designed to avoid downtime              | Downtime is involved        |
| Usage       | Hardware maintenance and load balancing | When downtime is acceptable |

### **Q27. What is vMotion?**

**Answer:**

vMotion is a VMware feature used to migrate a powered-on virtual machine from one ESXi host to another ESXi host.

During vMotion, the VM's active memory state and execution state are transferred from the source ESXi host to the destination ESXi host.

The VM continues running during the migration process, with only a brief switchover interruption.

We use vMotion for:

- Load balancing.
- Hardware maintenance.
- Moving VMs away from an ESXi host that requires maintenance.

### **Q28. Explain how vMotion works, including the transfer of VM memory state.**

**Answer:**

vMotion transfers a running virtual machine from a source ESXi host to a destination ESXi host.

The working process is:

1. We identify the source and destination ESXi hosts.
2. We verify that both hosts have compatible CPU resources and network connectivity.
3. The VM's storage must be accessible to the destination host for a standard shared-storage vMotion operation.
4. A VMkernel network interface is configured for vMotion traffic.
5. The initial VM memory contents are copied from the source host to the destination host.
6. While the VM continues running, memory pages that change are tracked and transferred again.
7. A brief switchover takes place, during which the VM execution is transferred to the destination host.
8. The VM resumes execution on the destination host.

The application continues operating with only a brief interruption during the final switchover.

**Example:**

Suppose we have ESXi Host 1 and ESXi Host 2.

A VM is running on ESXi Host 1. When we perform vMotion, the VM's memory and execution state are transferred to ESXi Host 2. The VM then continues running on ESXi Host 2.

### **Q29. What are the requirements for performing vMotion?**

**Answer:**

The main requirements for standard shared-storage vMotion are:

1. **Shared Storage:** Source and destination ESXi hosts should have access to the VM's shared datastore.
2. **Network Connectivity:** Both ESXi hosts should have proper network connectivity.
3. **Compatible CPU:** Source and destination hosts should have compatible CPU features.
4. **VMkernel Port Group:** A VMkernel network interface must be configured for vMotion traffic.
5. **Destination Resources:** The destination ESXi host should have sufficient CPU and memory resources.
6. **Compatible Configuration:** The source and destination hosts must have compatible virtualization and VM configurations.
7. **Connectivity:** The vMotion network must be configured correctly.

According to my notes, the vMotion network should have a minimum bandwidth of 1 Gbps.

**Additional clarification:** The 1 Gbps value is the minimum mentioned in your notes, not a universal performance recommendation for every modern vMotion environment.

### **Q30. What is a VMkernel port group, and why is it required for migration?**

**Answer:**

A VMkernel port group is a network configuration on an ESXi host that provides network connectivity for ESXi host-level services.

It is used for services such as:

- vMotion.
- Management network.
- Storage network services.
- Other host-level network services.

For vMotion, we configure a VMkernel interface with vMotion enabled.

This interface provides communication between the source and destination ESXi hosts for transferring VM memory and migration-related information.

**Important technical clarification:** Your notes describe a VMkernel port group as helping VMs communicate with the outside world. More precisely, VMkernel interfaces provide network services to the ESXi host. Virtual machine external connectivity is provided through VM networking and virtual switch port groups.

### **Q31. What is Storage vMotion?**

**Answer:**

Storage vMotion is a VMware feature used to migrate the storage files of a running virtual machine from one datastore to another datastore.

During Storage vMotion, the VM's storage files are moved while the VM continues running.

The VM can remain on the same ESXi host during a storage-only migration.

**Example:**

Suppose a VM is using Datastore 1, but Datastore 1 is running out of space.

We can migrate the VM's virtual disk files from Datastore 1 to Datastore 2 using Storage vMotion without shutting down the VM.

### **Q32. What are the requirements for performing Storage vMotion?**

**Answer:**

The main requirements are:

1. Source and destination datastores must be accessible to the ESXi host performing the migration.
2. The destination datastore must have sufficient free space.
3. Source and destination storage must be compatible with the VM's storage configuration.
4. The ESXi host must have proper connectivity to both datastores.
5. The migration must satisfy the platform's storage compatibility requirements.

According to my notes, both datastores should be connected to the same ESXi host, and the destination datastore must have sufficient space.

### **Q33. What is XvMotion?**

**Answer:**

XvMotion is the combination of vMotion and Storage vMotion.

It allows us to migrate a powered-on virtual machine from one ESXi host to another ESXi host while also migrating its virtual machine files from one datastore to another datastore.

It combines two operations:

1. Host migration.
2. Storage migration.

This is useful when we want to change both the ESXi host and the datastore of a running virtual machine.

### **Q34. What is the difference between vMotion, Storage vMotion and XvMotion?**

**Answer:**

| Feature               | vMotion                                                            | Storage vMotion                  | XvMotion                   |
| --------------------- | ------------------------------------------------------------------ | -------------------------------- | -------------------------- |
| Main purpose          | Host migration                                                     | Storage migration                | Host and storage migration |
| VM location           | Moves to another ESXi host                                         | Usually remains on the same host | Moves to another ESXi host |
| VM storage            | Remains on the same datastore in standard shared-storage migration | Moves to another datastore       | Moves to another datastore |
| VM power state        | Powered on                                                         | Can be powered on                | Powered on                 |
| Memory transfer       | Yes                                                                | No host memory migration         | Yes                        |
| Storage file transfer | No in standard shared-storage vMotion                              | Yes                              | Yes                        |

### **Q35. What are the advantages and use cases of VM migration?**

**Answer:**

The main advantages and use cases of VM migration are:

**1. Load Balancing:**

If one ESXi host has high resource utilization, we can migrate VMs to another ESXi host with available resources.

**2. Hardware Maintenance:**

Before performing maintenance on a physical server, we can migrate the running VMs to another ESXi host.

**3. Storage Maintenance:**

Using Storage vMotion, we can move VM files from one datastore to another datastore.

**4. Resource Management:**

We can distribute virtual machines across ESXi hosts based on available resources.

**5. Datastore Space Management:**

When a datastore has insufficient free space, we can migrate VM storage files to another datastore with sufficient capacity.

# **Section 6 – Cluster, HA, DRS and Fault Tolerance**

### **Q36. What is a cluster in virtualization?**

**Answer:**

A cluster is a group of multiple ESXi hosts managed together as a single logical resource pool.

When we add multiple ESXi hosts to a cluster, their available CPU and memory resources contribute to the cluster's available resources.

A cluster helps us configure enterprise virtualization features such as:

- High Availability (HA).
- Distributed Resource Scheduler (DRS).
- Fault Tolerance (FT).

**Example:**

Suppose we have three ESXi hosts:

- ESXi Host 1
- ESXi Host 2
- ESXi Host 3

When we add all three hosts to a cluster, we can manage their resources collectively and configure HA and DRS.

### **Q37. What is High Availability (HA)?**

**Answer:**

HA stands for High Availability.

It is a VMware feature that helps recover virtual machines when an ESXi host fails.

When an ESXi host fails, HA identifies the failure and restarts the affected virtual machines on another available ESXi host in the cluster.

The main purpose of HA is to reduce service downtime and provide VM availability.

### **Q38. Explain how HA works in a VMware cluster.**

**Answer:**

HA works at the cluster level.

The working process is:

1. First, we create a cluster by adding multiple ESXi hosts.
2. We enable HA at the cluster level.
3. VMware installs FDM (Fault Domain Manager) agents on all ESXi hosts in the cluster.
4. These agents continuously exchange heartbeat information.
5. When one ESXi host stops sending heartbeats, the other hosts identify a possible host failure.
6. The cluster determines that the affected host is unavailable.
7. HA restarts the VMs from the failed host on another available ESXi host, provided sufficient resources and storage access are available.

**Example:**

Suppose ESXi Host 1, Host 2 and Host 3 are part of a cluster.

If Host 1 fails, HA identifies the failure and restarts its VMs on Host 2 or Host 3, depending on resource availability.

### **Q39. What are FDM agents, and how do ESXi hosts identify host failures?**

**Answer:**

FDM stands for Fault Domain Manager.

FDM agents are installed on ESXi hosts when we enable VMware HA.

These agents are responsible for monitoring host availability and coordinating HA operations.

**Working process:**

1. FDM agents run on the ESXi hosts in the cluster.
2. They exchange heartbeat messages with each other.
3. Each host monitors the availability of other hosts.
4. When a host stops sending heartbeats, the remaining hosts investigate whether it has failed or is experiencing a communication problem.
5. If a host failure is confirmed, HA coordinates the restart of affected VMs on available hosts.

### **Q40. What happens when an ESXi host fails in an HA-enabled cluster?**

**Answer:**

When an ESXi host fails in an HA-enabled cluster, the following process takes place:

1. FDM agents detect the host failure through heartbeat monitoring.
2. Other ESXi hosts in the cluster identify the failed host.
3. The HA mechanism determines which VMs were running on the failed host.
4. It selects another available ESXi host.
5. The VMs are restarted on the selected host.
6. Once restarted, the Guest OS and applications become available again.

**Important:** HA does not continue the failed VM's execution from the exact instruction where it stopped. It restarts the VM on another host. Therefore, some downtime is involved.

### **Q41. What are the requirements and disadvantages of HA?**

**Answer:**

**Requirements:**

1. There should be at least two ESXi hosts in the cluster.
2. HA must be enabled at the cluster level.
3. Sufficient CPU and memory resources should be available on the remaining ESXi hosts.
4. VM storage must be accessible to the destination ESXi hosts.
5. Proper network connectivity must be available between ESXi hosts.

**Disadvantages:**

The main disadvantage of HA is that VM downtime occurs because the virtual machines must restart on another ESXi host after a host failure.

Also, if the remaining cluster hosts do not have sufficient resources, all affected VMs might not be able to restart immediately.

### **Q42. What is Distributed Resource Scheduler (DRS)?**

**Answer:**

DRS stands for Distributed Resource Scheduler.

It is a VMware feature used to balance workloads across ESXi hosts in a cluster.

DRS monitors resource utilization across the cluster.

Whenever one ESXi host has a high workload and another host has available resources, DRS can migrate virtual machines from the heavily loaded host to another host using vMotion.

The main purpose of DRS is to maintain balanced resource utilization across the cluster.

### **Q43. How does DRS work?**

**Answer:**

DRS works by monitoring the resource utilization of ESXi hosts in a cluster.

The working process is:

1. We create a cluster by adding multiple ESXi hosts.
2. We enable DRS at the cluster level.
3. DRS monitors CPU and memory resource utilization across the ESXi hosts.
4. When an ESXi host experiences high resource utilization, DRS identifies the workload imbalance.
5. It identifies another ESXi host with available resources.
6. DRS recommends or automatically performs VM migration using vMotion, depending on the configured automation level.
7. The VMs are distributed across the hosts to balance the workload.

**Example:**

Suppose ESXi Host 1 has high CPU utilization, while ESXi Host 2 has available CPU resources.

DRS can migrate a VM from Host 1 to Host 2 using vMotion.

### **Q44. What are the advantages and requirements of DRS?**

**Answer:**

**Advantages:**

1. Automatically balances workloads across ESXi hosts.
2. Uses vMotion to migrate virtual machines.
3. Helps improve resource utilization.
4. Reduces resource imbalance across the cluster.
5. Helps maintain VM performance by distributing workloads.

**Requirements:**

1. Shared network connectivity.
2. Shared storage accessible to the required hosts.
3. Compatible CPUs on source and destination ESXi hosts.
4. VMkernel port group configured for vMotion.
5. Sufficient resources on destination ESXi hosts.
6. Datastores with sufficient free space.
7. At least two ESXi hosts in the cluster.
8. DRS enabled at the cluster level.

### **Q45. What is Fault Tolerance (FT)?**

**Answer:**

FT stands for Fault Tolerance.

It is a VMware feature that provides continuous availability for a virtual machine by maintaining a secondary copy of the VM on another ESXi host.

The two VM instances are:

1. Primary VM (Master VM).
2. Secondary VM (Shadow VM).

If the Primary VM or its host fails, the Secondary VM takes over as the new Primary VM.

Unlike HA, which restarts the VM after a failure, FT is designed to provide continuous VM execution without the normal reboot and restart process.

The main purpose of FT is to provide higher availability and reduce interruption during host failure.

### **Q46. Explain how Fault Tolerance works using Master VM and Shadow VM.**

**Answer:**

Fault Tolerance uses two virtual machine instances:

- Master VM.
- Shadow VM.

The Master VM runs on one ESXi host, and the Secondary or Shadow VM runs on another ESXi host.

The Secondary VM is kept synchronized with the Primary VM through Fault Tolerance mechanisms.

**Working process:**

1. We enable FT for the required virtual machine.
2. VMware creates a Secondary or Shadow VM on another ESXi host.
3. Both VM instances execute in a synchronized manner.
4. The Primary VM continues serving the workload.
5. If the Primary VM or its host fails, the Secondary VM takes over as the new Primary VM.
6. A new Secondary VM is created to restore FT protection.

**Important technical clarification:** Your notes describe the Shadow VM as being in an inactive state. More precisely, the FT Secondary VM is running in synchronization with the Primary VM; it is not simply a powered-off backup copy.

This is what allows FT to provide near-continuous execution when the Primary VM fails.

### **Q47. What are the requirements for enabling Fault Tolerance, and how do you enable it?**

**Answer:**

**Requirements:**

1. Shared storage must be available.
2. VMkernel networking must be configured for FT-related communication.
3. Source and destination ESXi hosts must have compatible CPUs.
4. Sufficient resources should be available on the destination ESXi host.
5. The hosts must support the selected FT configuration.
6. The VM must satisfy the FT compatibility requirements.

**Steps to enable FT according to my notes:**

1. Log in to vCenter/vSphere.
2. Select the required virtual machine.
3. Right-click on the VM.
4. Select Fault Tolerance.
5. Click Turn On Fault Tolerance.
6. Power on the VM as required by the configured workflow.
7. VMware creates the Secondary or Shadow VM on another ESXi host.

Your notes specifically mention powering off the VM before enabling FT.

**Additional clarification:** Exact prerequisites and activation steps depend on the vSphere version, FT configuration and VM compatibility. The above describes the basic workflow covered by your notes.

### **Q48. What is the difference between HA, DRS and FT?**

**Answer:**

| Feature           | HA                                    | DRS                                      | FT                                    |
| ----------------- | ------------------------------------- | ---------------------------------------- | ------------------------------------- |
| Full form         | High Availability                     | Distributed Resource Scheduler           | Fault Tolerance                       |
| Main purpose      | VM recovery after host failure        | Workload balancing                       | Continuous VM availability            |
| Working mechanism | Restarts affected VMs on another host | Uses vMotion to move VMs                 | Maintains a synchronized Secondary VM |
| Failure handling  | VM restart                            | Not primarily a failure-recovery feature | Secondary VM takes over               |
| Downtime          | Some downtime during VM restart       | Migration-related interruption may occur | Designed to avoid VM restart downtime |
| Configuration     | Cluster level                         | Cluster level                            | VM level                              |
| Main benefit      | VM recovery                           | Balanced resource utilization            | Continuous availability               |

**Interview conclusion:**

HA is used for VM recovery, DRS is used for workload balancing, and FT is used to provide continuous availability by maintaining a synchronized Secondary VM.

# **Section 7 – Snapshots, Clones and Templates**

### **Q49. What is a snapshot in virtualization?**

**Answer:**

A snapshot is a point-in-time representation of a virtual machine.

It captures the state of a VM at a particular point in time so that we can return to that state when required.

We use snapshots before performing activities such as:

- Software installation.
- Configuration changes.
- Testing.
- Operating system updates.
- Application changes.

For example, before installing a new application inside a VM, we can take a snapshot. If the installation causes an issue, we can revert to the previous snapshot.

### **Q50. What information does a snapshot capture, and how many snapshots can we take per VM according to your notes?**

**Answer:**

A snapshot captures the state of a virtual machine at a specific point in time.

It can include:

1. VM disk state.
2. VM configuration state.
3. VM memory state, when the memory snapshot option is selected.
4. VM power state information.

After creating a snapshot, VMware creates snapshot-related files in the datastore, including a `.vmsn` file for snapshot state information.

**Number of snapshots:**

According to my notes, we can take up to **32 snapshots per VM**.

The snapshot size can be smaller than the complete VM size because a snapshot generally tracks changes rather than creating a complete independent copy of all virtual disk data.

**Additional clarification:** The 32-snapshot limit should be understood in the context of the VMware version and snapshot-chain limits. It is not a recommendation to keep 32 snapshots active. Long snapshot chains can affect storage usage and performance.

### **Q51. What operations can we perform on snapshots? Explain the steps to create, revert and delete a snapshot.**

**Answer:**

We can perform three main operations on snapshots:

1. Take Snapshot.
2. Revert Snapshot.
3. Delete Snapshot.

**1. Steps to create a snapshot:**

1. Log in to vCenter/vSphere or the ESXi Host Client.
2. Select the required virtual machine.
3. Right-click on the VM.
4. Select Snapshots.
5. Click Take Snapshot.
6. Enter the snapshot name and description.
7. Select whether to include VM memory, if required.
8. Click Create.

**2. Steps to revert a snapshot:**

1. Log in to vCenter/vSphere.
2. Select the required virtual machine.
3. Open the Snapshot Manager.
4. Select the snapshot to which we want to revert.
5. Click Revert.
6. Confirm the operation.

The VM returns to the selected snapshot state.

**3. Steps to delete a snapshot:**

1. Log in to vCenter/vSphere.
2. Select the required virtual machine.
3. Open Snapshot Manager.
4. Select the snapshot that we want to delete.
5. Click Delete.
6. Confirm the operation.

**Important:** Deleting a snapshot does not mean deleting the current VM. VMware consolidates the snapshot changes into the base virtual disk as required.

### **Q52. What is a clone, and why do we use VM cloning?**

**Answer:**

A clone is an exact copy of an existing virtual machine at a particular point in time.

When we create a clone, VMware creates another VM with its own virtual machine configuration and virtual disk files.

We use cloning for:

1. Creating duplicate virtual machines.
2. Creating test environments.
3. Deploying multiple similar VMs.
4. Creating a separate copy for testing configuration changes.
5. Maintaining a separate VM instance based on an existing VM.

According to my notes, we can create a clone when the source VM is powered on or powered off.

**Example:**

Suppose we have one Linux VM and want to create three additional VMs with a similar configuration.

Instead of installing the OS and configuring everything separately, we can clone the existing VM.

### **Q53. What are the different types of cloning? Explain Hot Clone and Cold Clone.**

**Answer:**

There are two types of cloning mentioned in my notes.

**1. Cold Clone:**

Cold cloning means creating a clone when the source virtual machine is in a powered-off state.

**2. Hot Clone:**

Hot cloning means creating a clone when the source virtual machine is in a powered-on state.

| Feature         | Hot Clone                          | Cold Clone                  |
| --------------- | ---------------------------------- | --------------------------- |
| Source VM state | Powered on                         | Powered off                 |
| VM availability | Source VM continues running        | Source VM is stopped        |
| Usage           | When we want to clone a running VM | When downtime is acceptable |

**Additional clarification:** Hot cloning may require additional considerations to ensure that the copied operating system and application data are consistent. VMware's supported cloning workflow also depends on the selected vSphere version and VM configuration.

### **Q54. What are the steps to clone a virtual machine?**

**Answer:**

The steps to clone a virtual machine are:

1. Log in to vCenter/vSphere.
2. Select the required source virtual machine.
3. Right-click on the VM.
4. Select Clone.
5. Enter the name of the new virtual machine.
6. Select the target datastore.
7. Customize the virtual hardware if required.
8. Customize the Guest OS if required.
9. Select whether to power on the VM after creation.
10. Review the configuration.
11. Click Finish/Create.

After completing these steps, VMware creates a new virtual machine based on the source VM.

The cloned VM has its own virtual machine files and can be managed independently.

### **Q55. What is a VM template?**

**Answer:**

A VM template is a golden copy of an existing virtual machine.

It is used to create multiple virtual machines with a predefined configuration.

For example, suppose we have configured a Linux VM with all required operating system settings and applications.

We can convert that VM into a template and use it to deploy multiple virtual machines with the same base configuration.

According to my notes:

- A template is a golden copy of a VM.
- It is used to create multiple VMs.
- A template cannot be powered on directly like a normal VM.
- We use the Deploy Template option to create new virtual machines.

### **Q56. Why do we use templates, and what is the difference between a template and a clone?**

**Answer:**

We use templates to create multiple virtual machines with a predefined configuration.

Instead of creating and configuring every VM manually, we maintain a golden copy and deploy new VMs from it.

**Difference between Template and Clone:**

| Feature       | Template                                     | Clone                              |
| ------------- | -------------------------------------------- | ---------------------------------- |
| Meaning       | Golden copy of a VM                          | Duplicate copy of an existing VM   |
| Purpose       | Creating multiple VMs                        | Creating another VM                |
| Usage         | Repeated VM deployment                       | VM duplication and testing         |
| Power state   | Cannot be powered on directly as a normal VM | Can be powered on                  |
| Source        | Used as a deployment image                   | Created from an existing VM        |
| Configuration | Used as a standard base configuration        | Copies the source VM configuration |

According to my notes, templates use less space compared to clones.

**Additional clarification:** Actual storage consumption depends on the storage format, provisioning and cloning method. The main advantage of a template is standardized and repeatable VM deployment, rather than a guaranteed storage saving in every configuration.

### **Q57. What are the steps to convert a VM into a template and deploy multiple VMs using it?**

**Answer:**

We perform this operation using vCenter/vSphere.

**Part 1 – Convert a VM into a Template**

1. Log in to vCenter.
2. Navigate to the required ESXi host or cluster.
3. Select the virtual machine.
4. Right-click on the VM.
5. Select Template.
6. Select Convert to Template.
7. Confirm the operation.

Now the VM is converted into a template.

**Part 2 – Deploy Virtual Machines from the Template**

1. Log in to vCenter.
2. Select the required template.
3. Right-click on the template.
4. Select Deploy New VM from This Template.
5. Enter the new VM name.
6. Select the destination folder.
7. Select the target ESXi host or cluster.
8. Select the datastore.
9. Configure network and Guest OS customization settings if required.
10. Review the configuration.
11. Click Finish.

We can repeat the deployment process to create multiple virtual machines from the same template.

# **Section 8 – Virtual Networking**

### **Q58. What is a Virtual Switch, and why do we use it?**

**Answer:**

A Virtual Switch, also called vSwitch, is a software-based networking component used in VMware virtualization.

It provides network connectivity between virtual machines and external networks.

We use a virtual switch to:

1. Connect virtual machines to each other.
2. Connect virtual machines to external networks.
3. Connect virtual machine network interfaces to physical network interfaces.
4. Manage virtual machine network connectivity.

**Example:**

Suppose we have two virtual machines running on the same ESXi host.

If both VMs are connected to the same virtual switch and compatible network settings, they can communicate with each other through that virtual switch.

If they need external network connectivity, the virtual switch can use a physical network adapter, also called an uplink.

### **Q59. What are the different types of virtual switches? Explain Standard and Distributed Virtual Switches.**

**Answer:**

According to my notes, there are two types of virtual switches:

1. Standard Virtual Switch.
2. Distributed Virtual Switch.

**1. Standard Virtual Switch (vSS):**

A Standard Virtual Switch is configured on an individual ESXi host.

It is used to connect virtual machines running on that host and provide network connectivity.

It supports:

- VM-to-VM communication.
- Connectivity to external networks through physical network adapters.

**2. Distributed Virtual Switch (vDS):**

A Distributed Virtual Switch provides centralized virtual networking across multiple ESXi hosts.

It allows us to maintain consistent network configuration across different ESXi hosts.

It is used when we want virtual machines running on different ESXi hosts to communicate through a common distributed virtual networking configuration.

### **Q60. What is the difference between Standard Virtual Switch and Distributed Virtual Switch? How do VMs communicate with external networks and VMs on other ESXi hosts?**

**Answer:**

**Difference between Standard and Distributed Virtual Switches:**

| Feature               | Standard Virtual Switch                            | Distributed Virtual Switch                                     |
| --------------------- | -------------------------------------------------- | -------------------------------------------------------------- |
| Configuration         | Configured on an individual ESXi host              | Centrally managed across multiple ESXi hosts                   |
| Management            | Host-level management                              | Centralized management through vCenter                         |
| VM communication      | Supports communication between VMs connected to it | Supports consistent VM networking across multiple ESXi hosts   |
| Network configuration | Maintained separately on each ESXi host            | Shared configuration across participating hosts                |
| Usage                 | Suitable for individual ESXi host networking       | Suitable for multi-host enterprise virtualization environments |

**How VMs communicate with external networks:**

1. A VM has a Virtual NIC (vNIC).
2. The Virtual NIC is connected to a virtual switch.
3. The virtual switch is connected to a physical network adapter through an uplink.
4. The physical network adapter connects to the physical network switch.
5. Through this physical network infrastructure, the VM communicates with external systems.

**How VMs communicate across different ESXi hosts:**

Suppose:

- VM1 is running on ESXi Host 1.
- VM2 is running on ESXi Host 2.

Both VMs are connected to compatible network configurations.

The network traffic travels through the virtual switches, physical NICs and physical network infrastructure.

A Distributed Virtual Switch helps maintain consistent networking configuration across both ESXi hosts.

Therefore, VM1 and VM2 can communicate even though they are running on different physical ESXi hosts.

# **Virtualization – Final Completion Summary**


## **Important interview preparation notes**

There are a few distinctions worth retaining from this preparation:

- **vMotion:** Moves a running VM between ESXi hosts.
- **Storage vMotion:** Moves VM storage files between datastores.
- **XvMotion:** Combines host and storage migration.
- **HA:** Restarts VMs on another host after a host failure.
- **DRS:** Balances workloads across ESXi hosts.
- **FT:** Maintains a synchronized secondary VM for continuous availability.
- **Snapshot:** Captures a VM's point-in-time state.
- **Clone:** Creates a separate copy of an existing VM.
- **Template:** Acts as a golden copy for deploying multiple VMs.
- **Standard vSwitch:** Configured per ESXi host.
- **Distributed vSwitch:** Centrally managed across multiple ESXi hosts.

**Virtualization question bank: complete.**
