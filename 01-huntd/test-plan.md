> Documento original em inglês (convertido de .docx).

# Test Plan — Huntd

Web Application and Mobile Application

## 1. Project Information

| Item                   | Description                            |
|----------------------------|--------------------------------------------|
| **Project Name**           | Huntd                                      |
| **Application Type**       | Web Application and Mobile Application     |
| **Web Platforms**          | Desktop Web Browser and Mobile Web Browser |
| **Mobile Platform**        | Android or iOS                             |
| **Tester**                 | Part-time Student                          |
| **Test Management Tool**   | TestRail                                   |
| **Defect Management Tool** | Jira                                       |

## 2. Test Objective

**Objective:** Validate the functionality, usability, navigation, validations and access permissions of the Huntd web and mobile applications according to the documented requirements and implicit product requirements.

## 3. Test Scope

### Web Application

- Main Page

- For Companies

- For Engineers

- Authentication / Registration

- Candidates

- Candidate Profile

- Recruiter Profile

- Jobs

- Chats / Messages

- Bonus

- Footer

### Mobile Application

- Login / Authentication

- My Chats

- Candidate Profile

- Recruiter Profile

- Preferences

- Sign Out

## 4. Test Strategy

The application will be tested using functional and exploratory testing based on the documented requirements and the expected behavior of each feature.

Testing will include:

- Functional testing

- UI and layout verification

- Navigation testing

- Form validation

- Input validation

- Authentication testing

- Permission testing

- Link and redirection testing

- Data display verification

- Positive and negative scenarios

- Integration between application features where applicable

## 5. Test Case Design

Test cases will be created in TestRail based on the application requirements and feature decomposition.

For the Web application, all identified features will be covered with test cases.

For the Mobile application, test cases will cover only the features that are implemented in the application, according to the project requirements.

## 6. Permission Testing

Permission testing will verify the access and behavior of application features for different user states and roles:

- Logged-out user

- Candidate

- Recruiter

The permissions will be documented in a separate Permission Testing table.

## 7. Test Environment

### Web

- Desktop web browser

- Mobile web browser

### Mobile

- Android or iOS application

### Tools

- TestRail for test case management and execution

- Jira for defect tracking

## 8. Defect Management

Defects identified during testing will be reported in Jira.

Each defect should contain:

- Summary

- Description

- Steps to reproduce

- Expected result

- Actual result

- Priority

- Evidence, when applicable

- Related feature/story

The corresponding defects will also be linked to the relevant TestRail test results.

## 9. Test Execution

Test cases will be executed in TestRail after the test design phase.

The execution results will be recorded as:

- Passed

- Failed

- Blocked, when applicable

- Not Run, when applicable

Failed test cases will be investigated and corresponding defects will be reported in Jira when a product defect is confirmed.

## 10. Traceability

A Requirements Traceability Matrix (RTM) will be created to establish the relationship between:

**Technical Requirements → Features/Modules → Test Cases**

Separate RTMs will be maintained for the Web and Mobile applications due to their different scopes.

## 11. Test Deliverables

- Test Plan

- Web Decomposition

- Mobile Decomposition

- Permission Testing Table

- Web RTM

- Mobile RTM

- Jira Stories

- Jira Bugs

- Web TestRail Test Cases

- Mobile TestRail Test Cases

- Test Execution Results

- Final Test Report

- Test Summary

## 12. Completion Criteria

Testing will be considered completed after:

- All planned Web test cases have been executed.

- All implemented Mobile features have been covered and tested.

- Test results have been recorded in TestRail.

- Identified defects have been reported in Jira.

- TestRail defects are linked to the corresponding Jira issues.

- Test execution and defect statistics are documented in the Test Summary.
