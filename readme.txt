
Execution with numpy

 
`import time
import numpy as np` 

These are the import statements that are used to import the necessary modules. `time` module is used to calculate the execution time of the program and `numpy` module is used to create a large array of numbers and to perform the summation.


`start_time = time.time()` 

This line captures the current time before the calculation starts.

`arr = np.arange(15000000000, dtype=np.int64)` 

This line creates a numpy array of 15000000000 integers using the `np.arange()` function. The `np.int64` parameter specifies the datatype of the elements in the array to be 64-bit integer.



`total = np.sum(arr)` 

This line calculates the sum of all the elements in the numpy array using `np.sum()` function.



`end_time = time.time()` 

This line captures the current time after the calculation has finished.



`print('sum is:', total)
print('Execution time:', end_time - start_time)` 

These lines print the sum of all elements in the array and the execution time of the program in seconds. The execution time is calculated by taking the difference between the start time and end time captured earlier.
> Written with [StackEdit](https://stackedit.io/).
