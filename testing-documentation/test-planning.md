# Test Planning
Is a crucial process in software testing that involves creating a detailed document outlining the **aproach**, **goals**, **resources**, **timeline**, **and scope of testing activities**. It helps establish testing strategies, allocate resources, and track the overall progress of the testing process. Key components of a test plan include defining objetctives, deliverables, and the testing environment, which ensures all stakeholders are aligned and aware of testing goals.

## 📌 Importance of Designing a Test Plan
Designing a Test plan is a critical step in software testing because it establishes the foundation for how testing activities will be conducted. A well-structured test plan provides:

- **Clarity of scope**: Defines what will be tested and what will not, helping the teams avoid wasted effort.
- **Risk Management**: Identifies potential risks early (e.g., thight deadlines, complex integrations, lack of environments) and allows the QA team to design strategies to mitigate them.
- **Alignment with project goals**: Ensures that testing objectives are consistent with businness requeriments and stakeholder expectations.
- **Resource planning**: Helps determine the tools, environments, and human resources required for effective testing.
- **Quality assurance**: Seets quality standards, acceptance criteria, and metrics for evaluating success.

---

## 📌 Adaptating Scope and Risks Based on the Project
Every project is different, so the test plan must be adaptable:
- **For small or low-risk projects**: Testing can be lighter, with a reduced scope and faster cycles.
- **For large or high-risk projects**: Testing must be more rigorous, covering integration, performance, and security. Risks like scalability or downtime are prioritized.
- **Agile Projects**: Test plans are more dynamic and iterative, continuosly adapting as requeriments envolve.
- **Critical systems (e.g., finance, healthcare)**: Test plans must account for compliance, safety, and strict regulations, so risks are managed with detailed test coverage.

---

## 📝 Test Plan / Example

**1. Introduction**
<br>This document describes the strategy, scope, objectives, and activities for the testing process of the project E-commnerce Web Application. The purpose of this plan is to ensure that the application meets business and technical requirements before release.

---

**2. Objectives**
- Validate that the shopping cart works correctly.
- Ensure the paymwent gateway integrates successfully.
- Verify user registration and login functionalities.
- Confirm that the application is responsesive across devices.

---

**3. Scope**
In Scope ✅
- Functional testing of registration, login, cart, checkout, and payment.
- Integration testing between front-end, API, and database.
- Basic performance testing for load handling.
Out of Scope ❌
- Securyti penetration testing.
- Third-party API stress testing.
- Non-functional testing beyond performance.

---

**4. Risks**
- **High Risk**: Payment gateway downtime may delay testing.
- **Medium Risk**: Limited test data could affect coverage.
- **Low Risk**: UI inconsistencies across browsers.

Mitigation: Create mock payment services, generate synthetic test data, prioritiza browser coverage.

---

**5. Test Strategy**
- **Test Levels**: Unit, Integration, System, E2E.
- **Approach**: Risk-based testing, Agile iterative execution.
- **Automation**: Unit and Integration tests automated (JUnit, Selenium)
- **Manual Testing**: E2E workflows and exploratory testing.

---

**6. Test Design Techniques**
- **Equivalence Partitioning**: Validate input fields (e.g., email, password).
- **Boundary Value Analysis**: Test limits (e.g., cart max items).
- **Decision tables**: Payment success/failure scenarios.
- **State Transition Testing**: User login states (logged in, logged out).

---

**7. Test Cases (Examples)**

|**ID**   |**Title**           |**Steps**  |**Expected Result**  |**Priority**  |
----------|--------------------|-----------|---------------------|--------------|
| TC-001  | User Login Valid   | Enter valid credentials and submit | User redirected to dashboard | High |
| TC-002  | User Login Invalid | Enter wrong password | Error Message displayed | High |
| TC-003  | Add Item to Cart   | Select product, click "Addo to Cart" | Item appears in cart | Medium |
| TC-004  | Checkout Without Address | Try checkout without filling address | Error message prompts user to add it | High |

---

**8. Tools**
- **Unit Testing**: JUnit, NUnit
- **Integration/E2E Testing**: Selenium, Cypress
- **Performance**: JMeter
- **Reporting**: Allure, Extent Reports

---

**9. Deliverables**
- Test Plan Document
- Test Cases & Test Data
- Test Execution Results
- Test Summary Report

