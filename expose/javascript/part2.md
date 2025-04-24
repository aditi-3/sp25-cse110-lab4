# Explore
#### 1. What will happen at line 12 and why? If the code causes an error, explain why.

    Line 12 will just return the value of i at the end of the for loop iteration. It will be equal to the length of prices.It prints 3.

#### 2. What will happen at line 13 and why? If the code causes an error, explain why.

    discountedPrice would return the calculation of prices[i] * (1-discount) for when i = prices.length-1. In this case it would be 300*(1-0.5) = 150.

#### 3. What will happen at line 14 and why? If the code causes an error, explain why. 

    finalPrice rounds discountedPrice to the second decimal place, but it will still be printed as an integer, 150.

#### 4. What will this function return? Give a brief explanation why. If the code causes an error, explain why

    The final output is an array called discounted that stores all the items and their discounted price. We take the original prices of all the items, do the math to calculate the discounted price. Store discounted price of each item into discountedPrice variable, then round it and store it into finalPrice. Then we push it into the discounted array. Once all the item prices are calculated, we return it. It returns [50, 100, 150].

##### 5. What will happen at line 12 and why?  If the code causes an error, explain why. ^^^ (assume this function is being called like the others: discountPrices([100, 200, 300], 0.5)).

    There is an error since i is not a global variable, so we cannot access it outside the for loop block.

#### 6. What will happen at line 13 and why? If the code causes an error, explain why.

    An error will occur for the same reasons as question 5, discoundedPrices can only be accessed inside the for loop.

#### 7. What will happen at line 14 and why? If the code causes an error, explain why.

    Since the console.log statement is inside the function and it is in the same scope as where the finalPrice is declared, we are able to access it. That means line 14 will print 0.

#### 8. What will this function return? Give a brief explanation. If the code causes an error, explain why.

    The function will return the same result as question 4. It will calculate the discounted price of each item in the prices array and return it through discounted array. It returns [50, 100, 150].

#### 9. What will happen at line 11 and why? If the code causes an error, explain why.

    There will be an error since i is defined using let which means we cannot access it outside of the for loop block.

#### 10. What will happen at line 11 and why? If the code causes an error, explain why.

    Line 12 will return the length of prices array, 3.

#### 11. What will this function return? Give a brief explanation. If the code causes an error, explain why.

    The code will successfully calculate and return the list of discounted prices given their original prices for all items. (Same as question 4 and 8). It returns [50, 100, 150].

#### 12. Given the above Object, write the notation for:  (These should be in your part2.md)
#### A. Accessing the value of the name property in the student object

    student.name

#### B. Accessing the value of the Grad Year property in the student object

    student["Grad Year"]

#### C. Calling the function for the greeting property in the student object

    student.greeting()

#### D. Accessing the name property of the object in the Favorite Teacher property in student

    student["Favorite Teacher"].name

#### E. Access index zero in the array of the courseLoad property of the student object

    student.courseLoad[0]

#### 13. Arithmetic
#### A. '3' + 2

    Output = '32'. The operation concatnated string '3' and 2 after it. It converted 2 to a string

#### B. '3' - 2

    Output = 1. The operation subtracted 2 from 3. It converted 3 to integer

#### C. 3 + null

    Output = 3. Since null also means there is nothing, it was converted to 0. The operation we performed was 3 + 0.

#### D. '3' + null

    Output = '3null'. Here, null was converted to a string and concatnated with '3'.

#### E. true + 3

    Output = 4. True is also the binary 1, so here, we did 1 + 3.

#### F. false + null

    Output = 0. False is also 0 in binary and null is also represented as 0. In the end, we did 0 + 0.

#### G. '3' + undefined

    Output = '3undefined'. Since there is no integer value that defines undefined, we treat it as a string and concatnate it to '3'.

#### H. '3' - undefined

    Output = NaN. The subtractions triggers both values to be converted to integer. Since undefined is not a number, 3 - NaN turns into NaN.

#### 14. Comparison
#### A. '2' > 1

    Output = true. The greater than sign concatnated '2' as an integer to perform the operation.

#### B. '2' < '12'

    Output = false. The less than sign will convert both inputs to an integer to perform the operation.

#### C. 2 == '2'

    Output = true. Once again, the equals comparison will convert any value that isn't an integer to an integer and then compute the result.

#### D. 2 === '2

    Output = false. This time, === is checking the type and value. Since 2 and '2' are different types, it is false.

#### E. true == 2

    Output = false. True can be represented as 1 in binary and comparing the equality of 1 to 2 is false.

#### F. true === Boolean(2)

    Output = true. The integer 2 is evaluated to true in this case since any non zero number is true. 


#### 15. Explain the difference between the == and === operators.

    The == comparison only checks if the two values are the same when they have a common data type. This means JS will convert one or both of the types to match each other. But, the === operation will check both the type and the value, so if the two values do not have the same data type then it will automatically be false.

#### 16. Given the above Object, write a for...in loop that will iterate through it and print out the value of the property if the property starts with the letter r, or if the value of that property is an odd number.  (This should be in a JS file part2-question16.js)
```js
for (const property in object) {
    let prop = object[property]
    if (property[0] == 'r' || (typeof prop === 'number' && prop % 2 === 1)) {
        console.log(`${property}: ${object[property]}`);
    }
}
```

#### 17. If the function above is called with the following parameters modifyArray([1,2,3], doSomething), what will be the result? Briefly walk through how you arrived at that result. (This should be in your part2.md). Here we are passing in a function as a parameter, however we can also return a function from another function just as easily, you're encouraged to play around with callbacks as they are used heavily in frontend JS development. 

    Line 13 calls the modifyArray function and passes [1,2,3] and doSomething into the parameters. Within the modifyArray function, there is a newArr that stores a modified array using the parameter values ([1,2,3]). Inside the modifyArray function, there is also a for loop that loops through [1,2,3] and calls the doSomething function for each element. The doSomething array uses the element as a parameter and multiplies it by 2. This result is stored into newArr. So at the end of the program, the modifyArray returns the input array but with all its elements multiplied by 2 ([2,4,6]).

#### 18. The above program only prints out the time once when executed. Modify this code such that the program prints out the current time every second.  (This should be a JS file - part2-question18.js)

```js
setInterval(() => {
    let d = new Date();
    let time = d.toLocaleTimeString();
    console.log(time);
}, 1000);
```

#### 19. What is the output of the above code? (This should be in your part2.md)

    The function prints out 1, 4, and 3 then 2 (after one second of executing).