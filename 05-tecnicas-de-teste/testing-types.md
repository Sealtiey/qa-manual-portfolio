# Classificação dos tipos de teste

Mapa de tipos de teste organizado por critério de classificação, feito em draw.io. Arquivo original: [`diagramas/testing-types.drawio`](diagramas/testing-types.drawio). Conteúdo original em inglês, transcrito do diagrama.

### Object of Testing

- **Non-Functional** — Evaluates aspects that are not directly related to functionality, but rather how the system behaves.
  - **Security Testing** — Identifies vulnerabilities in the system to protect against attacks.
  - **Usability Testing** — Evaluates the ease of use and user experience.
  - **Compatibility Testing** — Checks if the software works correctly across different devices, browsers, or operating systems.
  - **Reliability Testing** — Measures the stability of the system over time.
- **Functional** — It verifies if the software meets the specified functional requirements. It evaluates what the system does .

### Knowledge of the System

- **Black box** — Without additional tools and knowledge about how system works.
- **White box** — Testing with knowledge about how system work, testing on the code level.
- **Grey box** — Partly knowledge about how system works with some additional tools.

### Levels of the Testing

- **Unit (Component)** — Testing of separate small modules on the code level. Usually by developers.
- **Integration Testing** — Verifies the interaction between components or modules.
- **System Testing** — Tests the complete system, validating integrated functionalities.
- **Acceptance Testing** — Validates if the system meets the client’s/user’s requirements.

### Related to Changes

- **Smoke Test** — Quickly verify if the most critical functions of an application are working. This test is performed on an early build of the code to ensure that the application is stable enough for further detailed testing.
- **Sanity Test** — Verify if the modified or newly added functionalities are working as expected. It is typically performed after a smoke test and before more in-depth testing, such as regression testing.
- **Regression Test** — Ensure that recent changes in the code have not negatively impacted the existing functionalities of the system. It involves re-running previous test cases to confirm that nothing has been broken.
- **Retest** — Verify if a defect that was fixed in a previous version of the system has truly been resolved. It is essentially a repetition of the tests performed earlier, focusing on areas where errors were found.

### Code execution status

- **Static Test** — Static testing involves analyzing the code without executing it. It focuses on reviewing the source code, identifying potential errors such as syntax issues, style problems, security vulnerabilities, or compliance with best practices.

### Basis of Scenarios

- **Negative Test** — Negative testing aims to verify how the system handles invalid inputs or unexpected behaviors. It tests the system’s robustness, ensuring that it does not fail undesirably or present errors when confronted with unexpected data or interactions.
- **Positive Test** — The positive test is based on the premise that the system should function correctly when the user provides valid inputs or performs expected actions. In other words, it validates that the system is meeting the requirements and functioning as expected under normal usage conditions.

### Degree of Automation

- **Manual** — In this case, the tests are performed by a tester manually, without the use of automated tools.
- **Automated** — In this case, tests are performed using tools and automated scripts. These tests can be executed repeatedly without the need for human intervention.

### Level of Preparation

- **Exploratory** — Exploratory testing is performed in three stages: planning, execution, and research. This type of testing is more flexible and is ideal for testing aspects of the product that may not have been anticipated beforehand. The goal is to explore the system in a more creative way and discover flaws that would not be identified in predefined tests.
- **Test Case** — This type of testing is based on specific documentation. The tester follows a set of predefined and documented test cases that describe the conditions and steps required to verify if the software is working correctly.
- **Monkey Test** — Monkey testing is a type of automated testing in which the program explores the system randomly and chaotically. It does not follow a logical sequence or plan but performs random actions in the system, potentially leading to the discovery of unpredictable failures.

### Performance

It measures response time, scalability, and stability under load.

- **Spike Testing** — It evaluates how the system responds to rapid and sudden spikes in load, such as a sudden increase in users or traffic .
- **Stress Testing** — It evaluates how the system handles a load beyond the expected, up to the point of failure.
- **Scalability Testing** — It checks how the system can scale to handle increased load.

### Outros tipos presentes no diagrama

- **Portability Testing** — Tests whether the software can be transferred and executed in different environments.
- **Dynamic Test** — Dynamic testing involves the actual execution of the code in a test environment to verify its behavior. This allows identifying errors that only manifest when the code is running, such as logic errors, integration failures, or performance issues.
- **Load Testing** — It checks how the system behaves with an expected load of users or transactions .
- **Ad-Hoc** — Ad-hoc testing is performed without formal planning. There are no test cases or documentation, and the tester explores the product without a clear direction, aiming to find flaws in an improvised manner.
