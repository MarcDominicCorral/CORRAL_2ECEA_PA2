# CORRAL_2ECEA_PA2

# ECE2112

# Programming_Assignment_2
This Programming Assignment contains Python Code solution to Normalization and Divisible by 3 problems. This is made by Marc Dominic C. Corral from 2 ECE-A as a programming assignment for ECE 2112 - Advance Computer Programming and Algorithms course.

# Normalization Problem 
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. 

# Python Code:
```python
import numpy as np

X = np.random.random((5,5))
X

M = X.mean()
M

STD = X.std()
STD

Z = (X-M)/STD
Z

np.save("X_normalized.npy" , Z)

print ("\nNormal Array:\n\n", X)
print ("\nNormalized Array:\n\n", Z)
```

# Output:
<img width="603" height="349" alt="image" src="https://github.com/user-attachments/assets/a355cdaa-3a2a-43e6-b2da-a5494b2825f4" />

(The output may not be always the same since the python code generates a randon variable everytime we run the code.)

# Code Explanation:
```python
import numpy as np #Imports numpy to the code

X = np.random.random((5,5)) #This creates a random 5x5 array and stores it to variable X.
X

M = X.mean() #This gets the mean from the variable X and stores it to variable M.
M

STD = X.std() #This gets the standard deviation from variable X and stores it to variable STD.
STD

Z = (X-M)/STD #This solves the Normalization using the formula and saves it to the variable Z.
Z

np.save("X_normalized.npy" , Z) #This saves the Normalization Code into ther Numpy file 

print ("\nNormal Array:\n\n", X)
print ("\nNormalized Array:\n\n", Z) #This prints both Random Normal Array and the Normalized Array.
                                     #The "\n" is a special character used to indicate the end of a line and start a new one, I used this special character to make the output neat and presentable.
```

# Divisible by 3 Problem 
This Python Code creates a 10 x 10 ndarray, which are the squares of the first 100 positive integers.

# Python Code:
```python
import numpy as np

A = np.arrange(1,101)
A

np.shape(A)

square = A.reshape(10,10)**2

divisible_by_3 = square[square%3 == 0]

np.save ("div_by_3.npy", divisible_by_3)

print ("\n10x10 Array: \n\n, square)
print ("\nNumbers Divisible by 3: \n\n", divisible_by_3)
```
# Output:
<img width="671" height="391" alt="image" src="https://github.com/user-attachments/assets/9f32b037-f1fb-4b7a-bc43-51b807a45125" />

# Code Explanation:
```python 
import numpy as np #Imports numpy to the code

A = np.arrange(1,101) #This gets an array with elements of 1-100 and stores it in the variable A.
A

np.shape(A) #This loads the shape of the Array A.

square = A.reshape(10,10)**2 #This reshapes Array A into a 10x10 Array and squaring each and every element inside the array by the function "**2" and stores it in variable square.

divisible_by_3 = square[square%3 == 0] #This takes all the variables of array square and looks for every element divisible by 3 using modulo "%3" and stores it in variable divisible_by_3.

np.save ("div_by_3.npy", divisible_by_3) #This saves the code into the Numpy file.

print ("\n10x10 Array: \n\n, square)
print ("\nNumbers Divisible by 3: \n\n", divisible_by_3) #This prints both squared 10x10 Array and the elements divisible by 3 Arrays.
                                                         #The "\n" is a special character used to indicate the end of a line and start a new one, I used this special character to make the output neat and presentable.
```


