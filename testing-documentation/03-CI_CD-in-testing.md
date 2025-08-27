# ⚙️ CD/CD in Testing Context?

## 🏛️ What is CI/CD?
- **Continuous Integration (CI)** developers integrate code frequently (daily or multiple times per day). Automated builds and tests run to detect issues early.
- **Continuous Delivery (CD)**  ensures code is always in a deployable state through automated testing and packaging.
- **Continuous Deployment (CD)** extends delivery by automatically deploying to production after passing tests.

---

##🧪 Role Testing in CI/CD
Testing in the backbone of CI/CD. Every pipeline stage has different types of tests:
1. Unit tests (CI stage)
  - Run after every commit/pull request.
  - Validates small pieces of code.
  - Provide fast feedback.
2. Integration Test (CI/CD stage)
  - Run after successful unit tests.
  - Validate interaction between modules, services, and external systems.
  - Ensure APIs, databases, and components with mocked together correctly.
  - Often require a test environment with mocked or real dependences.
3. System & End-to-End Tests (CD stage)
  - Run before deploying to staging/production.
  - Validate user workflows across the entire system.
  - Example: "Login -> Add to product to cart -> Checkout."
4. Non-functional Tests
  - Performance, security, usability test often integrated into pipelines before release.

---

## 🔁 How to integration Testing Fits in CI/CD
- Runs in a dedicated CI pipeline stage (after unit tests).
- Uses tests doubles (mocks/stubs) for unavaible services, or runs with containers for real dependencies.
- Example flow:
1. Developer commit code.
2. CI pipeline runs units tests.
3. Integration test stage spins up Docker containers (database, services).
4. Automated integration test validate module interactions.
5. If all pass -> build moves forward.

This ensure fail fast -> issues in service communication are caught before stagins.

---

## 🛠️ Popular Tools in the Market
### CI/CD Orchestration
- **Jenkins** -> Open source, highly customizable.
- **GitHub Actions** -> Built into GitHub repos, integrates easily with workflows.
- **GitLab** -> Integrated into GitLab, powerful pipelines witth YAML configs.
- **CircleCI** -> Cloud based, easy stup for modern pipelines.
- **Azure DevOps Pipelines** -> Microsoft ecosystem CI/CD solution.

### Testing Tools Integrated in CI/CD
- **Unit Testing** -> JUnit (Java), pytest (Python), NUnit (C#), Mocha/Jest (JavaScript).
- **Integration Testing** -> Postman/Newman, Rest Assured, Karate, WireMock (for stubbing).
- **UI/E2E Testing** -> Selenium, Cypress, Playwright.
- **API Mocking & Virtualization** -> WireMock, MockServer, Hoverfly.
- **Performance Testing** -> JMeter, Gatling, Locust.
- **Security Testing** -> OWASP ZAP, SonarQube, Synk.

### Container & Environment Setup
- **Docker & Docker Compose** -> Spin up databases, services for integration tests.
- **Kubernetes** -> Run tests against cloud-native environments.
- **Testcontainers** (Java, Python, etc.) -> Run lightweight containers for integration testing inside test code.

---

## Example: CI/CD Pipeline with Integration Testing (Using GitHub Actions)
```
name: CI Pipeline

on: [push, pull_request]

jobs:
  buid-and-test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      # Run unit tests
      - name: Run Unit Tests
        run: ./gradlew test

      # Spin up DB for integration tests
      - name: Start Services with Docker Compose
        run: docker-compose up -d

      # Run integration tests
      - name: Run Integrations Tests
        run: ./gradlew integrationTest

      # Run end-to-end tests (Selenium example)
      - name: Run E2E Tests
        run: ./gradlew test
```

---

## 🎯 Benefits of CI/CD in Testing
- **Faster feedback loop** -> Detect defects earlier.
- **Consistency** -> Same tests run across all environments.
- **Reduced risk** -> Each stage adds confidence before release.
- **Scalability** -> Parallel testing across multiple environments.
- **Quality gates** -> Block faulty builds before reaching production.

---

>Summary
>
>CI/CD transforms testing into a continuous, automated, and integrated process. Integration testing is a critical stage that ensures modules, APIs, and services work correctly before code moves to staging and production.


  
