# Introduction: Abstract Data Types and Data Structures

A datatype is a collection of objects and a set of operations that act on those objects.

An abstract datatype is a datatype that is organized in such a way that the specification of the objects and the specification of the operations that act on those objects are separated from the representation of the objects and the implementation of the operations.

Basically, its an User-defined  datatype in which we can define the variable and the function that are defined on them.

Eg: Struct

# Basic complexity analysis – Best, Worst, and Average Cases

Q) Why do we need to perform analysis of a program?

A) We need to perform analysis to answers these questions:

- Does the program efficiently use primary and secondary storage?
- Is the program’s running time acceptable for the task?

The performance and efficiency of an algorithm can be found by understanding its complexity. To compare the complexity of an algorithm we would need to calculate the growth of the function with respect to input.

```
Example 1

Sum(a,b) {
	c = a + b;  // 2 units of time
	return c;   // 1 unit of time
}

Thus, 3 units of time in total
Hence, the time taken for the funtion to run is a constant 3 units
```
```
Example 2

Sum_of_array(a[],n) {               //  Cost          Frequency 
	int sum = 0;                    //    1               1
	for (int i = 1; i < n; i++) {   //    3               n
		sum += a[i];                //    2              n-1
	}
	return sum;                     //    1               1
}

Here, total runtime = 1 + 3n + 2(n-1) + 1 = 5n
```
```
Example 3

transpose(a[],n) {                        //   Cost          Frequency
	for (int i = 0; i < n; i++) {         //     3               n
		for (int j = i+1; j < n; j++) {   //     4      1+2+3+...+n = n(n+1)/2
			swap(a[i][j],a[j][i]);        //     3      n(n+1)/2 - n = n(n-1)/2
		}
	}
}

Here, the total runtime = 3n + 4 * n(n+1)/2 + 3 * n(n-1)/2 = (7/2)(n^2 + n)
```
## Space Complexity

Space complexity is the amount of memory that is needed to run the program to completion.
## Time Complexity

Time complexity is the amount of time that is needed to run the program to completion.

# Asymptotic Analysis

## Big O

$f(x) = O(g(n))$ (read as “f of n is big oh of g of n”) iff (if and only if) there exist positive constants $c$ and $n_0$ such that $f(n) ≤ cg(n)$ for all $n$, $n ≥ n_0$.

![Pasted image 20240902220518](Pasted%20image%2020240902220518.png)
## Big Ω

$f(n) = Ω(g(n))$ (read as “f of n is big omega of g of n”) iff there exist positive constants $c$ and $n_0$ such that $f(n) ≥ cg(n)$ for all $n$, $n ≥ n_0$.

![Pasted image 20240902220533](\References\Pasted%20image%2020240902220533.png)
## Big Θ

$f(n) = Θ(g(n))$ (read as “f of n is nig theta of g of n”) iff there exist positive constants $c_1$, $c_2$ and $n_0$ such that $c_1g(n) ≤ f(n) ≤ c_2g(n)$ for all $n$, $n ≥ n_0$.

![Pasted image 20240902220420](Pasted%20image%2020240902220420.png)

# Analyzing Programs – Space Bounds

# Complexity Calculation of Simple Algorithms

## Linear Search

## Binary Search
