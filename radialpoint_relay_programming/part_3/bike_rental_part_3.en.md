# Radialpoint Relay Programming
Our assignments are grouped around a bike rental system.

## Behavior Driven Development
Testing in an integral part of creating a successful product.  However, tests are often difficult to write and understand for team members not directly involved in the coding.  Behavior Driven Development (BDD) is an attempt to help with this.  You are asked to write a simple BDD framework that will understand a subset of a common BDD syntax, the Gherkin language.  To keep things simple you will be implementing and testing a basic calculator offering only the four basic operations: addition, subtraction, multiplication and division.

## BDD Syntax
Here is an example of the syntax of a test scenario for our calculator.

```
Scenario: Testing calculator operators
  Given constants:
    | name  | value   |
    | pi    | 3.14159 |
    | e     | 2.71828 |
  When I add 4 to 5
  Then I expect the value 9
  When I multiply -6 by 20
  Then I expect the value -120
  When I subtract $.e to $.pi
  Then I expect the value 0.42331
```

In this scenario, each line is a step to execute by the test framework.  The `Given` step sets a pre-condition, the `When` step executes an operation on the calculator and the `Then` step validate the result (post-condition).  Constants can be defined using the table format above and referenced with the dollar sign symbol `$`.  Each step is on a separate line and the indentation is optional.  The numerical values are only examples.  Your code should work with any float values and any variable names.

## Setup
0. (5%) Create a **readme** file that includes a clear explanation of how to run your command line program written in **your preferred programming language**.  You program must take as a parameter a path to a scenario file.

0. (5%) Display the scenario name that is currently executed (i.e. the text after the `Scenario:` prefix)
```
Executing scenario: Testing calculator addition
```

0. (10%) Implement support for the addition scenario:
```
Scenario: Testing calculator addition
    When I add 4 to 5
    Then I expect the value 9
```
    and display a message stating that the test passed successfully.
```
Executing [Testing calculator addition]
-> When I add 4 to 5
-> Then I expect the value 9 (success)
Scenario [Testing calculator addition] ended successfully
```

0. (10%) Implement support for the subtraction, multiplication and division scenario:
```
Scenario: Testing calculator sub, mult and div
  When I add 4 to 5
  Then I expect the value 9
  When I multiply -6 by 20
  Then I expect the value -120
  When I subtract 1.5 to 3
  Then I expect the value  1.5
  When I divide 100 by 200
  Then I expect the value 0.5
```

    and display a message stating that the test passed successfully.
```
Executing [Testing calculator sub, mult and div]
-> When I add 4 to 5
-> Then I expect the value 9 (success)
-> When I multiply -6 by 20
-> Then I expect the value -120 (success)
-> When I subtract 1.5 to 3
-> Then I expect the value  1.5 (success)
-> When I divide 100 by 200
-> Then I expect the value 0.5 (success)
Scenario [Testing calculator sub, mult and div] ended successfully
```

0. (10%) Implement support for constants
```
Scenario: Testing operation with constants
  Given constants:
    | name  |  value  |
    | pi    | 3.14159 |
    | e     | 2.71828 |
  When I subtract $.e to $.pi
  Then I expect the value 0.42331
```

    and display
```
Executing [Testing operation with constants]
-> When I subtract $.e to $.pi
-> Then I expect the value 0.42331 (success)
Scenario [Testing operation with constants] ended successfully
```

0. (10%) Detect error cases:
```
Scenario: Testing operation with constants
  Given constants:
    | name  |  value  |
    | pi    | 3.14159 |
    | e     | 2.71828 |
  When I subtract $.e to $.pi
  Then I expect the value 999.42331
```
    and display a message stating the step that failed with the faulty value
```
Executing [Testing operation with constants]
-> When I subtract $.e to $.pi
-> Then I expect the value 999.42331 but got 0.42331 (failed)
Scenario [Testing operation with constants] failed
```

0. (50%) Make sure your code is robust:
    - does it support any type of indentation and no indentation?
    - does it support positive and negative values for all operations?
    - does it support float for all operations?
    - does it fails gracefully on large values and on division by zero?
    - does it support several scenarios in the same file?

