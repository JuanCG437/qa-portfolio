# Introduction to a Software Testing

This brief section will provide an introduction to software testing, where we address concepts of testing with test design techniques, test strategic and approaach, type of testing, testing Levels or Macro-Levels and other concepts.

---

## 📄 Introduction to Concepts Testing
>[Testing](https://github.com/JuanCG437/qa-portfolio/blob/main/testing-documentation/terminology.pdf)
>
> Brief introduction to concepts testing

## 🔎 Test Design Techniques
>[Techniques](https://github.com/JuanCG437/qa-portfolio/blob/main/testing-documentation/test-design-techniques.md)
>
> Main application techniques in test design

## 🧩 Test Strategic & Approach
>[Strategic](https://github.com/JuanCG437/qa-portfolio/blob/main/testing-documentation/test-strategic-%26-approach.md)
>
>Brief test strategy and approach

## 📐 Test Plannification and Management
>[]()

---

## Test Automation Pyramid
The testing pyramid is a concept in software testing that illustrates how different types of automated test should be balanced in a project to ensure efficiency, maintainability, and fast feedback.
It was introduced by **Mike Cohn** in his book *Secceeding with Agile.*

### 📐 Structure of the Testing Pyramid:
The pyramid is typically dividied into three layers:

**1. Unit Test (Base of Pyramid)**
- ✅ Largest number of test.
- Test individual components, functions, or classes in isolation.
- Fast to run and easy to maintain.
- Example: Testing a method that calculates discounts in a shopping cart.

**2. Integration Tests (Middle layer)**
- ⚖️ Moderate number of tests.
- Validate how different components or modules work together.
- Slower that unit tests, but still automated.
- Example: Testing that your API correctly communicates with a database.

**3. End-To-End (E2E) or UI Tests (Top of the pyramid)**
- 🔝 Fewest test.
- Test the system as a whole, from the user interface down through the backend.
- Provide confidence that the entire workflow functions, but are slow and fragile if overused.
- Example: Testing that a user can log in, add an item to the cart, and complete a purchase.

<p align="center">
<img width="500" height="280" alt="pyramid testing simplified" src="https://global-uploads.webflow.com/619e15d781b21202de206fb5/6316d9e765cd53d9937e2b6a_The-Testing-Pyramid-Simplified-for-One-and-All.webp" />
<br/>
  <sub>© Image source: Webflow Global Uploads</sub>
</p>

## 📊 Why the Pyramid Shape?
- **Wide base** = lots of fast, reliable unit tests.
- **Narrow top** = fewer slow, brittle E2E/UI tests.
- The idea is to **get quick feedback** from unit and integration tests, and only rely on expensive E2E tests for critical workflows.

## ✅ Benefits
- Faster feedback cycles.
- Lower maintenance costs (fewer flaky tests).
- Balanced test coverage (confidence without excessive overhead).

