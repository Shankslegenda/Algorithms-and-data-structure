# Algorithms-and-data-structure
1-assignment
Sakenov Aldiyar
IT-2501
Task-1.Print Digits of a Number.
<img width="1353" height="626" alt="image" src="https://github.com/user-attachments/assets/91cfbb47-c0ca-4533-b29b-8971f31f02d7" />



in function,printDigits i divide entered number to 10,to define  how many digits there are and what numbers.
Base case is the case when recursive function should be stopped to avoid the stack overflow.Here is n<10,because we separating each digitis from another


Task-2.Average of Elements.
<img width="1353" height="741" alt="image" src="https://github.com/user-attachments/assets/5724ef89-477d-4457-aa9a-dee01a14b55b" />


firstly,i sumed all the numbers.Secondly, divided into the numbers of element(basically found average of array.)
Task-3.Prime number check 1)
<img width="1353" height="567" alt="image" src="https://github.com/user-attachments/assets/618bf173-d32e-466b-a83a-528d7df40aad" />

2)<img width="1353" height="609" alt="Снимок экрана 2026-03-19 в 00 00 55" src="https://github.com/user-attachments/assets/fbb6bc7c-c771-428a-97ff-367f0a1e8712" />


so,i wrote n<=2,in case,if number is 1 or 0,because 1 and 0 are neither prime nor composite number.after we check one more time ,if n is 2,which is prime number.after that the process is,we divide the number,and if there is any reminder,than we add one more to x(iteration steps),and while x!=n or not x%n=0 we keep dividing,if n is dividable by x,the number is composite
Task-4.Factorial
<img width="1353" height="542" alt="image" src="https://github.com/user-attachments/assets/f341b432-2c58-4207-80d4-9b1facf5c974" />


so in recursive function ,I implemented the logic of N!=N*(N-1)*(N-2)....
Task-5.Fibonacci 1)
<img width="1353" height="502" alt="image" src="https://github.com/user-attachments/assets/3b01ad7c-cbb7-436b-b5be-659d4ab94111" />

2)<img width="1353" height="502" alt="image" src="https://github.com/user-attachments/assets/804ea8bc-15a5-46ac-b038-22d1fe2a55bb" />


the Fibonacci sequence is the sequence of numbers where each number is sum of 2 previous numbers.So basically,f(n)=f(n-1)+f(n-2).
Also,about the base case,if F(0)=0 and f(1)=1.During the completing this task,I've been reading about it and i knew that fibonacci sequence is example of using recursive function inefficiently,and has exponential time complexity for large n,because of having too many calculations.

Task-6.Power function
<img width="1353" height="545" alt="image" src="https://github.com/user-attachments/assets/80bef095-f2c0-4a7a-9f7d-aa1d72f4971b" />

This task looks similar to the factorial one.but instead of multiplying n*(n-1) ,you are multiplying a**n,so each time you  multiply,you have to reduce the n,so, the logic is :n*pow(n-1),where dareje is recursive function.

Task-7.Reverse output
<img width="1353" height="563" alt="image" src="https://github.com/user-attachments/assets/1ce14353-56bb-4612-8765-4c04d0902dfd" />


Firstly we enter thu number of elements in array and after we need to reverse them.So,we need to print them backwards,as(n-1).

Task-8.Check digits in String 1)
<img width="1353" height="576" alt="image" src="https://github.com/user-attachments/assets/6a2e4a90-f67c-4ad1-8840-ddb4852817eb" />



2)


<img width="1353" height="576" alt="image" src="https://github.com/user-attachments/assets/542ae10f-eb61-4c9f-a2bc-53af4d6b9db9" />


 if (!Character.isDigit(s.charAt(x))) return false;Getting the charcter at x index from string s.After,we check if its digit.if false,return false.
 in first case(123a12),at 3rd index there are a,and it is not a digit,so return false.
 second case(123456),each character is digit.return true.

Task-9. Count characters in a string 1)
<img width="1353" height="505" alt="image" src="https://github.com/user-attachments/assets/c8f38a9b-0164-423c-bc91-da1589387115" />


2)<img width="1353" height="541" alt="Снимок экрана 2026-03-19 в 00 11 39" src="https://github.com/user-attachments/assets/fedcc0b8-6e32-486e-ac07-920b2eb27bd3" />

Base case,function should stop when the string is finished.otherwise it would be infinite loop.Recursive case is adding 1 for each letter skiping another letter

Task-10.GCD 1)<img width="1353" height="511" alt="Снимок экрана 2026-03-19 в 00 12 08" src="https://github.com/user-attachments/assets/dd187054-4d2e-49ff-b045-149f433e4bfc" />


2)
<img width="1353" height="582" alt="Снимок экрана 2026-03-19 в 00 12 51" src="https://github.com/user-attachments/assets/8fd978c0-90db-4011-bd6c-d728d387ffd9" />

each step we replace a and b(a,b)-> (b,a%b),,that let us to find GCD as soon as possible.
