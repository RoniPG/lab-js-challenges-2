1. Challenge 1:
  - Answer: 
    
    b) "xyz" and "xyz"
  - Explanation: 

    Since we reassign the value of foo inside the function, the result will always be the new value until it is reassigned again.


2. Challenge 2:
  - Answer:
      
    a) 10 and 1
  - Explanation:

    When we call the function, we reassign the value of a within the function using the given parameter. However, this does not change the original a. In the first call, we see the reassignment inside the function, but if we log the value outside the function, it remains unchanged.


3. Challenge 3:
  - Answer:

    a) ReferenceError: sayHi is not defined
  - Explanation:

    In the order of execution, the code runs from top to bottom. The first line of execution is a call to a function that has not been defined yet. Because of this, I believe we get a reference error.

  - Correct:
    
    If we copy and paste the code into the Node.js terminal, we first encounter a reference error. However, if we execute a file containing the same code, the output is (c) 'Hi there'. This happens because hoisting moves all function declarations to the top of the file before execution.
    

4. Challenge 4:
  - Answer:

    c) { num: 90 }
  - Explanation:

    This happens because we are not creating a new object; instead, we are assigning the same object to two different variables. As a result, any changes made to a or b will affect both.
5. Bonus - Challenge 5:
  - Answer:

    a) { name: "Bob", age: 30 } and { name: "Ada", age: 20 }    
  - Explanation:

    I think this will be similar to Challenge 2. The function is only modifying the parameter it receives, and I believe the parameter behaves like a copy of the object rather than referencing the object itself. First, we declare the firstRabbit, and then for the secondRabbit, we execute the function, passing firstRabbit as a parameter (as a copy). As a result, we get a copy of the first object with the modifications made inside the function. Inside the function, we first assign obj.age to the object, but immediately after, we reassign the entire object, so the final result reflects only the last change made.
- Correct:
    
    After analyzing the result of executing the code, which is (c) { name: "Bob", age: 10 } and { name: "Ada", age: 20 }, I realized that when passing an object as a parameter, we are passing its reference. This means that any modifications to its attributes will affect the original object. However, if we reassign the parameter to a new object, we create a new reference, and the original object remains unchanged.