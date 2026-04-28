# Part 2 - discountPrices, Data Types, and Callbacks

1. Line 12 prints 3. var is function-scoped, so i from the for loop is accessible outside it. After iterating over 3 elements, i increments to 3 before the loop condition fails, leaving i = 3 in function scope.

2. Line 13 prints 150. var is function-scoped so discountedPrice leaks out of the loop. The last iteration processed prices[2] = 300, so discountedPrice = 300 * (1 - 0.5) = 150.

3. Line 14 prints 150. finalPrice was declared with var at the top of the function so it is function-scoped. Its last assigned value from the loop was Math.round(150 * 100) / 100 = 150.

4. The function returns [50, 100, 150]. All console.log lines are commented out. It iterates over [100, 200, 300] with a 0.5 discount: 100*0.5=50, 200*0.5=100, 300*0.5=150, and pushes each into the discounted array.

5. Line 12 throws a ReferenceError: i is not defined. let is block-scoped so i only exists inside the for loop block. It cannot be accessed at line 12 outside the loop.

6. Line 13 throws a ReferenceError: discountedPrice is not defined. let is block-scoped so discountedPrice only exists inside the for loop block and cannot be accessed at line 13.

7. Line 14 prints 150. finalPrice was declared with let at the top of the function (outside the loop), so it is in scope at line 14 and holds 150 from the last loop iteration.

8. The function returns [50, 100, 150]. Same logic as Q4. Using let does not affect the return behavior since discounted and finalPrice are declared at function scope.

9. Line 11 throws a ReferenceError: i is not defined. i is declared with let in the for loop header, making it block-scoped to the loop. It cannot be accessed at line 11.

10. Line 12 prints 3. length is declared with const at the top of the function as const length = prices.length. It is accessible throughout the function body and prices.length = 3.

11. The function returns [50, 100, 150]. const discountedPrice is declared inside the loop block, so it gets a fresh binding each iteration — this is valid since const only prevents reassignment, not re-declaration in a new block scope. The loop correctly pushes each discounted value.

12.
A. student.name
B. student['Grad Year']
C. student.greeting()
D. student['Favorite Teacher'].name
E. student.courseLoad[0]

13. Arithmetic:
A. '3' + 2 = '32' — + with a string triggers concatenation; 2 coerces to '2'
B. '3' - 2 = 1 — - is numeric only; '3' coerces to 3
C. 3 + null = 3 — null coerces to 0 in numeric context
D. '3' + null = '3null' — + with a string; null coerces to 'null'
E. true + 3 = 4 — true coerces to 1
F. false + null = 0 — false coerces to 0, null coerces to 0
G. '3' + undefined = '3undefined' — + with a string; undefined coerces to 'undefined'
H. '3' - undefined = NaN — - is numeric; undefined coerces to NaN

14. Comparison:
A. '2' > 1 = true — '2' coerces to 2, and 2 > 1
B. '2' < '12' = false — both strings, lexicographic comparison; '2' > '1' alphabetically
C. 2 == '2' = true — loose equality coerces '2' to 2
D. 2 === '2' = false — strict equality, different types
E. true == 2 = false — true coerces to 1, and 1 != 2
F. true === Boolean(2) = true — Boolean(2) is true, and true === true

15. == is loose equality and performs type coercion before comparing, so values of different types can be equal (e.g. 2 == '2' is true). === is strict equality and checks both value and type with no coercion, so 2 === '2' is false. Always prefer === to avoid unexpected coercion behavior.

17. modifyArray([1,2,3], doSomething) returns [2, 4, 6]. The function iterates over [1, 2, 3], passes each element to doSomething which multiplies it by 2, and pushes the result into newArr. So 1 becomes 2, 2 becomes 4, 3 becomes 6.
