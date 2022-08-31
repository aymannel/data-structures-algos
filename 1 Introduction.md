# Introduction

## [Discrete mathematics](https://ocw.mit.edu/courses/6-042j-mathematics-for-computer-science-spring-2015/)

#### What is meant by a binary relation?
A binary relation is similar to function, but more general.
$$\text{Let}\quad A = \set{1, 2, 9} \quad\text{and}\quad B = \{1, 3, 7}$$
A binary relation $R$ is a set of ordered pairs of elements from sets $A$ and $B$, that associates elements of set $A$ with elements of set $B$ where the relation's condition is fulfilled. Thus for the relation $R$ 'less than',
$$R = \set{(1, 3), (1, 7), (2, 3), (2, 7)}$$

The domain set is defined as the elements of set $A$ whose ordered pairs $(a, b)$ belong to the binary relation $R$.
$$\text{Dom}(R) = \set{ a | (a, b) \in R }$$
$$\text{Dom}(R) = \set{1, 2}$$

The range set is defined as the elements of set $B$ whose ordered pairs $(a, b)$ belong to the binary relation.
$$\text{Ran}(R) = \set{ b | (a, b) \in R }$$
$$\text{Ran}(R) = \set{3, 7}$$

The domain set is therefore the set of elements representing the inputs, whereas the range set is the set of elements representing the outputs. The codomain set is the set of elements from which the range set takes its values.

#### An example of a different binary relation
If relation $R$ is 'greater than',
$$R = \set{(2, 1), (9, 1), (9, 3), (9, 7) }$$
$$\text{Dom}(R) = \set{2, 9} \qquad \text{Ran}(R) = \set{1, 3, 7}$$

#### What possible cardinalities can a binary relation have?
- One to one
- One to many
- Many to one

#### What possible cardinalities can a function have?
- One to one
- Many to one

#### What is meant by a deterministic algorithm?
An algorithm that given a particular input, will always produce the same single output.

#### What does the pigeon hole principle state?
If $m$ pigeons occupy $n$ holes, where $m > n$, then some holes must contain at least 2 pigeons.


---
## Algorithms
#### Define what is meant by an algorithm
An algorithm is a step-by-step procedure that maps all inputs to a single output in finite time. 

#### When does an algorithm solve a problem?
Where it returns a correct output for every input.

#### How do we prove an algorithm's correctness for small input size?
Case analysis

#### How do we prove an algorithm's correctness for large input size?
Algorithms with large inputs must be recursive and thus we prove correctness by induction.

#### How is an algorithm's efficiency analysed?
By counting the number of constant-time primitive operations in the algorithm and performing an asymptotic analysis.

#### What is meant by asymptotic analysis?
Asymptotic analysis is a method of describing a function's limiting behaviour. Thus, given the following function,
$$f(n) = 3n^{2} + n$$
As $n$ becomes very large, the function $f(n)$ is said to be asymptotically equivalent to (or simply, asymptotic to) $n^2$.

#### Describe asymptotic notation
Asymptotic notation is used to ignore constants that do not change with the input size of our problem.

- $O(f(n))$ upper bounds the asymptotic growth of a function.

- $\Omega(f(n))$ lower bounds the asymptotic growth of a function.

- $\Theta(f(n))$ both upper and lower bounds the asymptotic growth of a function.

#### Give examples of some common algorithms' asymptotic complexity
|           | constant | logarithmic | linear |  log-linear  | quadratic | polynomial |    expon.    |
| --------- |:--------:|:-----------:|:------:|:------------:|:---------:|:----------:|:------------:|
| $O(f(n))$ |  $O(1)$  | $O(\ln{n})$ | $O(n)$ | $O(n\ln{n})$ | $O(n^2)$  |  $O(n^c)$  | $2^{O(n^c)}$ |


#### An algorithm is considered efficient where it is asymptotic to what type of function?
When asymptotic to a constant, a polynomial function, or a logarithmic function.

---
## Model of Computation

#### What is meant by the word RAM model of computation?
The word RAM model of computation consists of a 'memory' (a sequence of addressable 'words', where a 'word' is a $w$ bit wide binary number) and a processor capable of performing basic operations on the memory in constant time.

#### Give examples of the basic operations that a word RAM processor can execute
- read and write at given address
- addition and subtraction
- bitwise operations
- boolean logic


#### What expression gives the minimum word size such that every word in a memory of size $n$ is addressable? 
$$w \geqslant \log_2{n}$$

#### What expression gives the maximum memory size given that each word is $w$ bits long?
$$n \leqslant 2^w$$


#### What is the approximate size limit of a memory consisting of 32 bit words?
$$2^{32} \approx 4 \text{ gigabytes}$$

#### What is the approximate size limit of a memory consisting of 32 bit words?
$$2^{64} \approx 16 \text{ exabytes}$$

---
## Data Structures

#### What is meany by a data structure?
A data structure is a systematic way of organising and accessing non-constant data. Each data structure supports a set of operations known as an interface.

#### How is data accessed in the sequence data structure?
Extrinsic order to elements allows accessing elements by index.

#### How is data accessed in the set data structure?
Intrinsic order to elements allows querying by element keys.

#### How does the interface-implementation paradigm appear in data structures?
Many implementations of a data structure can exist but they must all have the same interface.

#### Describe a static array and the asymptotic complexity of its interface
A static array is a static sequence of words of fixed width $w$, and size $n$.
- Allocating a static array of size $n$ initialised to zero in time $O(n)$.

- Returning a word stored at array index $i$ in time $O(1)$

- Writing a word at array index $i$ in time $O(1)$

#### Give an example of a static array in Python
A tuple, which is ordered, immutable and static.