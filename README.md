# Multi-Threading


#Methodology

Function multiply_matrices:
This function takes two parameters: constant_matrix, which is a constant matrix, and num_matrices, the number of random matrices to be multiplied with the constant matrix.
Inside the function, it iterates num_matrices times, each time performing matrix multiplication between constant_matrix and a randomly generated matrix of size 1000x1000 using NumPy's np.dot function.
It records the execution time for performing these matrix multiplications.

Main function main():
It initializes the constant matrix constant_matrix with random values of size 1000x1000.
It defines the number of matrices to multiply (num_matrices) and the maximum number of threads to use (num_threads).
It creates a list threads to store thread objects.
It iterates over a range of num_threads, creating a thread for each iteration using threading.Thread and passing the multiply_matrices function as the target function. Each thread is started after creation.
It joins each thread to wait for all threads to complete their execution.
It records the execution times of matrix multiplication for each number of active threads.
It plots the execution time versus the number of active threads using Matplotlib.
It creates a table using PrettyTable to display the execution times for each number of threads.


#Results
The code aims to measure the impact of multithreading on the execution time of matrix multiplication. By varying the number of active threads, it observes how the execution time changes.
However, there's a flaw in the way the threads are created and executed. The script starts multiple threads but doesn't utilize them effectively. Each thread performs the matrix multiplication independently without coordinating with others or sharing the workload.

<img width="254" alt="image" src="https://github.com/chinmayeeweb/Multi-Threading/assets/95276351/9c878db1-aaf8-428c-8785-b361ab55bf76">


As a result, the execution times measured for different numbers of active threads may not show a significant improvement because the workload is not distributed among the threads effectively.
Therefore, the plot and table might not accurately reflect the benefits of multithreading for this particular task.


<img width="428" alt="image" src="https://github.com/chinmayeeweb/Multi-Threading/assets/95276351/cfaa5e9b-390b-4a83-afb9-3179863dfdc3">






