

### Split 3

# SPLIT 3 — VALIDATION, PERFORMANCE, HEALTH, FIRMWARE, TROUBLESHOOTING, AUTOMATION & PROJECT APPLICATION

## Objective

Convert the Storage knowledge from Splits 1 and 2 into enterprise testing, validation, performance analysis, diagnostics, troubleshooting, RCA, automation and project capability.

## Recommended Position

Days 61–90 of the 90-day preparation, adjusted by actual mastery.

---

# MODULE 31 — STORAGE TESTING & VALIDATION TYPES

## Topics

- Functional Testing
- Sanity Testing
- Regression Testing
- Integration Testing
- System Testing
- Compatibility Testing
- Interoperability Testing
- Negative Testing
- Boundary Testing
- Performance Testing
- Stress Testing
- Soak Testing
- Endurance Testing
- Reliability Testing
- Recovery Testing
- Failover Testing
- Failback Testing
- Upgrade Validation
- Downgrade Validation
- Rollback Validation
- Data Integrity Testing
- Failure Injection
- Defect Verification
- Qualification Testing
- Release Qualification

---

# MODULE 32 — ENTERPRISE TEST DESIGN

## Topics

- Product Lifecycle
- Release Lifecycle
- Requirement Analysis
- Feature Analysis
- Risk Analysis
- Verification vs Validation vs Testing
- Test Strategy
- Test Plan
- Test Case
- Test Scenario
- Test Matrix
- Test Coverage
- Entry Criteria
- Exit Criteria
- Pass / Fail Criteria
- Validation Evidence
- Release Sign-Off

## Enterprise Activities

- Requirement → Validation Objective
- Feature → Test Coverage
- Test Case Design
- Test Matrix Development
- Pass / Fail Definition
- Failure Classification
- Release Readiness

---

# MODULE 33 — STORAGE HEALTH & DRIVE DIAGNOSTICS

## Topics

- SMART
- NVMe SMART
- smartctl
- nvme-cli
- Temperature
- Wear
- SSD Endurance
- Media Errors
- Critical Warnings
- Error Counters
- Health Threshold Validation
- Bad Blocks
- Predictive Failure Analysis
- Unsafe Shutdowns
- Power-Cycle Counters
- Telemetry Concepts

## Diagnostic Tools

- smartctl
- nvme-cli
- storcli
- dmesg
- Linux System Logs
- Controller Logs
- Storage Logs

## Goal

Collect and interpret defensible drive-health evidence.

---

# MODULE 34 — STORAGE FIRMWARE VALIDATION

## Topics

- Firmware Architecture at Validation Depth
- Firmware Release Changes
- Feature Impact Analysis
- Front-End Behavior
- Back-End Behavior
- Error Handling
- Power-Loss Considerations
- Firmware Regression

## Lifecycle Validation

- Baseline
- Upgrade
- Activation
- Verification
- Downgrade
- Rollback
- Recovery
- Compatibility
- Post-Upgrade Verification
- Functional Regression
- Performance Regression

## Failure Scenarios

- Firmware-Induced Failure
- Firmware-Induced Performance Regression
- Recovery After Firmware Operation
- Firmware / Driver Interoperability Failure

---

# MODULE 35 — STORAGE PERFORMANCE ENGINEERING

## Fundamentals

- IOPS
- Throughput
- Bandwidth
- Latency
- Average Latency
- Percentile Latency
- Tail Latency
- Queue Depth
- Block Size
- Sequential I/O
- Random I/O
- Mixed Workloads
- CPU Utilization
- Device Utilization
- Saturation
- Cache Hit Ratio

---

# MODULE 36 — FIO & PERFORMANCE TOOLS

## FIO

- Job Structure
- rw
- bs
- iodepth
- numjobs
- runtime
- Ramp Time
- direct
- ioengine
- Job Files

## Other Tools

- fio
- dd
- ioping
- bonnie++

## System Evidence

- iostat
- vmstat
- sar
- mpstat
- iotop
- pidstat

---

# MODULE 37 — PERFORMANCE TEST METHODOLOGY

## Topics

- Baseline
- Controlled Variables
- Warm-Up
- Steady State
- Repeatability
- Workload Design
- Comparison
- Regression Detection

## Enterprise Scenarios

- Performance Below Specification
- Latency Regression
- IOPS Regression
- Firmware Performance Regression
- Degraded RAID Performance
- Performance During Rebuild
- VM Storage Performance Degradation
- Multi-Path Performance Behavior

---

# MODULE 38 — PERFORMANCE BOTTLENECK ISOLATION

Trace performance problems through:

```text
Application
→ VM
→ Hypervisor
→ Host
→ CPU / Memory
→ Filesystem
→ Block Layer
→ Driver
→ PCIe / Network
→ Controller / Array
→ RAID / Pool
→ SSD
```

## Assessment

Given a performance problem, isolate the likely bottleneck layer using evidence rather than guessing.

---

# MODULE 39 — RELIABILITY / ENDURANCE VALIDATION

## Topics

* Stress Testing
* Endurance Testing
* Soak Testing
* Burn-In
* Long-Duration I/O
* Reliability Validation
* Recovery Validation
* Power Cycle Testing
* Hot Plug Validation
* Fault Injection

## SSD-Focused

* Endurance
* Wear
* Sustained Write
* Thermal Behavior
* Media Errors
* Garbage Collection Effects

---

# MODULE 40 — HIGH AVAILABILITY & PLATFORM VALIDATION

## Validate

* Dual Controllers
* Controller Failover
* Controller Failback
* Controller Reboot
* Power Cycle
* Power Supply Failure
* Network Port Failure
* Path Failure
* Redundancy
* Uninterrupted Availability

---

# MODULE 41 — HOST CONNECTIVITY VALIDATION

## Validate

* Fibre Channel
* iSCSI
* Multipathing
* Path Failover
* Host Discovery
* Device Rescan
* Connectivity Recovery

---

# MODULE 42 — DRIVE QUALIFICATION & COMPATIBILITY

## Qualification

* HDD Qualification
* SATA SSD Qualification
* SAS SSD Qualification
* NVMe SSD Qualification
* Vendor Qualification
* Capacity Qualification
* Interface Validation
* Drive Discovery
* Device Enumeration

## Compatibility

* Controller Compatibility
* Backplane Compatibility
* PCIe Lane Validation
* Firmware Compatibility
* Operating System Compatibility
* Driver Compatibility
* Mixed Drive Validation
* Platform Compatibility Matrix

---

# MODULE 43 — DRIVE / STORAGE SYSTEM INTEGRATION

## Validate

* RAID Integration
* RAID Rebuild
* Hot Spare Activation
* Drive Failure Simulation
* Degraded Mode
* Recovery
* Storage Pool Integration
* Controller Interaction

---

# MODULE 44 — STORAGE AUTOMATION STRATEGY

## Decide What Should Be

* Manual
* Automated
* Repeated
* Parameterized
* Regression-Gated

## Automation Activities

* Device Discovery
* Device Inventory
* Health Collection
* Firmware Inventory
* SMART Collection
* NVMe Data Collection
* Log Collection
* FIO Execution
* Output Parsing
* Evidence Bundling
* Threshold Validation
* Result Reporting
* Configuration Validation
* File Validation
* Storage Validation

---

# MODULE 45 — PYTEST STORAGE VALIDATION

## Topics

* Test Discovery
* Assertions
* Fixtures
* conftest.py
* Parameterization
* Markers
* Skip
* SkipIf
* XFail
* Test Organization
* External Command Mocking
* Failure Handling
* Reports

## Framework Structure

```text
Test Plan
→ Framework
→ Test Suites
→ Configuration
→ Target Inventory
→ Execution
→ Logs
→ Results
→ Reports
→ Regression
```

---

# MODULE 46 — CI / REGRESSION

## Topics

* Git Fundamentals
* Branching Basics
* Jenkins Concepts
* GitHub Actions Concepts
* Scheduled Regression
* Test Artifacts
* Failure Notifications
* Test Gating

---

# MODULE 47 — STORAGE DIAGNOSTICS & EVIDENCE

## Evidence Sources

* Linux Logs
* Kernel Logs
* dmesg
* journalctl
* Storage Logs
* Controller Logs
* System Logs
* Event Logs
* SMART
* NVMe Health
* PCIe Logs
* AER
* BMC Logs
* Firmware Evidence
* Performance Evidence
* Workload Data

## Evidence Bundle

```text
Environment
+
Configuration
+
Device State
+
Logs
+
Errors
+
Performance
+
Timeline
+
Reproduction Information
```

---

# MODULE 48 — STORAGE TROUBLESHOOTING FRAMEWORK

Use:

```text
Symptom
→ Evidence
→ Failure Layer
→ Hypothesis
→ Test Hypothesis
→ Eliminate Alternatives
→ Root Cause
→ Corrective Action
→ Verification
→ Regression
```

---

# MODULE 49 — FAILURE CLASSIFICATION

Classify failures into:

* Hardware
* PCIe
* BMC
* BIOS
* Driver
* OS
* NVMe
* Firmware
* Array
* Network
* Configuration
* Test Infrastructure
* Automation

---

# MODULE 50 — ENTERPRISE STORAGE FAILURE SCENARIOS

## Investigate

* Storage Device Not Visible
* NVMe Device Missing
* PCIe Device Not Enumerating
* Filesystem Not Mounting
* LUN Not Visible
* Missing LUN
* I/O Errors
* Path Problems
* Multipath Failure
* Slow Storage
* Performance Degradation
* RAID Degraded
* RAID Rebuild Failure
* Rebuild Performance Problem
* Storage Network Problem
* NFS Issues
* SMB Issues
* iSCSI Issues
* Fibre Channel Issues
* NVMe Issues
* Driver Failure
* Firmware Failure
* Controller Failure
* Controller Failover Problem
* Controller Failback Problem
* VM Storage Latency
* Process Hang Affecting Workload
* Kernel-Related Storage Failure

---

# MODULE 51 — RCA & DEFECT LIFECYCLE

## Failure Investigation

* Failure Reproduction
* Failure Isolation
* Timeline Construction
* Evidence Correlation
* Hypothesis Formation
* Hypothesis Elimination
* Root Cause
* Corrective Action
* Verification
* Regression

## Defect Lifecycle

```text
Failure
→ Investigate
→ Reproduce
→ Collect Evidence
→ Bug Report
→ Developer / Firmware Analysis
→ Fix
→ Fix Verification
→ Regression
→ Release Qualification
```

## Jira

* Defect Reporting
* Bug Verification
* Regression Verification
* Fix Validation
* Customer Issue Investigation

---

# MODULE 52 — ENTERPRISE STORAGE PLATFORM AWARENESS

## Platforms

* NetApp ONTAP
* Dell PowerStore
* Pure Storage
* Storage Virtualization Concepts

## Goal

Understand:

* Platform Architecture
* Provisioning
* Storage Presentation
* HA
* Protocols
* Enterprise Features
* Validation Implications

---

# MODULE 53 — CLOUD / MODERN STORAGE AWARENESS

## AWS

* AWS EBS
* AWS EFS
* AWS S3

## Azure

* Azure Managed Disk
* Azure Blob Storage

## Kubernetes

* Persistent Volumes (PV)
* Persistent Volume Claims (PVC)
* CSI Drivers

## Goal

Understand how enterprise storage concepts translate into cloud and container environments.

---

# MODULE 54 — PROJECT 1 APPLICATION

## Project 1 — Enterprise Storage Platform Feature Validation

Do not relearn the underlying Storage topics.

Apply the mastered knowledge to:

### Provisioning

* Storage Pools
* Volumes
* LUNs
* Thin Provisioning
* Thick Provisioning
* Capacity Expansion
* Volume Expansion
* LUN Mapping
* LUN Masking

### RAID

* RAID Creation
* RAID Deletion
* RAID Expansion
* RAID Migration
* RAID Rebuild
* Hot Spare
* Degraded Mode
* Recovery
* Consistency Check
* Background Initialization

### HA

* Controller Failover
* Controller Failback
* Dual Controller Operation
* Controller Reboot
* Power Cycle
* Power Supply Failure
* Network Port Failure

### Connectivity

* FC
* iSCSI
* Multipathing
* Path Failover
* Host Discovery
* Device Rescan

### Lifecycle

* Firmware Upgrade
* Firmware Downgrade
* Firmware Rollback
* Compatibility
* Mixed Firmware
* Recovery

### Performance

* FIO
* IOmeter
* IOPS
* Throughput
* Latency
* CPU Utilization
* Controller Utilization

### Stability

* Functional Regression
* Performance Regression
* Stress
* Soak
* Long Duration
* Stability Validation

### Automation

* Python
* Pytest
* Paramiko
* Jenkins
* Git

### Diagnostics

* Linux Logs
* Storage Logs
* Controller Logs
* System Logs
* Event Logs
* SMART

### Troubleshooting

* Failure Reproduction
* Failure Isolation
* RCA
* Bug Verification
* Jira
* Regression
* Fix Validation

---

# MODULE 55 — PROJECT 2 APPLICATION

## Project 2 — Enterprise Drive Validation

Do not relearn NVMe, PCIe, SSD, performance, diagnostics or automation.

Apply mastered knowledge to:

### Drive Qualification

* HDD
* SATA SSD
* SAS SSD
* NVMe SSD
* Vendor Qualification
* Capacity
* Interface
* Discovery
* Enumeration

### Compatibility

* Controller
* Backplane
* PCIe
* Firmware
* OS
* Driver
* Mixed Drives
* Compatibility Matrix

### Firmware

* Upgrade
* Downgrade
* Rollback
* Activation
* Recovery
* Compatibility
* Post-Upgrade Verification
* Data Integrity

### Health

* SMART
* NVMe SMART
* Temperature
* Wear
* Media Errors
* Critical Warnings
* Error Counters
* Thresholds

### Performance

* FIO
* IOmeter
* IOPS
* Throughput
* Latency
* Bandwidth
* Queue Depth
* Block Size
* Read / Write
* Mixed Workloads

### Reliability

* Stress
* Endurance
* Burn-In
* Long-Duration I/O
* Power Cycle
* Hot Plug
* Fault Injection

### Integration

* RAID
* RAID Rebuild
* Hot Spare
* Drive Failure
* Degraded Mode
* Recovery
* Storage Pools
* Controller Interaction

### Automation

* Python
* Pytest
* Paramiko
* Jenkins
* Git
* Discovery
* SMART Collection
* FIO Automation
* Health Monitoring
* Result Validation
* Log Collection
* Reporting

### Diagnostics

* smartctl
* nvme-cli
* storcli
* dmesg
* Linux Logs
* Controller Logs
* Storage Logs
* Error Pattern Analysis

### RCA

* Failure Reproduction
* Failure Isolation
* Root Cause Analysis
* Defect Verification
* Jira
* Regression
* Fix Validation
* Customer Issue Investigation

---

# CROSS-CUTTING SKILL — TESTING MINDSET

Testing is applied throughout Storage.

For every major Storage technology:

1. What am I validating?
2. Why does the feature exist?
3. What are normal scenarios?
4. What are negative scenarios?
5. What are boundary cases?
6. What could fail?
7. What evidence proves pass/fail?
8. How do I reproduce failure?
9. How do I isolate the failing layer?
10. How do I verify the fix?
11. What regression should follow?
12. What part should be automated?

---

# CROSS-CUTTING SKILL — PERFORMANCE

For every performance-sensitive feature:

```text
Baseline
→ Controlled Workload
→ Execute
→ Measure
→ Compare
→ Identify Regression
→ Isolate Bottleneck
→ Verify
```

---

# CROSS-CUTTING SKILL — TROUBLESHOOTING / RCA

For every major technology:

```text
Symptom
→ Evidence
→ Layer Identification
→ Hypothesis
→ Investigation
→ Elimination
→ Root Cause
→ Fix
→ Verification
→ Regression
```

---

# CROSS-CUTTING SKILL — INTERVIEW DEFENSE

For each major Storage topic:

```text
What?
Why?
How?
What happens internally?
What can fail?
How do you detect it?
What evidence do you collect?
Which layer do you investigate?
How do you reproduce it?
How do you isolate it?
How do you verify the fix?
How do you prevent regression?
Can it be automated?
What performance impact exists?
What trade-offs exist?
```

---

# SPLIT 3 — MASTER ASSESSMENT

Before final completion:

* [ ] Explain testing methodologies
* [ ] Design enterprise test strategy
* [ ] Design test cases and scenarios
* [ ] Build test coverage
* [ ] Define entry / exit criteria
* [ ] Define pass / fail criteria
* [ ] Collect storage health evidence
* [ ] Use SMART / NVMe diagnostics
* [ ] Understand firmware lifecycle validation
* [ ] Design FIO workloads
* [ ] Analyze IOPS / throughput / latency
* [ ] Analyze percentile / tail latency
* [ ] Identify bottlenecks
* [ ] Perform stress / soak / endurance validation
* [ ] Validate HA
* [ ] Validate host connectivity
* [ ] Qualify enterprise drives
* [ ] Validate compatibility
* [ ] Validate drive integration
* [ ] Plan Storage automation
* [ ] Build / understand pytest storage validation
* [ ] Understand CI / regression
* [ ] Collect complete evidence bundles
* [ ] Troubleshoot representative storage failures
* [ ] Perform RCA
* [ ] Understand defect lifecycle
* [ ] Apply Storage knowledge to Project 1
* [ ] Apply Storage knowledge to Project 2
* [ ] Defend Storage decisions in interviews
* [ ] Complete final Storage assessment

---

# FINAL STORAGE MASTERY TARGET

A completed Storage Mastery Syllabus should enable you to:

* [ ] Explain enterprise storage architecture end-to-end
* [ ] Explain Storage I/O
* [ ] Explain SATA / SAS / SCSI
* [ ] Explain NVMe / PCIe
* [ ] Explain SSD internals
* [ ] Explain RAID
* [ ] Explain enterprise storage arrays
* [ ] Explain SAN / NAS / iSCSI / FC
* [ ] Explain multipathing
* [ ] Explain Linux-facing Storage
* [ ] Explain server / BMC / virtualization relationships
* [ ] Design storage validation
* [ ] Validate Storage features
* [ ] Validate enterprise drives
* [ ] Validate firmware
* [ ] Analyze performance
* [ ] Analyze storage health
* [ ] Troubleshoot Storage failures
* [ ] Perform RCA
* [ ] Automate repeatable validation
* [ ] Apply knowledge to Project 1
* [ ] Apply knowledge to Project 2
* [ ] Defend the engineering decisions in interviews

```

This is the **three-split structure** I recommend using as your Storage master syllabus. The important thing is that the splits are **study partitions, not separate courses**: once a topic is mastered in its home split, Project 1 and Project 2 use that knowledge rather than making you relearn it.
```

