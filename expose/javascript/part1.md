# Part 1 - var/let/const Scoping

1. Line 9 prints "values added: 20". var is function-scoped so result is accessible anywhere in the function. Since add is true, the if block runs, result is set to 20, and the log executes normally.

2. Line 13 prints "final result: 20". var is function-scoped so result persists outside the if block and still holds 20 at line 13.

3. You should not use var because it is function-scoped rather than block-scoped, meaning variables declared inside blocks like if statements or for loops leak out into the rest of the function. This makes code unpredictable and leads to naming conflicts. let and const are block-scoped and behave more predictably.

4. Line 9 prints "values added: 20". let is block-scoped, but line 9 is inside the same if block where result was declared, so it is accessible and holds 20.

5. Line 13 throws a ReferenceError: result is not defined. let is block-scoped, so result only exists inside the if block. Line 13 is outside that block and cannot access result.

6. Line 9 throws a TypeError: Assignment to constant variable. const cannot be reassigned. Line 7 tries to reassign result = num1 + num2, but result was declared with const on line 5. This error is thrown before line 9 is ever reached.

7. Line 13 throws a ReferenceError: result is not defined. Even ignoring the reassignment issue, const is block-scoped like let, so result is not accessible outside the if block at line 13.
