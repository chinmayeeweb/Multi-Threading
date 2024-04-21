# Multi-Threading


#Methodology
Divide the Matrices: Break down the input matrices into smaller submatrices. The number of submatrices and their sizes depend on the number of threads available and the characteristics of the matrices.
Thread Creation: Create multiple threads, with each thread responsible for multiplying a specific pair of submatrices. The number of threads should be determined based on factors like the number of CPU cores available and the size of the matrices.
Thread Execution: Each thread performs the multiplication of its assigned submatrices. This involves iterating over the rows and columns of the submatrices and computing the dot product of corresponding rows and columns to populate the resulting submatrix.
Synchronization: Since multiple threads are accessing and updating shared data (e.g., the elements of the resulting matrix), synchronization mechanisms such as locks or barriers may be needed to ensure that threads do not interfere with each other's computations. For example, each thread might compute its part of the result in a separate temporary matrix and then combine these results into the final result matrix after all threads have finished.
Combining Results: Once all threads have completed their computations, combine the results obtained from each thread to construct the final result matrix. This typically involves aggregating the submatrices computed by each thread into the appropriate positions of the final matrix.
Thread Termination: After the matrix multiplication is complete, terminate or join all threads to release any allocated resources and ensure proper cleanup.
