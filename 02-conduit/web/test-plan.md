# Test Plan — Conduit

> Documento original em inglês (convertido de .docx).

## Introduction

The “Conduit” application is designed as an open-source application to train software development and testing skills. The main website functionality includes registration and sign-in, posting articles on different topics, reading articles, the ability to like an article, posting a comment, and following users.

The Test Plan is designed to prescribe the scope, approach, resources, and schedule of all testing activities of the “Conduit” website.

The plan identifies the features to be tested, the types of testing to be performed, the resources and schedule required to complete testing, and the risks associated with the plan.

## 1. Test strategy

### 1.1 Testing scope

#### 1.1.1 Features to be tested

| Module name | Login type | Description |
|---|---|---|
| Conduit logo | Logged in<br>Logged out |  |
| Home | Logged in<br>Logged out |  |
| Sign in |  |  |
| Publishing Articles | Logged in | Create, edit, and delete articles. |
| Comments | Logged in | Add, edit, and remove comments. |
| Follow Users | Logged in | Follow/unfollow users and display feed correctly. |
| Favorites and Likes | Logged in | Add/remove favorite articles and like posts. |

#### 1.1.2 Out of test scope

These areas are out of scope for this testing cycle:

- Website Security

- Website Performance

- Website API testing

- Test Automation

### 1.2 Test types

In this testing cycle, the Conduit website will be tested using the next testing types:

- System testing: all the testing will be conducted on a complete, integrated system to evaluate the system's compliance with its specified requirements.

  - Exploratory testing.

  - Smoke testing for each new build.

  - Functional testing of all the features

  - GUI testing

  - Compatibility testing: test only Windows and MacOS browsers

### 1.3 Risks and Issues

| Risk | Mitigation |
|:--:|:--:|
| Team members lack the required skills for website testing | Rapid training before the start of the testing cycle. |
| Not enough time to test all browsers and OS. | Prioritize testing on the most widely used browsers and operating systems. |
| Not enough time to execute all test scenarios. | Focus on critical cases with the greatest impact on users. |
| A member of the team has got sick | Ensure that another member is familiar with critical tasks. |

### 1.4 Test Logistics

#### 1.4.1 Who will test?

• QA Team: Responsible for creating and executing test cases.

• Mentors: Reviewing test cases and providing support on technical issues.

#### 1.4.2 When will the testing occur?

The team will start the testing after:

• Testing will begin after the MVP development is complete and a stable version of the system is available.

• The testing cycle will follow the schedule described in the timeline.

## 2. Test objective

The test objectives are to verify the functionality and API of the Conduit app. The testing should be focused on the flow of publishing articles and sharing information between members. The main features are authorization, posting new articles, following members, saving favorite articles on their pages, adding likes, and writing comments. Testing should be done on preselected versions of browsers and mobile devices described in the "System resource" section.

## 3. Test criteria

#### 3.1 Suspension criteria

- 10% of P0/P1 tests failed, which should lead to the testing suspension until the development team fixes all the corresponding bugs.

- 30% of P2/P3 tests failed, which should lead to the testing suspension until the development team fixes all the corresponding bugs.

#### 3. 2 Exit criteria

The test execution will be stopped no later than the last day of the sprint. The exit criteria should be met to complete the testing cycle:

- The mandatory Execution rate is 95%.

- The mandatory Pass rate is 100% for P0/P1 tests.

- The mandatory Pass rate is 80% for P2/P3 tests.

- All necessary artifacts collected: test cases, and bug reports.

- The product should not have known bugs with severity Critical and Major and bugs with Priority High at the time of finishing testing.

- The list of allowed bugs is agreed upon with the developers and managers.

## 4. Resource planning

### 4.1 System resources

| No. | Resources | Description                                                  |
|-----|-----------|--------------------------------------------------------------|
| 1   | Browser   | Google Chrome, Mozilla Firefox and Safari (latest versions). |
| 2   | Network   | Stable connection of at least 10 Mb/s.                       |
| 3   | Computer  | Windows 10+, macOS 11+, Ubuntu 20.04+.                       |

### 4.2 Human resources

| No. | Resources | Description of tasks |
|---|---|---|
| 1 | QA members | • Create test cases, execute tests, and report bugs. |
| 2 | Mentors | • Review test cases and validate execution. |

## 5. Test environment

Testing should be conducted in the production environment. To run the app locally for working with DB we will use Docker.

*(O diagrama genérico de arquitetura cliente-servidor do documento original foi omitido.)*

## 6. Schedule & estimation 

### 6.1 All project tasks and estimation

| Task | Members | Estimate effort |
|----|----|----|
| Create Test plan | QA members | 3 man-hour |
| Create decomposition, decision table, state transition diagram | QA members | 5 man-hour |
| Create Test cases | QA members | 5 man-hour |
| Review Test cases | Mentors | 2 man-hour |
| Test cases execution | QA members | 8 man-hour |
| Create Bug reports | QA members | 4 man-hour |
| Writing test report | QA members | 3 man-hour |

### 6.2 Schedule to complete these tasks

| Task | 1-st Sprint | 2-nd Sprint | 3-rd Sprint |
|---|---|---|---|
| Create Test plan | ✔ |  |  |
| Create decomposition, decision table, state transition diagram | ✔ |  |  |
| Create Test cases |  | ✔ | ✔ |
| Review Test cases |  | ✔ | ✔ |
| Test cases execution |  |  | ✔ |
| Create Bug reports |  |  | ✔ |
| Writing and preparing test results |  |  | ✔ |

## 7. Test deliverables

### 7.1 Before the testing phase

- Approved Test Plan.

- Test Cases created and reviewed.

### 7.2 During the testing

- Test Cases Execution.

- Bug Reports Generated.

### 7.3 After the testing cycle is over

- Final Report Consolidating Results.

- List of Suggested Improvements.
