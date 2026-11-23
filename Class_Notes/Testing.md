# **Testing – Complete Interview Questions & Answers**

# **Section 1 – Testing Fundamentals**

### **Q1. What is software testing, and why is testing important?**

**Answer:**

Software testing is the process of verifying whether a software product or application is working according to the expected behaviour or not.

Developers develop the product, and testers or QA engineers test the product to identify defects and verify its functionality.

**Why is testing important?**

1. Testing helps improve the quality of the product.
2. It helps identify defects before releasing the product to customers.
3. It reduces the chances of customers facing issues after release.
4. It helps improve customer satisfaction.
5. It improves the overall quality and reputation of the company.

If we release a product without proper testing, there are high chances that customers may experience issues or bugs.

### **Q2. What are the different ways of testing? Explain manual testing and automation testing with advantages and disadvantages.**

**Answer:**

There are two main ways of testing:

1. Manual Testing.
2. Automation Testing.

**1. Manual Testing:**

Manual testing is the process of verifying a software product manually to check whether it is working according to the expected behaviour.

In manual testing, testers execute test cases without depending on automation scripts or tools.

*Advantages:*

- Easy to perform testing without writing scripts.
- Useful for manual interaction and exploratory testing.
- Helps testers understand the product functionality.

*Disadvantages:*

- It takes more time.
- It is less efficient for repetitive execution.
- It is not suitable for long-term repetitive test cases.

**2. Automation Testing:**

Automation testing is the process of verifying a software product using scripts or tools to check whether it is working according to the expected behaviour.

In automation testing, test cases are executed with the help of automation scripts or tools.

*Advantages:*

- More efficient.
- Saves execution time.
- Reduces manual interaction.
- Useful for repetitive test execution.
- Helps execute regression test cases repeatedly.

*Disadvantages:*

- 100% test coverage cannot be achieved through automation alone.
- Implementation cost can be high.
- Automation scripts require development and maintenance.

### **Q3. When should we choose manual testing and when should we choose automation testing?**

**Answer:**

We choose manual testing or automation testing depending on the type of test case and testing requirements.

**Manual Testing:**

We use manual testing when:

1. We need to understand new product functionality.
2. We need exploratory testing.
3. We need to verify manual interactions.
4. The test case requires human observation and judgement.
5. The test cases are executed occasionally.

**Automation Testing:**

We use automation testing when:

1. Test cases need to be executed repeatedly.
2. We perform regression testing frequently.
3. Test cases are time-consuming.
4. We need repeatable test execution.
5. We need to reduce manual execution effort.

**Example:**

Suppose we have 1,000 test cases.

We may execute some important test cases manually during initial testing and automate stable, frequently repeated test cases for regression testing.

### **Q4. What are the different methods of testing? Explain White Box, Black Box and Grey Box testing.**

**Answer:**

There are three main testing methods:

1. White Box Testing.
2. Black Box Testing.
3. Grey Box Testing.

**1. White Box Testing:**

White Box Testing is a testing method used to identify issues in the software source code.

Testers need knowledge of the developer's code.

*Advantages:*

- Helps identify issues in the source code.
- Helps optimize developer code.

*Disadvantages:*

- Requires skilled engineers.
- Implementation cost can be high.

**2. Black Box Testing:**

Black Box Testing is a testing method used to identify issues in software functionality without requiring knowledge of the internal source code.

Testers verify the product functionality using inputs and expected outputs.

*Advantages:*

- Testers do not need knowledge of developer code.
- Useful for validating product functionality.

*Disadvantages:*

- Some internal code-related issues may not be identified.
- Inefficient testing may occur without proper test coverage.

**3. Grey Box Testing:**

Grey Box Testing combines the benefits of White Box and Black Box testing.

Testers have knowledge of both the product functionality and some internal implementation details.

*Advantages:*

- Combines the benefits of both testing methods.
- Helps improve testing coverage.

*Disadvantages:*

- Requires skilled engineers.
- It may take more time to complete.

### **Q5. What is the difference between Functional Testing and Non-Functional Testing?**

**Answer:**

**Functional Testing:**

Functional testing verifies whether the product or software is working according to the functional requirements.

It checks what the system is supposed to do.

Examples:

- Functional Verification Testing.
- Unit Testing.
- Smoke Testing.
- Regression Testing.
- Retesting.
- Integration Testing.
- System Testing.

**Non-Functional Testing:**

Non-functional testing verifies how the product or software behaves under different conditions.

It checks aspects that are not directly covered by functional testing.

Examples:

- Performance Testing.
- Load Testing.
- Stress Testing.
- Security Testing.
- Scalability Testing.

| Functional Testing               | Non-Functional Testing                              |
| -------------------------------- | --------------------------------------------------- |
| Verifies functionality           | Verifies product behaviour and quality attributes   |
| Checks expected functionality    | Checks performance and other non-functional aspects |
| Based on functional requirements | Based on non-functional requirements                |
| Example: RAID creation           | Example: RAID performance under workload            |

# **Section 2 – SDLC, STLC and Testing Types**

### **Q6. What is SDLC? Explain all stages of the Software Development Life Cycle.**

**Answer:**

SDLC stands for Software Development Life Cycle.

It is the complete process followed to develop and maintain a software product.

According to my notes, SDLC contains seven stages.

**1. Idea:**

Every software product or application starts with an idea.

The requirement or idea is identified and approved.

**2. Design:**

Once the idea is approved, architects design the product.

**3. Coding:**

Developers implement the design by writing the required code.

**4. Testing:**

Testers perform testing to verify that the product is working correctly and identify defects.

**5. Release:**

After testing is completed, the product is released to the market.

**6. Support:**

After release, the support team helps customers resolve issues.

**7. End of Life (EOL):**

After a certain period, the product reaches the end of its life, and further support may no longer be provided.

The SDLC flow is:
````

Idea\
|\
Design\
|\
Coding\
|\
Testing\
|\
Release\
|\
Support\
|\
End of Life

```

### **Q7. What is STLC? Explain all stages of the Software Testing Life Cycle.**

**Answer:**

STLC stands for Software Testing Life Cycle.

It is the complete process followed by testers to perform software testing.

According to my notes, STLC contains six stages.

**1. Requirement Analysis:**

In this phase, testers analyse customer requirements and work with developers to understand the requirements.

**2. Test Planning:**

In this phase, testers plan the complete testing activities.

We decide:

- What to test.
- What not to test.
- What testing strategy to follow.
- What test environment is required.
- What resources are required.
- Test schedule and estimation.

**3. Test Design:**

In this phase, testers prepare test cases.

We can prepare:

- Manual test cases.
- Automation test cases.

**4. Test Environment Setup:**

In this phase, we prepare the test environment or test bed for executing the test cases.

**5. Test Execution:**

In this phase, testers execute the test cases on the test environment.

After execution, we record the result as PASS or FAIL.

If a test case fails, we investigate the issue and raise a bug when a product defect is identified.

**6. Test Reporting:**

In this phase, we prepare test reports.

We report:

- Number of test cases executed.
- Number of test cases passed.
- Number of test cases failed.
- Number of defects raised.
- Testing status.

The STLC flow is:
```

Requirement Analysis\
|\
Test Planning\
|\
Test Design\
|\
Test Environment Setup\
|\
Test Execution\
|\
Test Reporting

```

### **Q8. What is the difference between SDLC and STLC?**

**Answer:**

| SDLC                                                             | STLC                                                                                        |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Software Development Life Cycle                                  | Software Testing Life Cycle                                                                 |
| Focuses on developing the software product                       | Focuses on testing the software product                                                     |
| Includes idea, design, coding, testing, release, support and EOL | Includes requirement analysis, planning, design, environment setup, execution and reporting |
| Developers and other project teams participate                   | Primarily testing team activities                                                           |
| Produces a software product                                      | Produces testing results, defect reports and quality evidence                               |

**Example:**

In SDLC, developers develop a product and release it.

In STLC, testers analyse the requirements, prepare test cases, configure the test environment, execute test cases and report defects.

### **Q9. What is the difference between Unit Testing and Integration Testing? Explain System Testing as well.**

**Answer:**

**1. Unit Testing:**

Unit testing is also called Code Level Testing.

In unit testing, developers test individual units of source code before integrating them into the complete application.

It helps identify issues at the individual code-unit level.

**2. Integration Testing:**

Integration testing is a level of software testing in which individual units are combined and tested as a group.

It helps identify issues related to communication and interaction between different modules.

Both developers and testers can perform integration testing.

**3. System Testing:**

System testing is a level of software testing in which we test the complete product or system.

We verify end-to-end functionality and customer use cases.

For example, we execute the complete workflow of a product to check whether all functionalities are working correctly.

| Unit Testing                   | Integration Testing        | System Testing                   |
| ------------------------------ | -------------------------- | -------------------------------- |
| Tests individual code units    | Tests combined modules     | Tests the complete system        |
| Mainly performed by developers | Developers and testers     | Testing team                     |
| Code-level testing             | Module interaction testing | End-to-end functionality testing |

### **Q10. What are DVT (Design Verification Testing) and FVT (Functional Verification Testing)?**

**Answer:**

**DVT – Design Verification Testing:**

DVT stands for Design Verification Testing.

It is performed to verify whether the implemented product or design meets the defined design requirements and specifications.

It helps identify design-related issues.

**FVT – Functional Verification Testing:**

FVT stands for Functional Verification Testing.

It is performed to verify the product functionality against the expected behaviour and functional requirements.

We test the available functionality and verify whether the product is working as expected.

**Difference:**

| DVT                           | FVT                              |
| ----------------------------- | -------------------------------- |
| Design Verification Testing   | Functional Verification Testing  |
| Verifies design requirements  | Verifies functional requirements |
| Focuses on design correctness | Focuses on product functionality |

*Additional interview clarification:* Your notes identify DVT and FVT but provide much more detail about FVT than DVT. The DVT explanation above expands the definition.

### **Q11. What is the difference between Regression Testing and Retesting?**

**Answer:**

**Regression Testing:**

Regression testing is performed to ensure that existing functionalities are not affected by recent code changes or bug fixes.

Whenever developers provide a new build containing changes, testers execute regression test cases to confirm that other functionalities are still working correctly.

**Retesting:**

Retesting is performed by executing previously failed test cases on a new build to verify whether the reported defects have been fixed.

It is also called defect verification or bug verification.

**Example:**

Suppose we execute 1,000 test cases:

- 700 test cases pass.
- 300 test cases fail.

We raise bugs for the failed test cases.

After developers provide a new build:

- We perform retesting on the failed test cases.
- We perform regression testing to ensure that existing functionalities are not affected.

| Regression Testing                                              | Retesting                                                   |
| --------------------------------------------------------------- | ----------------------------------------------------------- |
| Checks whether existing functionalities are affected by changes | Checks whether previously failed test cases are now passing |
| Covers impacted and existing functionalities                    | Covers specific failed test cases                           |
| Performed after changes or bug fixes                            | Performed after a defect fix                                |
| Focuses on unintended side effects                              | Focuses on defect verification                              |

### **Q12. What is the difference between Smoke Testing and Sanity Testing?**

**Answer:**

**Smoke Testing:**

Smoke testing is performed after installing a new software build to verify whether the basic functionalities are working.

It is also called Build Verification Testing.

The purpose is to check whether the build is stable enough for further testing.

**Example:**

After installing a new build:

1. Verify that the application launches.
2. Verify that login works.
3. Verify that the basic functionality works.
4. Confirm that the build is suitable for further testing.

**Sanity Testing:**

Sanity testing is performed when we have less time and need to execute only the important test cases.

We select important test cases based on changes, fixes and critical functionalities.

| Smoke Testing                            | Sanity Testing                                                 |
| ---------------------------------------- | -------------------------------------------------------------- |
| Performed on a new build                 | Performed to verify specific changes or impacted functionality |
| Checks basic build stability             | Checks important selected functionality                        |
| Also called Build Verification Testing   | Focused testing                                                |
| Helps decide whether to continue testing | Helps verify whether a particular change is working            |

### **Q13. What is Adhoc Testing and Monkey Testing? When do we perform them?**

**Answer:**

**1. Adhoc Testing:**

Adhoc testing is an unplanned testing approach performed without formal test planning or documentation.

According to my notes, when testers complete their assigned test cases early, they can perform adhoc testing.

**Example:**

Suppose a tester has completed all assigned test cases in a 10-day schedule within 8 days.

The tester can use the remaining time to perform adhoc testing to identify additional issues.

**2. Monkey Testing:**

Monkey testing is a type of testing performed without detailed knowledge of the product functionality.

The tester performs random actions or inputs to identify unexpected behaviour.

**When do we perform them?**

- Adhoc testing: When assigned test cases are completed and additional exploratory testing time is available.
- Monkey testing: When we want to check how the application behaves under random inputs or actions.

### **Q14. What is Performance Testing? Explain Load Testing and Stress Testing with examples.**

**Answer:**

Performance testing is a type of non-functional testing in which we verify the performance of a device or product under test using different workloads.

There are two types mentioned in my notes:

**1. Load Testing:**

Load testing is performed to verify whether the product or system can handle workloads within its supported limits.

**Example:**

If an application supports 1,000 concurrent users, we execute a workload with 1,000 users and verify its performance.

**2. Stress Testing:**

Stress testing is performed by applying workloads above the supported level to check how the product behaves under excessive load.

**Example:**

If an application supports 1,000 concurrent users, we increase the workload to 1,500 users and observe how the system behaves.

| Load Testing                        | Stress Testing                                  |
| ----------------------------------- | ----------------------------------------------- |
| Workload is within supported limits | Workload is above supported limits              |
| Checks normal performance           | Checks behaviour under excessive load           |
| Verifies supported capacity         | Identifies breaking points and stability issues |

### **Q15. What is Compatibility Testing? Why do we perform it?**

**Answer:**

Compatibility testing is a type of testing in which we verify whether the product works correctly with different hardware configurations and environments.

We perform compatibility testing to ensure that the product works across different hardware platforms.

**Example:**

Suppose we are testing an application on different laptop configurations:

- Intel CPU laptop.
- HP laptop.
- Dell laptop.
- Lenovo laptop.

We execute the same test cases on different hardware configurations and verify whether the product works consistently.

In enterprise storage validation, compatibility testing can also involve different server models, storage adapters and hardware configurations.

### **Q16. What is Acceptance Testing? Explain Alpha Testing and Beta Testing with examples.**

**Answer:**

Acceptance Testing is a level of testing performed to verify whether a product meets customer requirements and acceptance criteria and is suitable for acceptance.

It focuses on whether the product satisfies user and business needs.

Two types of acceptance testing are:

**1. Alpha Testing:**

Alpha Testing is a type of acceptance testing performed in the developer's testing environment by people outside the development organization.

These may include:

- Potential users.
- Customer representatives.
- Independent testing teams.

The purpose is to identify defects and collect feedback before the product is released for wider external use.

**Example:**

Suppose our company develops an Enterprise Storage Array.

1. The development team completes the product development.
2. Our internal QA team completes the initial testing.
3. Customer representatives visit our development/testing facility.
4. They execute their test cases on our storage array.
5. They verify the product against their requirements.
6. They provide feedback and report any issues.

This is Alpha Testing.

**2. Beta Testing:**

Beta Testing is a type of acceptance testing performed at an external environment by potential or existing users/customers or other roles outside the development organization.

The product is provided to selected customers or users so they can evaluate it under their actual operating conditions and provide feedback.

**Example:**

Suppose our company develops an Enterprise Storage Array.

1. Alpha Testing is completed.
2. A beta version of the storage array is provided to selected customers.
3. Customers install the storage array in their own environment.
4. They connect their servers and configure storage.
5. They execute their actual workloads.
6. They monitor performance, reliability and functionality.
7. They report issues and provide feedback.

This is Beta Testing.

**Difference between Alpha and Beta Testing:**

| Feature          | Alpha Testing                                                       | Beta Testing                                           |
| ---------------- | ------------------------------------------------------------------- | ------------------------------------------------------ |
| Testing location | Developer's testing environment                                     | External/customer environment                          |
| Who performs it? | Potential users, customer representatives or independent test teams | Potential or existing users/customers                  |
| Environment      | Controlled developer environment                                    | External operational environment                       |
| Main purpose     | Identify defects and gather early feedback                          | Validate user needs and real-world behaviour           |
| Product stage    | Generally before beta testing                                       | Generally after alpha testing and before wider release |
| Feedback         | Provided to development/testing teams                               | Provided by external users/customers                   |

### **Q17. What is Positive Testing and Negative Testing? Why do we perform both?**

**Answer:**

**Positive Testing:**

Positive testing is a type of testing in which we provide valid inputs and check whether the product works as expected.

**Example:**

If a system accepts passwords between 8 and 15 characters, we enter a valid password of 10 characters and verify that it is accepted.

**Negative Testing:**

Negative testing is a type of testing in which we provide invalid inputs and verify whether the product handles them correctly.

The purpose is to ensure that invalid inputs do not crash the product or affect its stability.

**Example:**

For a password that supports 8 to 15 characters, we provide:

- 5 characters.
- 20 characters.
- Empty input.

The application should reject invalid input and remain stable.

We perform both types of testing to verify normal functionality and incorrect input handling.

### **Q18. What is End-to-End Testing?**

**Answer:**

End-to-End testing is a type of testing in which we verify the complete functionality of a product by executing a complete workflow from the starting point to the final result.

It checks whether all integrated components are working together correctly.

**Example:**

For an application, we can perform the following workflow:

1. Launch the application.
2. Log in.
3. Select a feature.
4. Enter the required information.
5. Submit the operation.
6. Verify the final result.

If the complete workflow works according to the expected behaviour, the End-to-End test case passes.

In my notes, this concept is closely related to System Testing, where testers execute complete product functionalities based on customer use cases.

# **Section 3 – Test Planning, Test Design and Test Documentation**

### **Q19. What is a Test Scenario and what is a Test Case? Explain the difference with an example.**

**Answer:**

**Test Scenario:**

A Test Scenario is a high-level description of a functionality that needs to be tested.

It defines what functionality we need to verify.

**Test Case:**

A Test Case is a detailed set of instructions used to verify whether a particular functionality works according to the expected behavior.

Every test case should contain the following fields:

1. Test Case ID.
2. Summary.
3. Preconditions.
4. Steps.
5. Expected Behavior.
6. Actual Result/Behavior.
7. Status.

**Example: Google Chrome Refresh Functionality**

Test Scenario:

Verify Google Chrome refresh functionality.

Test Case:

| Field                  | Details                                                                                                       |
| ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_001                                                                                                 |
| Summary                | Verify that Chrome refreshes the currently opened webpage                                                     |
| Preconditions          | Chrome is installed and can be launched. A valid website is accessible, and network connectivity is available. |
| Steps                  | 1. Open Chrome. 2. Navigate to a valid website. 3. Wait for the webpage to load. 4. Click the Refresh button. |
| Expected Behavior      | The currently opened webpage should refresh successfully without browser errors.                              |
| Actual Result/Behavior | Not executed yet.                                                                                             |
| Status                 | Not Executed                                                                                                  |

**Difference:**

| Test Scenario                   | Test Case                             |
| ------------------------------- | ------------------------------------- |
| High-level description          | Detailed verification procedure       |
| Defines what to test            | Defines how to test                   |
| Can contain multiple test cases | Covers a specific test condition      |
| Focuses on functionality        | Focuses on verification and execution |

### **Q20. What are the different mandatory fields of a Test Case? Explain each field with an example.**

**Answer:**

A Test Case is a documented procedure used to verify whether a particular product functionality is working according to the expected behavior.

Every test case must contain the following seven fields in our test-case format.

**1. Test Case ID:**

A unique identifier assigned to every test case.

Example:

`TC_RAID_001`

**2. Summary:**

A brief description of what functionality we are testing.

Example:

Verify RAID 5 creation using the minimum required number of drives.

**3. Preconditions:**

Conditions that must be satisfied before executing the test case.

Examples:

- Test environment should be ready.
- Required hardware should be available.
- Required firmware should be installed.
- User should have the necessary permissions.
- Required configuration should be completed.

**4. Steps:**

Step-by-step instructions that the tester follows while executing the test case.

Example:

1. Log in to the storage management interface.
2. Navigate to RAID configuration.
3. Select three compatible drives.
4. Select RAID 5.
5. Submit the RAID creation request.

**5. Expected Behavior:**

The behavior that should occur according to the product requirements.

Example:

RAID 5 should be created successfully, and the RAID Group should enter the expected healthy state.

**6. Actual Result/Behavior:**

The behavior actually observed when we execute the test case.

Example:

RAID 5 was created successfully, and the RAID Group entered the Online state.

If the test case has not been executed yet, record:

`Not executed yet`

**7. Status:**

The final execution status based on the comparison between expected and actual behavior.

Common statuses include:

| Status       | Meaning                                                                     |
| ------------ | --------------------------------------------------------------------------- |
| Not Executed | Test case has not been executed                                             |
| In Progress  | Test case execution is ongoing                                              |
| PASS         | Actual behavior matches expected behavior                                   |
| FAIL         | Actual behavior differs from expected behavior                              |
| BLOCKED      | Test case cannot be executed because of an unmet precondition or dependency |
| N/A          | Test case is not applicable to the current configuration                    |

**Complete Test Case Example:**

| Field                  | Details                                                                                                                                       |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_RAID_001                                                                                                                                   |
| Summary                | Verify RAID 5 creation                                                                                                                        |
| Preconditions          | Three compatible drives are available. RAID Controller is detected and healthy. Required permissions are available.                           |
| Steps                  | 1. Open RAID management utility. 2. Select three available drives. 3. Select RAID 5. 4. Submit the configuration. 5. Check RAID Group status. |
| Expected Behavior      | RAID 5 should be created successfully and enter the expected healthy state.                                                                   |
| Actual Result/Behavior | Not executed yet.                                                                                                                             |
| Status                 | Not Executed                                                                                                                                  |

**Important Interview Point:**

Expected Behavior is defined before test execution.

Actual Result/Behavior is recorded after test execution.

We should never copy the expected result into the actual result without executing the test case.

The test case can be designed before execution, but the actual result and final status must be updated during or after the execution.

### **Q21. How do you write test cases using a Functional Verification Document or Product Verification Document?**

**Answer:**

A Functional Verification Document (FVD) or Product Verification Document (PVD) contains detailed information about the functionality, requirements and expected behavior of a product.

As a tester, I refer to this document to understand the functionality and prepare appropriate test cases.

**Process:**

1. Read and understand the FVD/PVD.
2. Identify all product functionalities.
3. Identify the requirements and expected behaviors.
4. Prepare high-level test scenarios.
5. Derive positive and negative test cases.
6. Identify the preconditions for each test case.
7. Write detailed execution steps.
8. Define expected behavior for every test case.
9. Assign a unique Test Case ID.
10. Keep actual result and status fields ready for execution.
11. Review test cases for requirement coverage.
12. Map requirements to test cases using the Traceability Matrix.

**Example: RAID 5 Functionality**

Suppose the FVD specifies that RAID 5 supports three or more compatible drives.

Test Scenario:

Verify RAID 5 creation functionality.

Derived Test Cases:

- Verify RAID 5 creation using three compatible drives.
- Verify RAID 5 creation using four compatible drives.
- Verify RAID 5 creation with fewer than three drives.
- Verify that RAID 5 creation is rejected when no drives are selected.
- Verify RAID 5 status after successful creation.
- Verify RAID 5 behavior when one member drive fails.

Each of these test cases must be documented using all seven mandatory fields defined in Q20.

**Objective:**

Ensure every functional requirement is covered by properly documented and executable test cases.

### **Q22. What is the difference between Test Plan and Test Strategy?**

**Answer:**

**Test Strategy:**

Test Strategy defines the overall approach that we follow for testing a product.

It describes the testing methodologies, scope, approach and general testing activities.

**Test Plan:**

A Test Plan describes the testing activities planned for a particular release or testing cycle.

It defines what test cases need to be executed for that release.

According to my notes, we select the required test cases from the Master Test Suite and create a Test Plan for a particular release.

| Test Strategy                         | Test Plan                                           |
| ------------------------------------- | --------------------------------------------------- |
| Overall testing approach              | Specific testing activities                         |
| Defines how testing will be performed | Defines what will be tested in a particular release |
| High-level document                   | More detailed execution-oriented document           |
| Can be applicable across releases     | Usually prepared for a specific release or project  |

### **Q23. What is a Test Suite, Test Cycle and Release Test Cycle? Explain the differences.**

**Answer:**

**1. Test Suite:**

A Test Suite is a collection of multiple test cases.

For example, a storage product may have separate test suites for RAID, drive discovery, performance and firmware testing.

**2. Test Cycle:**

A Test Cycle is a collection of test cases planned for a particular testing execution.

We create a Test Cycle by selecting test cases from the Master Test Suite or Master Test Plan.

**3. Release Test Cycle:**

A Release Test Cycle is the execution of selected test cases for a particular product release.

For every new release, we can create a new Test Cycle and update the execution results.

**Example:**

Suppose we have 100 test cases.

Release 1:

- Create Release 1 Test Cycle.
- Execute 100 test cases.
- Update PASS/FAIL results.

Release 2:

- Create Release 2 Test Cycle.
- Execute the required test cases.
- Update the results again.

Whenever we execute test cases, we update their execution status.

Initially, the status is Unexecuted. During execution, it becomes In Progress, and after execution, it becomes PASS or FAIL.

### **Q24. What are Entry Criteria and Exit Criteria?**

**Answer:**

**Entry Criteria:**

Entry criteria are the conditions that must be satisfied before starting testing.

According to my notes, successful build installation on the testbed is an entry criterion.

Other practical conditions include:

- Test environment should be ready.
- Required test cases should be available.
- Required hardware and software configurations should be available.
- Build should be successfully installed.

**Exit Criteria:**

Exit criteria are the conditions that must be satisfied before stopping or completing testing.

According to my notes, when the product becomes sufficiently defect-free and the testing objectives are achieved, we can consider testing complete.

Other practical conditions include:

- Planned test cases should be executed.
- Results should be documented.
- Critical defects should be resolved or formally accepted.
- Required testing reports should be prepared.

**Example:**

Suppose we have 1,000 test cases.

| Build   | Defects |
| ------- | ------- |
| Build 1 | 50 bugs |
| Build 2 | 5 bugs  |
| Build 3 | 0 bugs  |

After resolving the defects and satisfying the planned exit criteria, we can conclude the testing activity.

### **Q25. What is a Traceability Matrix? Why do we use it?**

**Answer:**

A Traceability Matrix is also called a Requirement Traceability Matrix (RTM).

It is a document that maps requirements or test scenarios to their corresponding test cases.

We use it to:

1. Verify whether all requirements are covered.
2. Identify missing test cases.
3. Track the execution status of test cases.
4. Identify which functionality is affected by a failure.
5. Ensure complete test coverage.

**Example:**

| Requirement   | Test Cases    | Status                       |
| ------------- | ------------- | ---------------------------- |
| Requirement 1 | TC1, TC2, TC3 | TC1 PASS, TC2 FAIL, TC3 PASS |
| Requirement 2 | TC4, TC5      | TC4 PASS, TC5 PASS           |
| Requirement 3 | TC6, TC7      | TC6 FAIL, TC7 Unexecuted     |

Using the Traceability Matrix, we can easily identify which requirements have passed, failed or remain unexecuted.

### **Q26. Explain the different Test Case Writing Techniques: Equivalence Partitioning, Boundary Value Analysis and Error Guessing.**

**Answer:**

There are three important test case writing techniques in my notes.

**1. Equivalence Partitioning:**

Equivalence Partitioning is a test case design technique in which we divide the input values into different groups or partitions.

We select representative values from each partition instead of testing every possible value.

**Example:**

Suppose a password must contain a minimum of 8 characters and a maximum of 15 characters.

We divide the inputs into three partitions:

| Partition   | Input                   | Expected Result |
| ----------- | ----------------------- | --------------- |
| Below range | Less than 8 characters  | Invalid         |
| Valid range | 8–15 characters         | Valid           |
| Above range | More than 15 characters | Invalid         |

We select representative values from each partition and execute the test cases.

**2. Boundary Value Analysis:**

Boundary Value Analysis is a test case design technique in which we test values at the boundaries of the supported range.

**Example:**

Suppose the valid password length is 8 to 15 characters.

We test:

- 7 characters – Invalid.
- 8 characters – Valid.
- 9 characters – Valid.
- 14 characters – Valid.
- 15 characters – Valid.
- 16 characters – Invalid.

This helps identify defects that occur at the minimum and maximum supported limits.

**3. Error Guessing:**

Error Guessing is a testing technique in which testers use their previous experience and knowledge to predict possible failure conditions.

**Example:**

Suppose I have previous experience testing RAID functionality.

I know that RAID 5 requires a minimum number of drives.

Based on that experience, I can design negative test cases such as attempting RAID 5 creation with insufficient drives.

This helps identify issues that may not be covered through normal test case design techniques.

### **Q27. Write five positive and five negative test cases for Google Chrome.**

**Answer:**

I would prepare separate positive and negative test cases to verify normal functionality and incorrect-input handling.

For every test case, I record all seven mandatory fields.

**A. Positive Test Cases**

**TC01 – Verify Google Chrome Launch**

| Field                  | Details                                                                                                    |
| ---------------------- | ---------------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_001                                                                                              |
| Summary                | Verify Chrome launches successfully                                                                        |
| Preconditions          | Google Chrome is installed. Supported OS is running.                                                       |
| Steps                  | 1. Navigate to the Chrome application. 2. Double-click the Chrome icon. 3. Wait for the browser to launch. |
| Expected Behavior      | Chrome should launch successfully and display the browser window.                                          |
| Actual Result/Behavior | Not executed yet.                                                                                          |
| Status                 | Not Executed                                                                                               |

**TC02 – Verify Valid Website URL**

| Field                  | Details                                                                                |
| ---------------------- | -------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_002                                                                          |
| Summary                | Verify opening a valid website URL                                                     |
| Preconditions          | Chrome is installed and can be launched. Internet connectivity is available, and the website is reachable. |
| Steps                  | 1. Open Chrome. 2. Enter a valid URL such as `https://www.google.com`. 3. Press Enter. |
| Expected Behavior      | The requested website should load successfully.                                        |
| Actual Result/Behavior | Not executed yet.                                                                      |
| Status                 | Not Executed                                                                           |

**TC03 – Verify Refresh Functionality**

| Field                  | Details                                                                                                 |
| ---------------------- | ------------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_003                                                                                           |
| Summary                | Verify webpage refresh functionality                                                                    |
| Preconditions          | Chrome is installed and can be launched. Network connectivity is available, and a valid website is reachable. |
| Steps                  | 1. Open a website. 2. Wait for it to load. 3. Click the Refresh button. 4. Wait for the page to reload. |
| Expected Behavior      | The webpage should refresh successfully without unexpected browser errors.                              |
| Actual Result/Behavior | Not executed yet.                                                                                       |
| Status                 | Not Executed                                                                                            |

**TC04 – Verify New Tab Functionality**

| Field                  | Details                                                              |
| ---------------------- | -------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_004                                                        |
| Summary                | Verify that Chrome opens a new tab                                   |
| Preconditions          | Chrome is installed, and a user profile is available.                 |
| Steps                  | 1. Open Chrome. 2. Press `Ctrl + T`. 3. Observe the browser window.  |
| Expected Behavior      | A new tab should open successfully without closing the existing tab. |
| Actual Result/Behavior | Not executed yet.                                                    |
| Status                 | Not Executed                                                         |

**TC05 – Verify Search Functionality**

| Field                  | Details                                                                                       |
| ---------------------- | --------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_005                                                                                 |
| Summary                | Verify searching using a valid keyword                                                        |
| Preconditions          | Chrome is installed and can be launched. Internet connectivity and a working default search engine are available. |
| Steps                  | 1. Open Chrome. 2. Enter a valid search keyword such as `Python programming`. 3. Press Enter. |
| Expected Behavior      | Relevant search results should be displayed by the configured search engine.                  |
| Actual Result/Behavior | Not executed yet.                                                                             |
| Status                 | Not Executed                                                                                  |

**B. Negative Test Cases**

**TC06 – Verify Invalid URL Handling**

| Field                  | Details                                                                                             |
| ---------------------- | --------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_006                                                                                       |
| Summary                | Verify Chrome handles a malformed URL                                                               |
| Preconditions          | Chrome is installed and can be launched.                                                            |
| Steps                  | 1. Open Chrome. 2. Enter a malformed URL such as `http://[invalid`. 3. Press Enter.                 |
| Expected Behavior      | Chrome should reject the invalid URL or display an appropriate error. The browser should not crash. |
| Actual Result/Behavior | Not executed yet.                                                                                   |
| Status                 | Not Executed                                                                                        |

**TC07 – Verify Unsupported URL Scheme Handling**

| Field                  | Details                                                                                                                                             |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_007                                                                                                                                       |
| Summary                | Verify Chrome handles an unsupported URL scheme                                                                                                     |
| Preconditions          | Chrome is installed and can be launched. No application handler is configured for the test scheme.                                                  |
| Steps                  | 1. Open Chrome. 2. Enter an unsupported URL scheme such as `unknownscheme://test`. 3. Press Enter. 4. Observe the browser response.                 |
| Expected Behavior      | Chrome should handle the unsupported scheme appropriately, for example by showing an error or handler prompt. The browser should remain responsive. |
| Actual Result/Behavior | Not executed yet.                                                                                                                                   |
| Status                 | Not Executed                                                                                                                                        |

**TC08 – Verify Empty URL Handling**

| Field                  | Details                                                                                              |
| ---------------------- | ---------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_008                                                                                        |
| Summary                | Verify Chrome handles an empty address-bar input                                                     |
| Preconditions          | Chrome is running and a browser tab is open.                                                         |
| Steps                  | 1. Focus the existing Chrome window. 2. Select the address bar. 3. Clear the existing text. 4. Press Enter. |
| Expected Behavior      | Chrome should handle the empty input without crashing or displaying an unexpected application error. |
| Actual Result/Behavior | Not executed yet.                                                                                    |
| Status                 | Not Executed                                                                                         |

**TC09 – Verify Website Access Without Network Connectivity**

| Field                  | Details                                                                                                                    |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_009                                                                                                              |
| Summary                | Verify website access when network connectivity is unavailable                                                             |
| Preconditions          | Chrome is installed and can be launched. A valid website URL is known. Network connectivity can be disconnected safely.    |
| Steps                  | 1. Disconnect the system from the network. 2. Open Chrome. 3. Enter the valid website URL. 4. Press Enter.                 |
| Expected Behavior      | Chrome should display an appropriate connection error or unavailable-page response. The browser should remain operational. |
| Actual Result/Behavior | Not executed yet.                                                                                                          |
| Status                 | Not Executed                                                                                                               |

**TC10 – Verify Refresh When Network Is Disconnected**

| Field                  | Details                                                                                                                                                   |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | TC_CHROME_010                                                                                                                                             |
| Summary                | Verify refresh behavior when network connectivity is unavailable                                                                                          |
| Preconditions          | Chrome is running, and a webpage has loaded successfully. Network connectivity can be disconnected safely.                                                |
| Steps                  | 1. Disconnect network connectivity. 2. Click the Refresh button on the already loaded webpage. 3. Observe the browser response.                            |
| Expected Behavior      | Chrome should handle the failed network request without crashing. The fresh webpage content should not be incorrectly reported as successfully retrieved. |
| Actual Result/Behavior | Not executed yet.                                                                                                                                         |
| Status                 | Not Executed                                                                                                                                              |

**Test Case Execution Summary:**

| Metric              | Count |
| ------------------- | ----- |
| Total Test Cases    | 10    |
| Positive Test Cases | 5     |
| Negative Test Cases | 5     |
| Executed            | 0     |
| Passed              | 0     |
| Failed              | 0     |
| Not Executed        | 10    |

### **Q28. Write five positive and five negative test cases for RAID.**

**Answer:**

RAID testing is performed to verify whether the RAID Controller or Storage Array is working according to the defined RAID requirements.

We need to verify RAID creation, drive compatibility, RAID status, data accessibility and fault handling.

For these examples, we assume a supported hardware RAID controller and compatible drives.

The minimum drive requirements used are:

- RAID 0 – 2 drives.
- RAID 1 – 2 drives.
- RAID 5 – 3 drives.

The tests should be performed using dedicated test drives without production data.

**A. Positive Test Cases**

**TC01 – Verify RAID 0 Creation**

| Field                  | Details                                                                                                                                                              |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_001                                                                                                                                                          |
| Summary                | Verify RAID 0 creation using two compatible drives                                                                                                                   |
| Preconditions          | RAID Controller is detected and healthy. Two compatible Unconfigured Good drives are available. No existing data needs preservation on these drives.                 |
| Steps                  | 1. Log in to the RAID Controller management utility. 2. Identify two available drives. 3. Select RAID 0. 4. Submit RAID creation. 5. Check the Virtual Drive status. |
| Expected Behavior      | RAID 0 should be created successfully and enter the expected healthy state. The configured capacity should be available.                                             |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                    |
| Status                 | Not Executed                                                                                                                                                         |

**TC02 – Verify RAID 1 Creation**

| Field                  | Details                                                                                                                                                    |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_002                                                                                                                                                |
| Summary                | Verify RAID 1 creation using two compatible drives                                                                                                         |
| Preconditions          | RAID Controller is detected and healthy. Two compatible drives are available. Both drives meet the supported RAID 1 requirements.                          |
| Steps                  | 1. Open RAID management utility. 2. Select two available drives. 3. Select RAID 1. 4. Submit the configuration. 5. Verify RAID status and usable capacity. |
| Expected Behavior      | RAID 1 should be created successfully. Both drives should participate in mirroring, and the Virtual Drive should enter the expected healthy state.         |
| Actual Result/Behavior | Not executed yet.                                                                                                                                          |
| Status                 | Not Executed                                                                                                                                               |

**TC03 – Verify RAID 5 Creation**

| Field                  | Details                                                                                                                                                               |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_003                                                                                                                                                           |
| Summary                | Verify RAID 5 creation using three compatible drives                                                                                                                  |
| Preconditions          | RAID Controller is detected and healthy. Three compatible drives are available. All drives satisfy the controller's RAID 5 requirements.                              |
| Steps                  | 1. Open RAID management utility. 2. Select three compatible drives. 3. Select RAID 5. 4. Submit the configuration. 5. Verify the RAID Group and Virtual Drive status. |
| Expected Behavior      | RAID 5 should be created successfully with distributed parity and the expected usable capacity. The RAID Group should enter the healthy state.                        |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                     |
| Status                 | Not Executed                                                                                                                                                          |

**TC04 – Verify Virtual Drive Creation on a RAID Group**

| Field                  | Details                                                                                                                                                                                                                                   |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_004                                                                                                                                                                                                                               |
| Summary                | Verify creation of a Virtual Drive or logical volume using an existing RAID Group                                                                                                                                                         |
| Preconditions          | A healthy RAID Group exists. Sufficient free capacity is available. RAID Controller management access is available.                                                                                                                       |
| Steps                  | 1. Open RAID management utility. 2. Select the healthy RAID Group or available drive group. 3. Select Create Virtual Drive. 4. Enter the required capacity and configuration. 5. Submit the request. 6. Verify the Virtual Drive details. |
| Expected Behavior      | A Virtual Drive should be created successfully with the requested configuration and capacity.                                                                                                                                             |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                                                                                         |
| Status                 | Not Executed                                                                                                                                                                                                                              |

**TC05 – Verify RAID Health and Read/Write Operations**

| Field                  | Details                                                                                                                                                                                                                               |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_005                                                                                                                                                                                                                           |
| Summary                | Verify RAID health and data accessibility after successful RAID creation                                                                                                                                                              |
| Preconditions          | A RAID Group and Virtual Drive have been created successfully. The Virtual Drive is accessible to the test host. Initialization has completed, or the controller reports an operational state that supports host I/O. A safe test area is available. |
| Steps                  | 1. Check RAID Group status. 2. Check Virtual Drive status and initialization progress. 3. Wait until initialization completes or the controller reports an operational state that supports host I/O, as defined by the product requirements. 4. Verify the logical device is detected by the OS. 5. Perform controlled write operations in the designated safe test area. 6. Read back the written data. 7. Compare the read data with the written data. |
| Expected Behavior      | RAID should remain in the expected healthy state. I/O should begin only after the product-defined initialization/operational condition is reached. Read/write operations should complete successfully, and the retrieved data should match the written data. |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                                                                                     |
| Status                 | Not Executed                                                                                                                                                                                                                          |

**B. Negative Test Cases**

**TC06 – Verify RAID 5 Creation with Insufficient Drives**

| Field                  | Details                                                                                                                                                              |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_006                                                                                                                                                          |
| Summary                | Verify RAID 5 creation is rejected when fewer than the minimum required drives are selected                                                                          |
| Preconditions          | RAID Controller is detected and healthy. Only two compatible available drives are present.                                                                           |
| Steps                  | 1. Open RAID management utility. 2. Select two available drives. 3. Attempt to create RAID 5. 4. Observe the controller response.                                    |
| Expected Behavior      | RAID 5 creation should be rejected because the minimum requirement of three drives is not satisfied. An appropriate error or validation message should be displayed. |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                    |
| Status                 | Not Executed                                                                                                                                                         |

**TC07 – Verify RAID Creation Without Selecting Drives**

| Field                  | Details                                                                                                                                                                |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_007                                                                                                                                                            |
| Summary                | Verify RAID creation is rejected when no physical drives are selected                                                                                                  |
| Preconditions          | RAID Controller is detected and healthy. RAID management utility is accessible.                                                                                        |
| Steps                  | 1. Open RAID management utility. 2. Navigate to RAID creation. 3. Select a supported RAID level. 4. Do not select any physical drives. 5. Submit the creation request. |
| Expected Behavior      | The controller should reject the request and display an appropriate validation message. No RAID Group or Virtual Drive should be created.                              |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                      |
| Status                 | Not Executed                                                                                                                                                           |

**TC08 – Verify RAID Degraded State After a Drive Failure**

| Field                  | Details                                                                                                                                                                                                                                                         |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_008                                                                                                                                                                                                                                                     |
| Summary                | Verify RAID enters Degraded state when one drive fails in a redundant RAID configuration                                                                                                                                                                        |
| Preconditions          | A healthy RAID 5 configuration or a healthy RAID 1 configuration consisting of exactly two mirrored drives exists. The array contains test data. The controller and drive bay support the planned failure simulation or hot-swap procedure. |
| Steps                  | 1. Verify that the RAID Group is healthy. 2. Identify a member drive. 3. Simulate its failure using a supported method or remove it according to the hardware service procedure. 4. Check the RAID Group status. 5. Verify whether the data remains accessible. |
| Expected Behavior      | The controller should identify the failed drive. The RAID Group should enter Degraded state while remaining accessible within the RAID level's fault-tolerance limit. An appropriate alert or event should be generated.                                        |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                                                                                                               |
| Status                 | Not Executed                                                                                                                                                                                                                                                    |

**TC09 – Verify Unsupported RAID Configuration Is Rejected**

| Field                  | Details                                                                                                                                                                   |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_009                                                                                                                                                               |
| Summary                | Verify rejection of RAID 6 creation with insufficient drives                                                                                                              |
| Preconditions          | RAID Controller supports RAID 6. Only three compatible drives are available.                                                                                              |
| Steps                  | 1. Open RAID management utility. 2. Select three drives. 3. Select RAID 6. 4. Submit the RAID creation request. 5. Observe the controller response.                       |
| Expected Behavior      | RAID 6 creation should be rejected because four drives are the minimum required. An appropriate error should be reported, and no incomplete RAID Group should be created. |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                         |
| Status                 | Not Executed                                                                                                                                                              |

**TC10 – Verify RAID Behaviour When a Drive Fails During I/O**

| Field                  | Details                                                                                                                                                                                                                                                                                                                                 |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Test Case ID           | RAID_TC_010                                                                                                                                                                                                                                                                                                                             |
| Summary                | Verify RAID handles a single drive failure during an active I/O workload                                                                                                                                                                                                                                                                |
| Preconditions          | A healthy RAID 5 test configuration exists. The Virtual Drive is accessible to the test host. Test data is available. The controller supports the planned drive-failure simulation or hot-swap procedure.                                                                                                                               |
| Steps                  | 1. Verify RAID 5 is in a healthy state. 2. Start a controlled read/write workload on the Virtual Drive. 3. Simulate the failure or supported hot removal of one member drive. 4. Monitor RAID Controller events and logs. 5. Check the RAID Group state. 6. Verify data accessibility. 7. Stop the workload and inspect data integrity. |
| Expected Behavior      | The controller should report the failed drive and transition RAID 5 into Degraded state. Since a single drive failure is within RAID 5 fault tolerance, the array should remain accessible. Any I/O errors during transition should be recorded and investigated. No silent data corruption should occur.                               |
| Actual Result/Behavior | Not executed yet.                                                                                                                                                                                                                                                                                                                       |
| Status                 | Not Executed                                                                                                                                                                                                                                                                                                                            |

**Test Case Execution Summary:**

| Metric              | Count |
| ------------------- | ----- |
| Total Test Cases    | 10    |
| Positive Test Cases | 5     |
| Negative Test Cases | 5     |
| Executed            | 0     |
| Passed              | 0     |
| Failed              | 0     |
| Not Executed        | 10    |

**Important RAID Testing Precautions:**

- Use dedicated test drives.
- Do not perform destructive RAID testing on drives containing production data.
- Confirm drive slot identification before removing a drive.
- Check RAID fault tolerance before simulating a failure.
- Record controller logs and event information.
- Verify data integrity after fault-injection testing.
- Follow the hardware vendor's hot-swap and recovery procedures.

# **Section 4 – Build, Test Execution and Defect Management**

### **Q29. What is a Build? What are DUT and SUT? How is a build released to testers?**

**Answer:**

**Build:**

A build is a working version of software or firmware created by developers.

Whenever developers implement new functionality, fix defects or make changes to existing code, they generate a new build and release it to testers.

For software, source code such as C/C++ is compiled into an executable.

For hardware devices, firmware is commonly provided as a binary file such as `.bin`.

**DUT – Device Under Test:**

DUT means Device Under Test.

It is the hardware device on which we perform testing.

**SUT – System Under Test:**

SUT means System Under Test or Software Under Test.

It is the complete system or software application that we are testing.

**How do developers release a build?**

According to my notes, developers can release builds through:

1. JIRA tools.
2. Shared servers.
3. Jenkins.
4. Shared folders.
5. Email.

**Example:**

A firmware developer fixes a drive initialization defect and generates a new firmware build.

The developer shares the build with the validation team. Testers install the build on the DUT and execute the relevant test cases.

### **Q30. Explain the testing workflow from receiving a new build to executing test cases.**

**Answer:**

The testing workflow is:

**Step 1 – Receive the Build**

Developers release a new software or firmware build.

**Step 2 – Understand Changes**

We identify whether the build includes:

- New functionality.
- Defect fixes.
- Changes to existing functionality.

**Step 3 – Identify Impacted Test Cases**

Based on the changes, we identify the test cases that need to be executed.

**Step 4 – Prepare Test Plan**

We select the required test cases from the Master Test Suite and prepare a Test Plan for the release.

**Step 5 – Prepare Test Environment**

We configure the required testbed and ensure the DUT/SUT is ready.

**Step 6 – Install the Build**

We install the received build on the testbed.

**Step 7 – Execute Test Cases**

We execute the planned test cases and record the results.

**Step 8 – Analyze Results**

We compare expected and actual results.

**Step 9 – Raise Defects**

If a test case fails because of product behaviour, we raise a bug and assign it to the developer.

**Step 10 – Verify Fixes**

After the developer provides a new build, we perform retesting and regression testing.

### **Q31. How do you determine whether a test case has Passed or Failed? How do you update and report test results?**

**Answer:**

We determine PASS or FAIL by comparing the actual result with the expected result.

**PASS:**

If all the test case steps execute according to the expected behaviour, we mark the test case as PASS.

**FAIL:**

If one or more steps do not work according to the expected behaviour, we mark the test case as FAIL.

**Example:**

Test Case: Verify Google Chrome launch functionality.

Expected Result: Google Chrome should open successfully.

Actual Result: Google Chrome opens successfully.

Result: PASS.

If Google Chrome does not open, the result is FAIL.

**Updating test results:**

Initially, a test case is in the Not Executed state.

During execution, we update it to In Progress.

After execution, we update the result to PASS or FAIL. If an unmet precondition or dependency prevents execution, we mark it as BLOCKED. If the test case does not apply to the current product or configuration, we mark it as N/A.

**Test Reporting:**

We prepare reports containing:

- Total test cases.
- Executed test cases.
- Passed test cases.
- Failed test cases.
- Defects raised.
- Current testing status.

We share the reports with the relevant team members and stakeholders.

### **Q32. What is a Bug/Defect? Explain the complete Bug Life Cycle.**

**Answer:**

A bug is a deviation from the expected behaviour of a software product.

Whenever a test case fails because the actual result is different from the expected result, we investigate the failure and identify whether it is a product defect.

The Bug Life Cycle describes the different stages through which a defect passes until it is resolved.

**Bug Life Cycle:**
```

Test Case Execution\
|\
PASS/FAIL\
|\
Raise Bug\
|\
NEW\
|\
OPEN\
|\
Assigned to\
Developer\
|\
IN PROGRESS\
|\
FIXED\
|\
Tester Verification\
|\
+------+------+\
\|             |\
Verified       Not Fixed\
\|             |\
CLOSE        REOPEN\
|\
Developer

```

**Explanation:**

1. **New:** Tester identifies and reports the defect.
2. **Open:** Defect is reviewed and accepted for investigation.
3. **Assigned:** Bug is assigned to the responsible developer.
4. **In Progress:** Developer investigates the defect.
5. **Fixed:** Developer implements a fix and provides a new build.
6. **Tester Verification:** Tester executes the failed test case again.
7. **Closed:** If the issue is resolved, tester closes the bug.
8. **Reopened:** If the issue still exists, tester reopens the bug and assigns it back to the developer.

Other possible resolutions include:

- Rejected/Invalid.
- Duplicate.
- Cannot Reproduce.
- Deferred/Won't Fix.
- False Alarm.

### **Q33. What are the different fields of a Bug Report?**

**Answer:**

A Bug Report contains information required to understand, reproduce and investigate a defect.

The important fields are:

1. **Project:** Project in which the defect is identified.
2. **Issue Type:** Bug.
3. **Summary:** Short description of the issue.
4. **Description:** Detailed explanation of the defect.
5. **Steps to Reproduce:** Step-by-step procedure to reproduce the problem.
6. **Expected Result:** Expected behaviour.
7. **Actual Result:** Actual behaviour.
8. **Assignee:** Developer responsible for investigating and fixing the bug.
9. **Environment:** Testbed configuration in which the issue occurred.
10. **Attachment:** Screenshots, logs and other supporting evidence.
11. **Priority:** Urgency with which the issue needs to be fixed.
12. **Severity:** Impact of the defect on product functionality.

**Examples of attachments:**

- Script logs.
- System logs.
- Dump logs.
- Screenshots.

### **Q34. What is the difference between Priority and Severity?**

**Answer:**

**Priority:**

Priority indicates how urgently a developer needs to fix a defect.

It is mainly determined based on business importance and the urgency of the issue.

According to my notes, priority levels are:

1. Blocker.
2. Critical.
3. Major.
4. Minor.
5. Trivial.

**Severity:**

Severity indicates how seriously the bug affects product functionality.

According to my notes:

- Severity 1 – Highest.
- Severity 5 – Lowest.

**Difference:**

| Priority                                           | Severity                                                  |
| -------------------------------------------------- | --------------------------------------------------------- |
| Indicates urgency of fixing the bug                | Indicates impact of the bug                               |
| Usually determined with business and project input | Usually assessed based on technical and functional impact |
| Helps decide fixing order                          | Helps understand seriousness                              |
| Blocker, Critical, Major, Minor, Trivial           | Severity 1 to 5 in the notes                              |

### **Q35. Explain High Priority–High Severity, Low Priority–Low Severity, High Priority–Low Severity and Low Priority–High Severity with examples.**

**Answer:**

**1. High Priority – High Severity**

The defect has a serious impact on product functionality and must be fixed immediately.

Examples:

- Payment transaction failure.
- Security breach exposing customer data.
- Production application becoming completely unavailable.

**2. Low Priority – Low Severity**

The defect has minimal impact and does not affect important product functionality.

Examples:

- Typo in a support email.
- Minor icon mismatch.
- Small cosmetic issue.

**3. High Priority – Low Severity**

The defect has a relatively small technical impact but needs immediate correction because of its business or customer importance.

Examples:

- Incorrect company logo displayed on the homepage.
- Outdated message displayed to customers.
- Notification showing incorrect content.
- Broken links on an important webpage.

**4. Low Priority – High Severity**

The defect has a serious functional impact but occurs in a rarely used feature or a less frequently accessed area.

Examples:

- Rare feature crashes the application.
- Security issue affecting an isolated feature.
- Failure in an administration-only function.

**Important:** Priority and severity are assessed based on the actual business context and product impact. They are not always directly proportional.

### **Q36. What do the bug resolutions Duplicate, Won't Fix, Cannot Reproduce and Deferred mean?**

**Answer:**

**1. Duplicate:**

If the same bug has already been reported by another tester or engineer, the developer marks the new bug as Duplicate.

Example: Two testers report the same login failure.

The second report is linked to the already existing bug.

**2. Won't Fix:**

If the development team decides not to fix the reported issue, the defect can be marked Won't Fix.

It may be because the issue is not considered important enough to fix or the expected behaviour is accepted.

**3. Cannot Reproduce:**

If the developer cannot reproduce the issue using the provided steps or environment, the defect may be marked Cannot Reproduce.

In this case, testers should provide additional logs, steps and environment information.

**4. Deferred:**

If the bug is valid but the developer plans to fix it in a future release, it can be marked Deferred for the current release.

### **Q37. When multiple testers report the same issue, how do you identify and avoid duplicate bugs?**

**Answer:**

When multiple testers report the same issue, we should first check the existing bug database before raising another defect.

My approach is:

1. Search the existing bug tracking tool for similar issues.
2. Check the bug summary and description.
3. Compare the steps to reproduce.
4. Verify whether the actual and expected results are the same.
5. Check the affected functionality and environment.
6. If the issue is the same, update the existing bug or link the new finding to it.
7. Raise a new bug only when the issue is genuinely different.

This avoids duplicate bug reports and unnecessary work for developers and testers.

### **Q38. What is the tester's approach when a developer closes a bug as Invalid?**

**Answer:**

If a developer closes a bug as Invalid, I first verify the reported issue again.

My approach is:

1. Review the bug description.
2. Verify the requirement or Functional Verification Document.
3. Execute the same steps again.
4. Check the expected and actual behaviour.
5. Collect supporting evidence such as screenshots and logs.
6. Verify whether the issue is genuinely valid.
7. Discuss the issue with the developer and provide the evidence.
8. If the issue is reproducible and violates the requirement, request reopening or reassigning the bug through the agreed defect management process.

If the behaviour is actually correct according to the requirement, I will accept the Invalid resolution.

### **Q39. What are the debugging steps you follow when a Test Case fails?**

**Answer:**

Whenever a test case fails, I follow a systematic debugging approach.

**Step 1 – Verify the Failure**

I execute the failed test case again and confirm whether the failure is reproducible.

**Step 2 – Check Expected and Actual Results**

I compare the expected result with the actual result and identify the exact deviation.

**Step 3 – Check Test Steps**

I verify whether all test case steps were executed correctly.

**Step 4 – Check the Test Environment**

I verify the testbed configuration, hardware connections, build version and other setup requirements.

**Step 5 – Check Logs**

I collect and analyse the relevant logs, screenshots and diagnostic information.

**Step 6 – Identify the Failure Category**

I investigate whether the issue is related to:

- Script.
- Test setup.
- Product functionality.

**Step 7 – Reproduce and Isolate**

I try to reproduce the issue and isolate the failure condition.

**Step 8 – Raise a Bug**

If it is a product issue, I create a bug with the reproduction steps, expected and actual results, environment details and supporting evidence.

### **Q40. How do you determine whether a test failure is caused by a Script Issue, Setup Issue or Product Issue?**

**Answer:**

Whenever a test case fails, we should not immediately conclude that the product has a defect.

First, we need to identify the failure source.

**1. Script Issue:**

A script issue occurs when the automation script itself is incorrect.

Examples:

- Incorrect command.
- Wrong input parameters.
- Incorrect validation logic.
- Wrong expected result defined in the script.

Approach:

- Review the automation script.
- Execute the same operation manually.
- Compare the manual result with the automation result.
- Correct the script if the product works manually.

**2. Setup Issue:**

A setup issue occurs when the test environment is not configured correctly.

Examples:

- Incorrect hardware connections.
- Missing device configuration.
- Incorrect testbed settings.
- Required services not running.

Approach:

- Verify the test environment.
- Check the hardware connections.
- Verify the configuration.
- Reconfigure the testbed if required.
- Execute the test case again.

**3. Product Issue:**

A product issue occurs when the product does not behave according to the expected requirements even though the test script and setup are correct.

Approach:

- Verify the requirement.
- Reproduce the issue.
- Execute the test manually if needed.
- Collect relevant logs and evidence.
- Raise a defect with complete reproduction steps.

**Summary:**

| Failure Type  | Main Investigation                                  |
| ------------- | --------------------------------------------------- |
| Script Issue  | Validate automation code and execution logic        |
| Setup Issue   | Validate test environment and configuration         |
| Product Issue | Validate product functionality against requirements |

### **Q41. How do you avoid work backlogs and ensure testing activities are completed on time?**

**Answer:**

To avoid work backlogs, we need proper planning, prioritization and continuous tracking of testing activities.

My approach is:

1. Prepare a clear Test Plan.
2. Divide work into manageable tasks.
3. Prioritize important and critical test cases.
4. Assign responsibilities to team members.
5. Track daily progress.
6. Identify blockers as early as possible.
7. Communicate delays and dependencies to the team.
8. Complete high-priority testing activities first.
9. Move incomplete work into the backlog and plan it appropriately in the next sprint.
10. Review progress regularly during daily Scrum meetings.

This helps us maintain a clear understanding of pending work and complete testing activities according to the release schedule.

# **Section 5 – Agile and Scrum Methodology**

### **Q42. What is Agile? Explain its principles and approach to software development.**

**Answer:**

Agile is a software development methodology in which development happens iteratively and incrementally.

It focuses on collaboration between developers, testers and customers.

In the Agile model, requirements can evolve during development, and coding and testing happen in parallel.

**Main principles covered in my notes:**

1. Customer collaboration.
2. Continuous communication between team members.
3. Iterative development.
4. Frequent delivery of working software.
5. Coding and testing in parallel.
6. Continuous feedback and improvement.

**Example:**

Suppose we are developing a storage management application.

Instead of developing the complete application at once, we divide the work into smaller sprints.

In each sprint, developers implement some functionality, testers verify it, and the team reviews the results.

This allows the team to identify defects and make improvements continuously.

### **Q43. What is the difference between the Waterfall Model and Agile Model?**

**Answer:**

According to my notes, Waterfall and Agile are two different software development models.

**Waterfall Model:**

Waterfall is a sequential software development model.

We complete one phase before moving to the next phase.

The stages are:

1. Idea.
2. Design.
3. Coding.
4. Testing.
5. Release.
6. Support.
7. End of Life.

**Agile Model:**

Agile is an iterative development model.

Development and testing activities happen in parallel, and requirements can evolve through collaboration with customers.

| Waterfall Model                                      | Agile Model                                      |
| ---------------------------------------------------- | ------------------------------------------------ |
| Sequential development                               | Iterative development                            |
| One phase is completed before moving to the next     | Work is divided into sprints                     |
| Changes are difficult after moving to the next phase | Changes can be incorporated during development   |
| Development and testing happen in separate stages    | Coding and testing happen in parallel            |
| Suitable for projects with stable requirements       | Suitable for projects with changing requirements |

### **Q44. What is Scrum? What are the responsibilities of a Scrum Master?**

**Answer:**

Scrum is a framework consisting of rules and standards used to implement Agile methodology.

It helps teams organize development and testing activities into smaller iterations called sprints.

**Scrum Master:**

A Scrum Master is responsible for creating and managing the sprint process.

Responsibilities mentioned in my notes include:

1. Creating and managing sprints.
2. Creating user stories and subtasks.
3. Organizing daily Scrum meetings.
4. Conducting sprint planning meetings.
5. Discussing work assignments with team members.
6. Monitoring sprint progress.
7. Helping the team identify and resolve blockers.

The Scrum Master coordinates with developers, testers, team leads and other team members.

### **Q45. What is a Sprint? Explain Sprint duration and how work is planned.**

**Answer:**

A Sprint is a fixed duration of time during which an assigned set of tasks or requirements is completed.

According to my notes, the sprint duration is generally 2 to 3 weeks.

For example:

- Week 1 – Sprint 1.
- Week 2 – Sprint 1.
- Week 3 – Sprint 2.

**Sprint Planning Process:**

1. Scrum Master conducts the sprint planning meeting.
2. Product Owner or Team Lead discusses requirements.
3. User stories are selected for the sprint.
4. Subtasks are created for each user story.
5. Tasks are assigned to developers and testers.
6. Sprint execution starts.
7. Team members update their task status.
8. After completing the work, subtasks and user stories are closed.
9. Sprint review and retrospective activities are performed.

### **Q46. What are Epic, User Story and Subtask? Explain with examples.**

**Answer:**

**1. Epic:**

An Epic is a large requirement or functionality that contains multiple related user stories.

According to my notes, an Epic can be created once during a project lifecycle or at the beginning of a major project phase.

**2. User Story:**

A User Story is a description of the type of work or functionality that needs to be completed by the team.

It acts as a template describing the requirement to be implemented or tested.

**Example:**

As a tester, I want to verify RAID creation functionality so that I can confirm whether the storage system creates RAID groups correctly.

**3. Subtask:**

A Subtask is a smaller part of a User Story.

Each engineer can be assigned separate subtasks to complete the work.

**Example:**

User Story: Verify RAID functionality.

Subtasks:

- Subtask 1: Prepare RAID test cases.
- Subtask 2: Configure the test environment.
- Subtask 3: Execute RAID test cases.
- Subtask 4: Prepare the test report.

### **Q47. What are Story Points? Why do we use them in Agile?**

**Answer:**

Story Points are used in Agile to estimate the relative effort or complexity required to complete a user story.

According to my notes, story points are assigned based on the priority and importance of the particular work.

**Example:**

Suppose we have three user stories:

| User Story                          | Story Points |
| ----------------------------------- | ------------ |
| Verify basic functionality          | 2            |
| Execute regression testing          | 5            |
| Perform complex performance testing | 8            |

Higher story points generally indicate that the task requires more effort or complexity.

We use story points to:

1. Estimate the effort required.
2. Plan sprint workloads.
3. Compare the relative complexity of tasks.
4. Understand the team's capacity.

*Additional clarification:* Story points are primarily estimates of relative effort, complexity and uncertainty; they are not a direct measure of priority or working hours.

### **Q48. What is a Product Backlog and Sprint Backlog? Explain Sprint Planning, Daily Scrum/Stand-up, Sprint Review and Retrospective meetings.**

**Answer:**

**1. Product Backlog:**

A Product Backlog is a prioritized list of requirements, features, improvements and defects that need to be completed for the product.

It contains the overall pending work for the product.

**2. Sprint Backlog:**

A Sprint Backlog contains the selected user stories and tasks that the team plans to complete during a particular sprint.

According to my notes, backlog also refers to remaining work from the current sprint that can be moved to the next sprint when it cannot be completed.

**3. Sprint Planning Meeting:**

Sprint Planning happens before starting a sprint.

During this meeting:

- Scrum Master participates.
- Product Owner discusses requirements.
- Team Lead discusses requirements and priorities.
- User stories are selected.
- Subtasks are created and assigned.

**4. Daily Scrum / Stand-up Meeting:**

It is a daily meeting conducted by the Scrum Master.

Team members discuss:

- What work they completed yesterday.
- What work they plan to do today.
- What issues or blockers they are facing.

Developers and testers participate in the meeting.

**5. Sprint Review Meeting:**

A Sprint Review is conducted at the end of a sprint.

The team presents and reviews the completed work and checks whether the sprint objectives have been achieved.

**6. Retrospective Meeting:**

A Retrospective Meeting is conducted after the sprint.

The team discusses:

- What went well in the previous sprint.
- What did not go well.
- What problems occurred.
- What improvements are required for the next sprint.

**Example:**

Suppose we completed a two-week sprint for RAID functionality validation.

During the retrospective meeting, the team discusses test execution delays, environment issues, defects and automation improvements before planning the next sprint.

# **Testing – Final Completion Summary**

## **Important concepts to retain for interviews**

The following concepts are particularly important across the question bank:

| Concept            | Key point                                              |
| ------------------ | ------------------------------------------------------ |
| Manual Testing     | Testing without depending on automation scripts        |
| Automation Testing | Executing test cases using scripts or tools            |
| White Box Testing  | Testing with knowledge of internal code                |
| Black Box Testing  | Testing without internal code knowledge                |
| Grey Box Testing   | Combination of White Box and Black Box                 |
| SDLC               | Complete software development lifecycle                |
| STLC               | Complete software testing lifecycle                    |
| Regression Testing | Checking existing functionality after changes          |
| Retesting          | Verifying previously failed test cases after fixes     |
| Smoke Testing      | Basic build verification                               |
| Sanity Testing     | Focused testing of important or impacted functionality |
| Test Scenario      | High-level functionality to test                       |
| Test Case          | Detailed steps to verify functionality                 |
| Test Plan          | Planned testing activities for a release               |
| Test Suite         | Collection of test cases                               |
| RTM                | Mapping requirements to test cases                     |
| Priority           | Urgency of fixing a defect                             |
| Severity           | Impact of a defect                                     |
| Agile              | Iterative development methodology                      |
| Scrum              | Framework used to organize Agile work                  |
| Sprint             | Fixed period for completing planned work               |

**Testing preparation is complete.**
```
