# DevTools Part 2 - Debugging

Visit https://cse110-sp26.github.io/Lab4_Hosted/ and use Chrome DevTools to debug the sum calculator.

1. What was the bug?
[YOUR ANSWER — Use the Sources tab or Console in Chrome DevTools to identify the bug. The bug is almost certainly that input values are being read as strings and concatenated instead of parsed as numbers. For example, entering 2 and 3 returns "23" instead of 5.]

2. How would you fix it?
[YOUR ANSWER — Wrap the input reads with parseInt() or Number() so that the values are treated as numbers before the addition operation. Screenshot the fix and save it as fix.png.]

Note: Screenshots result-calculateSum.png, result-dataType.png, and fix.png must be added manually to explore/devtools/ after you take them in Chrome DevTools.
