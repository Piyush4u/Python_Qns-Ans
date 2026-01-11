## 1. Text File Handling
1. **Word Counter:** Read a text file and count the number of times the words "the" and "this" appear.
2. **Line Filter:** Read a text file and display only those lines which begin with the uppercase letter 'T'.
3. **Longest Line:** Read a text file and find the line with the maximum number of characters.
4. **Reverse Content:** Read a text file and write its content to a new file, but with the order of lines reversed.
5. **Character Replacer:** Read a text file and create a new file where every space ` ` is replaced by a hyphen `-`.
6. **Four Letter Words:** Read a text file and display all words that have exactly 4 characters.
7. **Comment Stripper:** Read a Python source file (`.py`) and print only the lines that are **not** comments (i.e., lines that do not start with `#`).
8. **Digit Counter:** Read a text file and count how many digits (0-9) are present in the entire file.
9. **Formatting Text:** Read a text file containing lower case characters and write it to another file with every sentence capitalized.
10. **File Merge:** Write a program to merge the content of `file1.txt` and `file2.txt` into a third file `file3.txt`.

## 2. Binary File Handling (Using `pickle`)
11. **Student Search:** Create a binary file `student.dat` storing records `[RollNo, Name, Marks]`. Search for a student by name and display their RollNo and Marks.
12. **High Achievers:** Read `student.dat` and display the details of all students who have scored more than 90 marks.
13. **Delete Record:** Create a binary file with Employee records `[EmpID, Name, Salary]`. Input an EmpID and delete that record from the file.
14. **Append Record:** Write a program to append a new Employee record to an existing binary file.
15. **Salary Hike:** Update the binary file `employee.dat` by increasing the salary of all employees by 10%.
16. **Book Store:** Create a binary file `books.dat` with `[BookID, Title, Price]`. Count and display the number of books with a price greater than 500.

## 3. CSV File Handling
17. **Inventory Management:** Create a CSV file `data.csv` containing `[Item_Name, Quantity, Price]`. Read the file and calculate the total value of the inventory (Quantity * Price for each item).
18. **High Scorer:** Read a CSV file containing `[Name, Score]` and print the name of the person with the highest score.
19. **Delimiter Change:** Read a CSV file separated by commas and write it to a new file separated by tab characters (`\t`).
20. **User Search:** Create a CSV file `users.csv` with `[Username, Email]`. Accept a username from the user and display their email if it exists.

## 4. Data Structures (Lists, Stacks, Queues)
21. **Queue Implementation:** Write a program to implement a Queue (FIFO - First In First Out) using a list. Include functions for `enqueue`, `dequeue`, and `display`.
22. **Push/Pop Numbers:** Write a function that pushes all numbers greater than 100 from a generic list onto a Stack, and another function to pop and display them.
23. **List Statistics:** Write a program that takes a list of integers and returns a tuple containing the mean, median, and mode.
24. **Duplicate Remover:** Write a program that takes a list of numbers and returns a new list with all duplicates removed, preserving the original order.
25. **Matrix Addition:** Write a program using nested lists to perform the addition of two 3x3 matrices.

## 5. Random Module & Simulation
26. **Card Dealer:** Write a program to select a random card from a deck (e.g., "Ace of Spades", "7 of Hearts").
27. **Password Generator:** Generate a random secure password of length 8 containing uppercase, lowercase, numbers, and special characters.
28. **Coin Toss:** Simulate a coin toss 100 times and print how many times "Heads" and "Tails" appeared.
29. **Number Guesser:** The computer picks a number between 1 and 100. The user tries to guess it. The computer gives hints ("Too high" or "Too low") until the user guesses correctly.

## 6. String Manipulation & General Logic
30. **Palindrome Checker:** Input a string and check if it is a palindrome (reads the same forward and backward).
31. **Vowel Replacer:** Input a string and replace all vowels with an asterisk `*`.
32. **Email Validator:** Input an email address and check if it contains exactly one `@` and ends with `.com` or `.in`.
33. **Case Inverter:** Input a string. Convert uppercase letters to lowercase and vice versa (e.g., "HeLLo" -> "hEllO").
34. **Word Counter:** Input a sentence and count the number of words in it.
35. **Armstrong Number:** Check if a given 3-digit number is an Armstrong number (sum of cubes of digits equals the number).
