# BINF511 Python Assignment

This assignment is designed to test your understanding of the python concepts you learned in class. 

It is meant to be completed *individually* will be graded. 

Complete the exercises below and press the play button to execute the code. After completing each part press **Save** button to save the output. The assignment will be graded based on the output of your programs, there are a total of 20 points available. 

When you have completed the whole assignment click **File > Download as > IPython (.ipynb)** (DO NOT forget to include your name to the name of the file) and upload to myCourses.
## Part 1 : Strings and variable assignment
### *2 points total*

Assign the values below to variables and __print__ them: 

- Your complete name. [_1/4 points_]
- Your McGill ID number (as an `int`). [_1/4 points_]
- The scientific name of your favorite species. [_1/4 points_]
- Your height in meters (as a `float`). [_1/4 points_]
- Print *just* your last name using sub-strings and the original name variable you just defined above. [_1 point_]

# Enter the code for part 1 below

## Part 2: Opening files
### *3 points total*

**Make sure you have downloaded the `Exercise-file.txt` from the *MyCourses* portal and that you have it saved in the same directory as this notebook.** Then do the following: 

- Create a variable containing `Exercise-file.txt` as a file object in `r` mode using the `open()` funciton. [_1 point_]
- Using the `.read()` method, `print` the contents of the file. [_1 point_]
- Close the file object using the `.close()` method. [_1 point_]

# Enter the code for part 2 below

## Part 3: Lists and sub-lists
### *4 points total* 

Create the following lists: 

- A list called `positive` with the following strings: `R`, `H`, `K`. [_1/5 points_]
- A list called `negative` with the following strings: `D`, `E`. [_1/5 points_]
- A list called `polar` with the following strings: `S`, `T`, `N`, `Q`. [_1/5 points_]
- A list called `hydrophobic` with the following strings: `A`, `V`, `I`, `L`, `M`, `F`, `Y`, `W`. [_1/5 points_]
- A list called `other` with the following strings: `C`, `U`, `G`, `P`. [_1/5 points_]
- A list called `amino_acids` containing the previous 5 lists as elements (this is a list of lists). [_1 point_] 
- Print the complete `amino_acids` list and use the `len()` function to also print its length. [_1 point_]
- Print only the charged amino acids lists (`positive` and `negative`) by creating a sub-list of `amino_acids`. [_1 point_]

# Enter the code for part 3 below

## Part 4: Loops
### *2 points total*

**After running the previous cell** use a `for` loop to: 

- Loop through the elements of the `hydrophobic` list. 
- Print the following phrase: **`@ is the one-letter symbol of a hydrophobic amino acid.`**
    - Where `@` corresponds to each list element. [_2 points_]


# Enter the code for part 4 below

## Part 5: Functions
### *2 points total*

Define a new function that called **`dna2rna()`**. The function should take a string as an argument and do the following: 

- Using the `.replace()` method, replace every `T` with a `U`. [_1 point_]
    - *Check the first practical seen in class to remember how to use the `.replace()` method *
- Return the new string. [_1 point_]

Use the **`DNA_sequence`** variable below and a print statement to show your function works as expected. 

**Important note**: The function should just **`return`** the new string, the function **should not** print the string by itself. 
DNA_sequence = "ACTCGATCCAAATACTGCACAGAAACCTCCGGTGTCCACGGTGACTCACCCTATGGTTCGGGTACCATGG"

# Enter the code for part 5 below
def dna2rna(seq):
    
## Part 6: Conditional tests
### *7 points total*

Now, lets put it all together. Define a function called `nuc_ac_check` that takes a single string as an argument. Using `if/elif/else` statements as well as the boolean operators `and/or/not`, write code so your function performs the following checks: 

- Turn the input string to uppercase using the `.upper()` method. [*1 point*]
- If the string contains any character that **is not** `A`,`C`,`G`,`T` or `U`; `return` the string **`not an unambiguous nucleic acid`**. [*2 points*]
- If the string contains *exclusively* the characters `A`,`C`,`G`, and `U`; `return` the string **`RNA`**. [*2 points*]
- If the string contains *exclusively* the characters `A`,`C`,`G`, and `T`; `return` the string **`DNA`**. [*2 points*]

Assume that no input strings will contain numbers or special characters (including whitespaces). Remember, your function should **`return`** the strings, not print them. 

**Tips:**

- Be careful when programming your function, the order of the steps is very important for this function to work properly. 
- Remember you can loop through strings. Can you think of a useful string to loop through that will help you quickly check all the invalid characters? 
- Use the print statements in the bottom of the cell to check if your function is working as expected. 
# Enter the code for part 6 below
def nuc_ac_check(string):
    

# DON'T MODIFY THE FOLLOWING CODE, JUST USE IT TO CHECK YOUR FUNCTION
RNA_sequence = "GGUACGGCUUGGUAUCCCACUCAGUGGCACCUGUGGCCUCCAAAGACACGUCAUAAACCUAGCUCA"
peptide_sequence = 'acdttayvrppnmkhgfeddvrqpnac'
DNA_sequence = "actcgatactgcacagaaacctccggtgtctcaccctatggttcgggtcatgg"

print('The RNA_sequence variable is: ' + nuc_ac_check(RNA_sequence))
print('The peptide_sequence variable is: ' + nuc_ac_check(peptide_sequence))
print('The DNA_sequence variable is: ' + nuc_ac_check(DNA_sequence))
### Submission instructions:
When you finish the assignment, save the file by clicking **File > Download as > IPython (.ipynb)** and upload this file to myCourses.