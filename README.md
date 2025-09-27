# CORRAL_2ECEA_PA2

# ECE2112

# Programming_Assignment_2
This Programming Assignment contains Python Code solution to Normalization and Divisible by 3 problems. This is made by Marc Dominic C. Corral from 2 ECE-A as a programming assignment for ECE 2112 - Advance Computer Programming and Algorithms course.

# Normalization Problem 
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. 

# Steps:
1.) Import numpy into the Python Code.
```python
import numpy as np #Imports numpy to the code.
```
2.) Create a 5x5 ndarray with random numbers.
```python
X = np.random.random((5,5)) #This creates a random 5x5 array and stores it to variable X.
X
```
3.) Use .mean() to compute for the average.
```python
M = X.mean() #This gets the mean from the variable X and stores it to variable M.
M
```
4.) Use .std() to compute for the standard deviation.
```python
STD = X.std() #This gets the standard deviation from variable X and stores it to variable STD.
STD
```
5.) Compute the normalization using the formula:

<img width="149" height="101" alt="image" src="https://github.com/user-attachments/assets/50646460-5db8-46cf-9437-452d69b339ec" />

By translating the formula into a Python Code.
```python
Z = (X-M)/STD #This solves the Normalization using the formula and saves it to the variable Z.
Z
```
6.) Using np.save(), save the certain variable into the numpy file.
```python
np.save("X_normalized.npy" , Z) #This saves the Normalization Code into ther Numpy file
```
7.) Print the original ndarray and normalized ndarray.
```python
print ("\nNormal Array:\n\n", X)
print ("\nNormalized Array:\n\n", Z) #This prints both Random Normal Array and the Normalized Array.
                                     #The "\n" is a special character used to indicate the end of a line and start a new one, I used this special character to make the output neat and presentable.
```
8.) Combine all the commands and construct the Python Code.
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
9.) Run the Pyhthon Code. The output would be:

<img width="603" height="349" alt="image" src="https://github.com/user-attachments/assets/a355cdaa-3a2a-43e6-b2da-a5494b2825f4" />

<h6>Note: The output may not be always the same since the python code generates a randon variable everytime we run the code.</h6> 


# Divisible by 3 Problem 
This Python Code creates a 10 x 10 ndarray, which are the squares of the first 100 positive integers.

# Steps:
1.) Import numpy into the Python Code.
```python
import numpy as np #Imports numpy to the code.
```
2.) Make an array that contains numbers from 1 to 100.
```python
A = np.arrange(1,101) #This gets an array with elements of 1-100 and stores it in the variable A.
A
```
3.) Using .reshape(), reshape the array into a 10x10 array and square the result inside the array using the arithmetic **2.
```python
np.shape(A) #This loads the shape of the Array A.

square = A.reshape(10,10)**2 #This reshapes Array A into a 10x10 Array and squaring each and every element inside the array by the function "**2" and stores it in variable square.
```
4.) Using modulo(%) arithmetic, get the divisible by 3 and equate the results to zero.
```python
divisible_by_3 = square[square%3 == 0] #This takes all the variables of array square and looks for every element divisible by 3 using modulo "%3" and stores it in variable divisible_by_3.
```
5.) Using np.save, save the divisible by 3 variable into a numpy file.
```python
np.save ("div_by_3.npy", divisible_by_3) #This saves the code into the Numpy file.
```
6.) Print the Statement.
```python
print ("\n10x10 Array: \n\n, square)
print ("\nNumbers Divisible by 3: \n\n", divisible_by_3) #This prints both squared 10x10 Array and the elements divisible by 3 Arrays.
                                                         #The "\n" is a special character used to indicate the end of a line and start a new one, I used this special character to make the output neat and presentable.
```
7.) Combine all the commands and construct the Python Code.
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
8.) Run the Pyhthon Code. The output would be:

<img width="671" height="391" alt="image" src="https://github.com/user-attachments/assets/9f32b037-f1fb-4b7a-bc43-51b807a45125" />
