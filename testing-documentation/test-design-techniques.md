# 🏛️ Categories of Test Deisgn Techniques

Test design techniques are often grouped into three families:

## 1. Black-box techniques (focus on input/output, not code)
- Based on requirements, user stories, or system behavior.
- Test doesn't care about the internal logic.

### Examples:
#### 1. Equivalence Partitioning (EP)
- Divide inputs into grupos where system behavior is the same.
- Test on value from each group.
- Exammple: Age input (1-120 valid). Partitions: below 1 (invalid), 1-120 (valid), above 120 (invalid).

#### 2. Boundary Value Analysis (BVA)
- Defects often occur at edges of ranges.
- Test min, max, just below, just above.
- Example: If password length = 8 - 20 -> test 7, 8, 20, 21.

#### 3. Decision Table Testing
- Used when there are multiple conditions with different combinations.
- Example: Insurance price depends on [Age group] + [Has Accidents?]. Create a table of all conditions outcomes.

#### 4. State Transition Testing
- Checks system behavior when movin between states.
- Example: ATM card -> [Inserted -> PIN entered -> Correct PIN -> Access granted].
Wrong PIN moves to [Blocked] state.

#### 5. Use Case Testing
- Design test from user workflows.
- Example: "Buy item online" -> [Search product -> Add to cart -> Checkout -> Pay -> Confirm].

## 2. White-box Techniques (focus on code/logic)
- Based on the internal structure of the system.
- Often used by developers during unit testing.

Examples: 
**1. Statment Coverage** -> Ensure every line of code runs at least once.
**2. Decision Coverage** -> Ensure every decision (true/false branch) is tested.
**3. Path Testing** -> Validate all possible execution paths.

Examples: If (x>0) {...} else {...} -> need at least two test: one where `x>0`, another where `x<=0`

## 3. Experience-based Techniques (focus on tester's skill/intuition)
- Relies on tester's knowledge, experience, and creativity.

Examples:
**1. Error Guessing** -> Test predicts common failures.
Example: Entering special characters in username field.
**2. Exploratory Testing** -> Simultaneous learning, test design, and execution.
**3. Checklist-based Testing** -> Using known defect patterns or industry execution.
