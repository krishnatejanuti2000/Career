# PROJECT 2 — ENTERPRISE NVMe SSD DRIVE QUALIFICATION
## 3–4 Years Experience — Interview + Real-World Validation Scope

---

# PROJECT OBJECTIVE

Build the ability to qualify an enterprise NVMe SSD across:

Physical Platform
→ PCIe
→ NVMe
→ Linux
→ Firmware
→ Functional Validation
→ Performance
→ Stress/Reliability
→ Power/Reset
→ Error Handling
→ Debugging/RCA
→ Automation
→ Regression
→ Final Drive Qualification

The goal is NOT to become a PCIe/NVMe protocol designer.

The goal is to become a strong:

- NVMe Validation Engineer
- SSD Validation Engineer
- Storage Validation Engineer
- Storage QA Automation Engineer
- System Validation Engineer
- Storage Performance Test Engineer
- Enterprise Drive Qualification Engineer


============================================================
01. PHYSICAL INSTALLATION & PLATFORM BRING-UP
============================================================

## 1.1 Enterprise Server Hardware

- Enterprise server architecture
- Motherboard
- CPU
- Memory
- PCIe root complex
- PCIe root ports
- PCIe slots
- NVMe backplane
- NVMe drive bays
- U.2/U.3 awareness
- EDSFF awareness
- Add-in-card NVMe awareness
- PCIe lane connectivity
- Drive slot mapping

## 1.2 NVMe Installation

- Physical drive installation
- Drive seating
- Drive replacement
- Hot-plug vs non-hot-plug
- Power delivery
- Thermal considerations

## 1.3 Platform Bring-Up

- BIOS/UEFI initialization
- BMC initialization
- Hardware inventory
- PCIe topology
- Drive inventory
- Firmware prerequisites
- Platform compatibility

## 1.4 Validation

- Pre-install baseline
- Post-install validation
- Expected drive visibility
- Slot-to-drive mapping
- Evidence collection

## 1.5 Troubleshooting

- Drive not detected
- Drive intermittently detected
- Wrong slot mapping
- Power issue
- Backplane issue
- Slot issue
- Thermal issue
- Platform compatibility issue


============================================================
02. PCIe ARCHITECTURE FOR NVMe
============================================================

## 2.1 PCIe Fundamentals

- Why NVMe uses PCIe
- PCI vs PCIe
- PCIe hierarchy
- Root Complex
- Root Port
- Endpoint
- PCIe Switch
- Bus / Device / Function
- BDF

## 2.2 PCIe Generations

- Gen1 awareness
- Gen2 awareness
- Gen3
- Gen4
- Gen5
- Gen6 awareness
- Backward compatibility
- Link speed negotiation

## 2.3 PCIe Lanes

- x1
- x2
- x4
- x8
- x16
- NVMe x4 relationship
- Lane negotiation
- Link width

## 2.4 PCIe Layers

- Transaction Layer
- Data Link Layer
- Physical Layer
- TLP
- DLLP
- Flow control

## 2.5 PCIe Configuration

- Configuration space
- Vendor ID
- Device ID
- Class Code
- Command register
- Status register
- BAR
- PCIe capabilities
- MSI/MSI-X
- AER

## 2.6 What Must Be Understood Deeply

- Root Complex → PCIe Endpoint
- PCIe link establishment
- Link speed
- Link width
- Configuration space
- BAR
- PCIe error reporting

Do NOT spend excessive time on PCIe protocol-design-level details.


============================================================
03. PCIe ENUMERATION & CONFIGURATION
============================================================

## 3.1 Enumeration

- BIOS enumeration
- OS enumeration
- PCIe bus scanning
- Bus number
- Device number
- Function number
- BDF
- PCIe hierarchy

## 3.2 Linux Commands

- `lspci`
- `lspci -nn`
- `lspci -vv`
- `lspci -t`
- `lspci -D`
- `setpci`
- `dmesg`
- `journalctl`

## 3.3 Configuration Space

- Vendor ID
- Device ID
- Class Code
- Command register
- Status register
- BAR
- Capability structures
- PCI Express capability
- AER capability
- MSI/MSI-X

## 3.4 Driver Binding

- PCI device
- PCI driver
- NVMe driver
- Driver binding
- Driver unbinding awareness

## 3.5 Validation

- Expected BDF
- Device visibility
- Link speed
- Link width
- Driver binding
- PCIe capability verification

## 3.6 Troubleshooting

- Device absent from `lspci`
- Wrong BDF
- BAR allocation issue
- Resource allocation issue
- Driver not bound
- Link not established


============================================================
04. PCIe DIAGNOSTICS
============================================================

## 4.1 PCIe Health

- Link state
- Link speed
- Link width
- Negotiated speed
- Negotiated width
- Link retraining
- Link instability

## 4.2 AER

- Advanced Error Reporting
- Correctable errors
- Non-fatal errors
- Fatal errors
- Receiver errors
- Bad TLP
- Bad DLLP
- Completion timeout
- Unsupported Request

## 4.3 Linux Diagnostics

- `lspci -vv`
- `dmesg`
- `journalctl`
- `/sys/bus/pci`
- PCIe sysfs information

## 4.4 Reset Awareness

- FLR
- Hot reset
- Bus reset
- Cold reset
- Relationship between PCIe reset and NVMe reset

## 4.5 Troubleshooting

- Link downgrade
- x4 → x2/x1
- Gen5 → Gen4/Gen3
- AER errors
- Device disappearance
- Intermittent PCIe failure

## 4.6 RCA

Determine whether the failure originates from:

- Hardware
- PCIe link
- BIOS
- Firmware
- Driver
- Power
- Thermal


============================================================
05. NVMe ARCHITECTURE
============================================================

## 5.1 NVMe Fundamentals

- Purpose of NVMe
- NVMe vs SATA
- NVMe vs SAS
- NVMe over PCIe
- NVMe over Fabrics awareness

## 5.2 NVMe Components

- Host
- PCIe
- NVMe Controller
- Namespace
- Submission Queue
- Completion Queue
- Admin Queue
- I/O Queues

## 5.3 Controller

- Controller identification
- Controller registers
- Controller capabilities
- Controller status
- Controller configuration

## 5.4 Important Registers

- CAP
- VS
- CC
- CSTS
- AQA
- ASQ
- ACQ
- Doorbells

## 5.5 Core Concepts

- DMA
- Doorbell
- Interrupt
- Polling
- Queue pair
- Command
- Completion

## 5.6 Required Mental Model

Host
→ PCIe
→ NVMe Controller
→ Submission Queue
→ Command
→ SSD processing
→ Completion Queue
→ Host


============================================================
06. NVMe DETECTION & INITIALIZATION
============================================================

## 6.1 Complete Detection Flow

Physical Drive
→ PCIe Link
→ PCIe Enumeration
→ NVMe PCI Endpoint
→ NVMe Driver
→ Controller Initialization
→ Identify Controller
→ Namespace Discovery
→ Linux Block Device

## 6.2 Linux NVMe Driver

- NVMe driver
- Driver binding
- Controller initialization
- Controller reset
- Namespace registration
- Block device registration

## 6.3 Commands

- `lspci`
- `nvme list`
- `nvme id-ctrl`
- `nvme id-ns`
- `lsblk`
- `blkid`
- `dmesg`
- `journalctl`

## 6.4 sysfs

- `/sys/class/nvme`
- `/sys/class/block`
- `/sys/bus/pci`
- `/sys/bus/pci/drivers/nvme`

## 6.5 Detection Troubleshooting

### Not visible in BIOS/BMC

Investigate:

- Physical installation
- Slot
- Backplane
- Power
- Platform support

### BIOS sees it but OS does not

Investigate:

- PCIe enumeration
- BIOS configuration
- OS
- Kernel
- Driver

### `lspci` sees it but NVMe does not

Investigate:

- NVMe driver
- Controller initialization
- Firmware
- Kernel logs

### Controller exists but namespace does not

Investigate:

- Namespace configuration
- Firmware
- Controller state

### Namespace exists but block device does not

Investigate:

- Driver
- Block layer
- OS state


============================================================
07. NVMe COMMAND MODEL
============================================================

## 7.1 Command Structure

- Opcode
- Command Identifier
- Namespace ID
- Command-specific fields
- Metadata
- PRP
- SGL
- Status

## 7.2 Command Categories

### Admin Commands

- Identify
- Get Log Page
- Get Features
- Set Features
- Firmware Download
- Firmware Commit
- Device Self-Test
- Format NVM
- Namespace Management awareness

### I/O Commands

- Read
- Write
- Flush
- Dataset Management
- Write Zeroes
- Compare awareness

## 7.3 Command Flow

Host
→ Build command
→ Submission Queue
→ Doorbell
→ Controller
→ Execute
→ Completion Queue
→ Completion status

## 7.4 Validation

For every important command understand:

- Purpose
- Inputs
- Preconditions
- Expected output
- Status
- Failure conditions
- Recovery


============================================================
08. SUBMISSION / COMPLETION QUEUES
============================================================

## 8.1 Queue Concepts

- Submission Queue
- Completion Queue
- Admin Queue
- I/O Queue
- Queue pair

## 8.2 Queue Mechanics

- Queue creation
- Queue deletion
- Queue depth
- Head
- Tail
- Doorbell
- Phase bit
- Completion entry
- Interrupt
- MSI-X
- Polling

## 8.3 Performance Relationship

- Queue depth
- Parallelism
- IOPS
- Latency
- CPU utilization

## 8.4 Troubleshooting

- Queue creation failure
- Queue full
- Completion timeout
- Stalled queue
- I/O timeout
- Controller reset


============================================================
09. ADMIN COMMAND VALIDATION
============================================================

## 9.1 Identification

- Identify Controller
- Identify Namespace
- Identify Namespace List

## 9.2 Features

- Get Features
- Set Features
- Supported values
- Invalid values

## 9.3 Logs

- SMART / Health
- Error Information
- Firmware information
- Supported logs
- Telemetry awareness

## 9.4 Firmware Commands

- Firmware Download
- Firmware Commit

## 9.5 Other Important Commands

- Device Self-Test
- Format NVM
- Abort
- Namespace operations awareness

## 9.6 Negative Testing

- Invalid opcode
- Invalid NSID
- Invalid field
- Invalid parameter
- Unsupported feature
- Invalid state

## 9.7 Validation Pattern

Precondition
→ Execute Command
→ Check Status
→ Validate Response
→ Check Side Effects
→ Verify Recovery


============================================================
10. I/O COMMAND VALIDATION
============================================================

## 10.1 Core I/O

- Read
- Write
- Flush
- Write Zeroes
- Dataset Management
- Compare awareness

## 10.2 I/O Concepts

- LBA
- Block size
- Transfer size
- Queue depth
- Sequential I/O
- Random I/O
- Read/write mix

## 10.3 Functional Tests

- Single-block read/write
- Multi-block read/write
- First LBA
- Last valid LBA
- Boundary LBA
- Large transfer
- Small transfer
- Invalid LBA

## 10.4 Data Validation

- Known patterns
- Random patterns
- Write → Read → Compare
- Data persistence

## 10.5 Error Testing

- Invalid LBA
- Namespace unavailable
- Command timeout
- Media error
- Controller reset during I/O


============================================================
11. NVMe NAMESPACES
============================================================

## 11.1 Namespace Concepts

- Namespace
- NSID
- Namespace size
- Namespace capacity
- Namespace utilization

## 11.2 Namespace Operations

- Create
- Delete
- Attach
- Detach
- Format
- Identify

## 11.3 LBA Format

- Logical block size
- Metadata
- Supported LBA formats
- Formatting impact

## 11.4 Linux

- `nvme list`
- `nvme id-ns`
- `lsblk`
- `blkid`

## 11.5 Validation

- Single namespace
- Multiple namespaces
- Namespace isolation
- Namespace I/O
- Namespace attach/detach
- Namespace formatting


============================================================
12. NVMe HEALTH & TELEMETRY
============================================================

## 12.1 Health Information

- Critical warnings
- Temperature
- Available spare
- Available spare threshold
- Percentage used
- Data units read
- Data units written
- Host reads
- Host writes
- Power cycles
- Power-on hours
- Unsafe shutdowns
- Media/data integrity errors

## 12.2 Commands

- `nvme smart-log`
- `nvme error-log`
- `nvme get-log`

## 12.3 Telemetry

- Telemetry concept
- Log pages
- Controller telemetry
- Host-initiated telemetry
- Diagnostic collection

## 12.4 Validation

Capture baseline health and compare after:

- Stress
- Firmware update
- Reset
- Power cycle
- Error injection

## 12.5 Troubleshooting

Correlate:

- SMART
- Error log
- dmesg
- PCIe AER
- BMC SEL


============================================================
13. FIRMWARE VALIDATION
============================================================

## 13.1 Firmware Fundamentals

- Firmware version
- Firmware image
- Firmware slots
- Active firmware
- Firmware activation

## 13.2 Firmware Lifecycle

- Download
- Commit
- Activation
- Reset
- Reboot
- Power cycle

## 13.3 Core Tests

- Firmware upgrade
- Firmware downgrade
- Repeated upgrade
- Invalid firmware
- Wrong firmware
- Interrupted update
- Activation behavior

## 13.4 Post-Update Validation

- Firmware version
- Drive detection
- Controller availability
- Namespace availability
- Data integrity
- Health
- Performance
- Error logs

## 13.5 Failure Scenarios

- Firmware update failure
- Drive disappearance
- Controller not ready
- Failed activation
- Recovery after failed activation


============================================================
14. FEATURE VALIDATION
============================================================

## 14.1 Important Features

- Power management
- Number of queues
- Interrupt configuration awareness
- Arbitration awareness
- APST awareness
- Volatile write cache
- Dataset management
- LBA formats
- Protection information awareness

## 14.2 Validation

- Default value
- Supported value
- Unsupported value
- Boundary value
- Get feature
- Set feature
- Persistence
- Reset behavior
- Reboot behavior

## 14.3 Avoid

Do not spend excessive time memorizing every NVMe feature identifier.

Focus on features relevant to actual validation work.


============================================================
15. RESET & RECOVERY
============================================================

## 15.1 Reset Types

- NVMe controller reset
- PCIe FLR
- PCIe hot reset
- Bus reset
- System reboot
- Power cycle

## 15.2 Understand

- What gets reset
- Controller state
- Queue state
- Namespace state
- Driver behavior
- Recovery behavior

## 15.3 Tests

- Reset while idle
- Reset during read
- Reset during write
- Reset under FIO load
- Repeated resets

## 15.4 Validation

- Controller returns
- Namespace returns
- Block device returns
- I/O resumes
- No data corruption
- Error logs checked

## 15.5 Recovery Metrics

- Recovery time
- Detection time
- Namespace recovery
- I/O recovery


============================================================
16. POWER MANAGEMENT
============================================================

## 16.1 PCIe Power

- ASPM
- L0
- L0s
- L1
- L1 substates awareness

## 16.2 NVMe Power

- NVMe power states
- Active state
- Idle state
- APST

## 16.3 Validation

- Idle
- Active
- Power transition
- Long idle
- Resume
- Reboot
- Power cycle

## 16.4 Observe

- Device accessibility
- Latency
- Performance
- Temperature
- Recovery


============================================================
17. BIOS / UEFI VALIDATION
============================================================

## 17.1 Important Settings

- PCIe slot configuration
- PCIe generation
- Lane configuration
- Bifurcation awareness
- Above 4G decoding
- Hot plug
- NVMe boot support

## 17.2 Validation

- NVMe visibility
- Slot enable/disable
- Link generation
- Link width
- Boot behavior
- Configuration persistence

## 17.3 Troubleshooting

- BIOS sees / OS doesn't
- OS sees / BIOS doesn't
- Boot failure
- Configuration mismatch
- Firmware compatibility


============================================================
18. BMC / SEL VALIDATION
============================================================

## 18.1 BMC

- Hardware inventory
- Storage inventory
- PCIe inventory
- NVMe inventory
- Sensor monitoring

## 18.2 SEL

- System Event Log
- Event severity
- Timestamp
- Event source
- Event correlation

## 18.3 NVMe-Related Events

- Drive failure
- PCIe error
- Temperature event
- Power event
- Firmware event

## 18.4 Validation

Fault
→ OS logs
→ BMC
→ SEL
→ Correlate timestamps
→ Determine source

## 18.5 Troubleshooting

- BMC sees / OS doesn't
- OS sees / BMC doesn't
- Incorrect inventory
- Missing event
- Incorrect event


============================================================
19. COMPATIBILITY VALIDATION
============================================================

## 19.1 Compatibility Dimensions

- Drive
- Drive firmware
- Server
- Motherboard
- PCIe slot
- Backplane
- BIOS
- BMC
- OS
- Kernel
- NVMe driver

## 19.2 Compatibility Matrix

Drive
× Firmware
× Server
× BIOS
× BMC
× OS
× Driver

## 19.3 Testing

- Supported combinations
- Unsupported combinations
- Firmware combinations
- OS combinations
- BIOS combinations
- Driver combinations

## 19.4 Important Skill

Learn how to design a compatibility matrix rather than memorizing one.


============================================================
20. FUNCTIONAL VALIDATION
============================================================

## 20.1 Core Functions

- Detection
- Initialization
- Identify
- Namespace
- Read
- Write
- Flush
- Format

## 20.2 Functional Areas

- Admin commands
- I/O commands
- Namespace
- Firmware
- Health
- Power management
- Reset
- Recovery

## 20.3 Negative Testing

- Invalid command
- Invalid parameter
- Boundary condition
- Unsupported feature
- Invalid state

## 20.4 Regression

Validate functionality after:

- Firmware change
- Driver change
- BIOS change
- OS/kernel change
- Platform change


============================================================
21. PERFORMANCE / FIO
============================================================

## 21.1 Performance Metrics

- IOPS
- Throughput
- Bandwidth
- Latency
- Average latency
- Tail latency
- CPU utilization

## 21.2 Workloads

- Sequential read
- Sequential write
- Random read
- Random write
- Mixed read/write

## 21.3 Important Parameters

- Block size
- Queue depth
- Number of jobs
- Runtime
- Ramp time
- Direct I/O
- ioengine

## 21.4 FIO

Learn:

- Job file
- `--rw`
- `--bs`
- `--iodepth`
- `--numjobs`
- `--runtime`
- `--ramp_time`
- `--direct`
- `--ioengine`

## 21.5 Test Method

Baseline
→ Warm-up
→ Steady-state workload
→ Measure
→ Compare
→ Analyze

## 21.6 Analysis

- IOPS
- MB/s
- Latency
- p95
- p99
- CPU
- Queue depth
- Temperature

## 21.7 Troubleshooting

- Low IOPS
- High latency
- Low throughput
- Performance fluctuation
- Thermal throttling
- CPU bottleneck
- PCIe link downgrade


============================================================
22. STRESS / RELIABILITY
============================================================

## 22.1 Stress Types

- Long-duration I/O
- High queue depth
- Mixed workload
- Repeated reset
- Repeated reboot
- Power cycling
- Firmware cycles

## 22.2 Reliability

- Soak testing
- Stability
- Endurance awareness
- Error accumulation
- Recovery behavior

## 22.3 Monitor

- SMART
- Error log
- dmesg
- PCIe AER
- BMC SEL
- Temperature
- Performance

## 22.4 Failure Analysis

- First failure
- Reproducibility
- Failure frequency
- Correlation
- Recovery
- Data integrity


============================================================
23. POWER CYCLE / REBOOT VALIDATION
============================================================

## 23.1 Scenarios

- Normal reboot
- Warm reboot
- Cold boot
- Hard reset
- Power cycle

## 23.2 Test Conditions

- Idle
- Read
- Write
- Heavy FIO
- Firmware state

## 23.3 Validate

- Device detection
- Controller initialization
- Namespace availability
- Data persistence
- Health
- Error log
- Performance

## 23.4 Failures

- Device disappears
- Namespace missing
- Data corruption
- Slow initialization
- Firmware recovery failure
- PCIe enumeration failure


============================================================
24. DATA INTEGRITY
============================================================

## 24.1 Core Concepts

- Data corruption
- Data consistency
- Persistence
- Read-after-write
- Write verification

## 24.2 Test Patterns

- Known pattern
- Random data
- Zero pattern
- Sequential data

## 24.3 Core Tests

Write
→ Read
→ Compare

Write
→ Power Cycle
→ Read
→ Compare

Write
→ Reset
→ Read
→ Compare

Write
→ Firmware Update
→ Read
→ Compare

Stress
→ Read
→ Compare

## 24.4 Boundary Tests

- First LBA
- Last LBA
- Namespace boundary
- Small transfer
- Large transfer

## 24.5 Failures

- Miscompare
- Corruption
- Lost data
- Partial write
- Unexpected data


============================================================
25. ERROR INJECTION
============================================================

## 25.1 Purpose

Validate:

- Error detection
- Error reporting
- Logging
- Recovery
- Data integrity

## 25.2 Error Categories

- PCIe errors
- AER errors
- Invalid commands
- Invalid parameters
- I/O errors
- Timeout
- Controller reset
- Namespace errors
- Power interruption

## 25.3 Error Injection Flow

Inject
→ Detect
→ Log
→ Report
→ Recover
→ Validate Data

## 25.4 Evidence

- dmesg
- journalctl
- NVMe error log
- PCIe AER
- BMC SEL
- FIO/application result

## 25.5 Important Skill

Understand what failure you are intentionally creating and what behavior you expect from:

- Drive
- Firmware
- Controller
- Driver
- OS
- BMC


============================================================
26. ERROR DEBUGGING / RCA
============================================================

## 26.1 Debugging Method

Reproduce
→ Collect Evidence
→ Isolate Layer
→ Form Hypothesis
→ Test Hypothesis
→ Identify Root Cause
→ Verify Fix
→ Regression

## 26.2 Debugging Layers

Application
↓
Filesystem
↓
Block Layer
↓
NVMe Driver
↓
NVMe Controller
↓
PCIe
↓
Firmware
↓
Hardware

## 26.3 Evidence

- `dmesg`
- `journalctl`
- `lspci`
- `nvme`
- SMART
- NVMe error log
- PCIe AER
- BMC SEL
- FIO output
- Protocol analyzer

## 26.4 Common Failures

- NVMe missing
- PCIe link downgrade
- Controller reset
- I/O timeout
- Namespace missing
- Firmware failure
- Data miscompare
- Thermal throttling
- Performance degradation

## 26.5 RCA Structure

- Symptom
- Impact
- Environment
- Reproduction
- Timeline
- Evidence
- Suspected layer
- Root cause
- Workaround
- Fix
- Verification
- Regression


============================================================
27. PROTOCOL ANALYZER / LECROY
============================================================

## 27.1 Why Use a Protocol Analyzer?

Use it when OS-level evidence is insufficient to determine what is happening on the PCIe link.

## 27.2 Learn

- PCIe traffic capture
- Link training
- TLP
- DLLP
- Configuration transactions
- Memory transactions
- Completion
- Retries
- PCIe errors
- Reset sequence

## 27.3 Debugging

- Enumeration failure
- Link training failure
- Completion timeout
- Unsupported Request
- PCIe protocol errors

## 27.4 Analyzer Workflow

Capture
→ Filter
→ Decode
→ Identify failure
→ Correlate timestamp
→ Compare with OS logs

## 27.5 Correlation

Protocol Analyzer
+
dmesg
+
PCIe AER
+
NVMe error log
+
BMC SEL

## 27.6 Scope

Learn enough to analyze and explain captures.

Do NOT spend excessive time becoming a PCIe protocol-analyzer specialist.


============================================================
28. PYTHON — NVMe VALIDATION AUTOMATION
============================================================

## 28.1 Python Fundamentals Required

- Variables
- Data types
- Conditions
- Loops
- Functions
- Arguments
- `*args`
- `**kwargs`
- Lists
- Tuples
- Dictionaries
- Sets
- Strings
- File handling
- Exceptions
- OOP
- Modules
- Packages

## 28.2 System Automation

- Execute Linux commands
- Capture stdout
- Capture stderr
- Return codes
- Timeout handling
- Process execution

## 28.3 NVMe Automation

Automate:

- `nvme list`
- `nvme id-ctrl`
- `nvme id-ns`
- `nvme smart-log`
- `nvme error-log`
- `lspci`
- `lsblk`
- `dmesg`

## 28.4 Parsing

- Text parsing
- JSON parsing
- Regex
- Log parsing

## 28.5 Validation Automation

Execute
→ Capture
→ Parse
→ Validate
→ Report

## 28.6 Error Handling

- Command failure
- Timeout
- Device missing
- Permission error
- Unexpected output

## 28.7 Storage Automation Design

- Reusable functions
- Utilities
- Configuration
- Logging
- Reporting
- Result collection

## 28.8 Do NOT Overstudy

- Web development
- GUI development
- Data science
- Machine learning
- Advanced algorithms unrelated to automation


============================================================
29. PYTEST VALIDATION
============================================================

## 29.1 Fundamentals

- Test discovery
- Test functions
- Assertions
- Fixtures
- Parameterization
- Markers
- Setup
- Teardown

## 29.2 Storage Test Structure

tests/
├── test_detection.py
├── test_health.py
├── test_firmware.py
├── test_namespace.py
├── test_io.py
├── test_reset.py
└── test_performance.py

## 29.3 Fixtures

- NVMe device
- Namespace
- Test environment
- Setup
- Cleanup

## 29.4 Parameterization

- Different drives
- Firmware versions
- Namespaces
- Block sizes
- Queue depths

## 29.5 Assertions

- Device detected
- Firmware version
- Namespace count
- Health values
- Command status
- Data integrity

## 29.6 Test Reporting

- Pass
- Fail
- Error
- Skip
- Logs
- Evidence

## 29.7 Important Advanced Topics

- `conftest.py`
- Custom markers
- Hooks awareness
- Parallel execution awareness
- Plugin awareness

## 29.8 Failure Classification

- Product failure
- Test failure
- Automation failure
- Environment failure
- Infrastructure failure


============================================================
30. GIT / JENKINS / REGRESSION / CI
============================================================

## 30.1 Git

- Repository
- Branch
- Commit
- Push
- Pull
- Merge
- Pull Request
- Tag
- Revert
- Conflict resolution

## 30.2 Testing Types

- Smoke
- Sanity
- Functional regression
- Full regression
- Release regression

## 30.3 Jenkins / CI

- Pipeline
- Build
- Environment setup
- Test execution
- Artifact
- Logs
- Reports
- Notifications

## 30.4 Storage Validation Pipeline

Code
→ Build
→ Environment Setup
→ Drive Detection
→ Pytest
→ Functional Tests
→ Performance Tests
→ Reports

## 30.5 Regression Triggers

- Firmware change
- Driver change
- BIOS change
- OS/kernel change
- Platform change
- Drive change

## 30.6 Failure Classification

- Product defect
- Automation defect
- Environment failure
- Infrastructure failure
- Configuration issue


============================================================
31. ENTERPRISE DRIVE QUALIFICATION
============================================================

## 31.1 Qualification Fundamentals

- Drive qualification
- Platform qualification
- Compatibility qualification
- Release qualification

## 31.2 Qualification Inputs

- Drive model
- Firmware
- Capacity
- Form factor
- PCIe generation
- Server
- BIOS
- BMC
- OS
- Driver

## 31.3 Qualification Areas

- Physical installation
- PCIe
- Detection
- NVMe
- Admin commands
- I/O
- Namespace
- Health
- Firmware
- Features
- Reset
- Power
- BIOS
- BMC
- Compatibility
- Functional validation
- Performance
- Stress
- Power cycle
- Data integrity
- Error injection
- Debugging

## 31.4 Qualification Matrix

Drive
× Firmware
× Server
× BIOS
× BMC
× OS
× Driver
× Workload

## 31.5 Entry Criteria

- Hardware ready
- Platform ready
- Firmware available
- OS ready
- Driver ready
- Test environment ready

## 31.6 Exit Criteria

- Functional tests passed
- Compatibility validated
- Performance validated
- Stress completed
- Data integrity validated
- Error recovery validated
- Critical issues resolved or formally accepted
- Required evidence collected

## 31.7 Defect Lifecycle

Failure
→ Reproduce
→ Collect evidence
→ Log defect
→ RCA
→ Fix
→ Verify
→ Regression

## 31.8 Final Qualification Report

- Environment
- Drive details
- Firmware
- Platform
- OS
- Test coverage
- Results
- Failures
- RCA
- Known issues
- Qualification conclusion


============================================================
FINAL PRIORITY
============================================================

## VERY DEEP — CORE INTERVIEW + JOB SKILLS

03. PCIe Enumeration & Configuration
04. PCIe Diagnostics
05. NVMe Architecture
06. NVMe Detection & Initialization
07. NVMe Command Model
08. Submission / Completion Queues
09. Admin Command Validation
10. I/O Command Validation
12. NVMe Health & Telemetry
13. Firmware Validation
15. Reset & Recovery
19. Compatibility Validation
21. Performance / FIO
22. Stress / Reliability
24. Data Integrity
26. Error Debugging / RCA


## DEEP — IMPORTANT SUPPORTING SKILLS

01. Physical Installation & Platform Bring-Up
02. PCIe Architecture
11. NVMe Namespaces
14. Feature Validation
16. Power Management
17. BIOS / UEFI Validation
18. BMC / SEL Validation
20. Functional Validation
23. Power Cycle / Reboot
25. Error Injection
27. Protocol Analyzer / LeCroy
28. Python NVMe Automation
29. Pytest Validation
31. Enterprise Drive Qualification


## STRONG WORKING KNOWLEDGE

30. Git / Jenkins / Regression / CI



============================================================
THE ENGINEER WE ARE BUILDING
============================================================

By the end of Project 2 preparation, the target capability is:

"Give me an enterprise NVMe SSD, a server platform,
Linux, firmware and a workload.

I should be able to:

1. Install the drive.
2. Verify platform readiness.
3. Trace PCIe enumeration.
4. Verify NVMe detection.
5. Understand controller initialization.
6. Validate namespaces.
7. Execute and validate admin commands.
8. Validate I/O.
9. Validate health.
10. Validate firmware.
11. Validate features.
12. Test reset/recovery.
13. Test power behavior.
14. Validate BIOS/BMC interaction.
15. Test compatibility.
16. Run functional validation.
17. Run FIO performance tests.
18. Run stress/reliability tests.
19. Perform power-cycle testing.
20. Validate data integrity.
21. Inject errors.
22. Debug failures.
23. Perform RCA.
24. Automate tests using Python.
25. Build Pytest tests.
26. Run regression through CI.
27. Produce a final qualification result."


============================================================
MASTER DEBUGGING MODEL
============================================================

Whenever a failure occurs, think:

Physical
  ↓
Power
  ↓
BIOS/BMC
  ↓
PCIe Link
  ↓
PCIe Enumeration
  ↓
NVMe Driver
  ↓
NVMe Controller
  ↓
Namespace
  ↓
Block Layer
  ↓
I/O
  ↓
Firmware
  ↓
Performance
  ↓
Data Integrity


============================================================
MASTER PROJECT 2 FLOW
============================================================

Physical Installation
        ↓
Platform Bring-Up
        ↓
BIOS / BMC
        ↓
PCIe Architecture
        ↓
PCIe Enumeration
        ↓
PCIe Diagnostics
        ↓
NVMe Architecture
        ↓
NVMe Detection
        ↓
Controller Initialization
        ↓
NVMe Commands
        ↓
Submission / Completion Queues
        ↓
Namespaces
        ↓
Health / Telemetry
        ↓
Firmware
        ↓
Features
        ↓
Reset / Recovery
        ↓
Power Management
        ↓
Compatibility
        ↓
Functional Validation
        ↓
Performance
        ↓
Stress / Reliability
        ↓
Power Cycle
        ↓
Data Integrity
        ↓
Error Injection
        ↓
Debugging / RCA
        ↓
Protocol Analyzer
        ↓
Python Automation
        ↓
Pytest
        ↓
CI / Regression
        ↓
ENTERPRISE DRIVE QUALIFICATION
