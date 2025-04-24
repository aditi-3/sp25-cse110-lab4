# Explore
#### 1. What is printed by line 9? If the code returns an error, explain why.

    Line 9 would print the value of `num1` + the value of `num2`. 
    If `num1` = 10 and `num2` = 10 then line 9 will print 20, "values printed: 20"

#### 2. What is printed by line 13? If the code returns an error, explain why. 

    Line 13 will print the same result as line 9 because `var` acts as a global variable and can access any changes made to it in the if statement through the else-statement. "final result: 20"

#### 3. Why should you not use var? Explain why. 

    `var` cannot be block-local or loop-local which means it works similar to a global variable. It prevents block-visibility, and prevents private variables. Everyone will beable to access everything.

#### 4. What is printed by line 9? If the code returns an error, explain why.

    Line 9 would print the value of `num1` + the value of `num2`. "values added: 20"

#### 5. What is printed by line 13? If the code returns an error, explain why. 

    Line 13 would cause an error since `result` was definted inside the if-statement, so the else-statement has no idea what it is

#### 6. What is printed by line 9? If the code returns an error, explain why. 

    `const` cannot be reassigned, so an attempt to do so will cause an error. "values added: 0"

#### 7. What is printed by line 13? If the code returns an error, explain why. 

    `const` has the same scope as `let` which means the else-statement has no idea what `result` is since it is declared inside if-else causing an error.

