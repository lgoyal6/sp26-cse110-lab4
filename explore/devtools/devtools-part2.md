# DevTools Part 2 - Debugging

Visit https://cse110-sp26.github.io/Lab4_Hosted/ and use Chrome DevTools to debug the sum calculator.

1. The bug was that the input values from the HTML form were being read as strings instead of numbers. When you do input.value in JavaScript it always returns a string, so adding two inputs was concatenating them (e.g. "3" + "2" = "32") instead of adding them numerically.

2. The fix is to wrap the input values with Number() when reading them, so Number(input.value) converts the string to a number before the addition is performed.
