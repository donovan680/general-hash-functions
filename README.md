# general-hash-functions
Hash functions are by definition and implementation generally regarded as Pseudo Random Number Generators (PRNG). From this generalization it can be assumed that the performance of hash functions and comparisons between other hash functions can be determined by modeling the functions as PRNGs. 

 Analysis techniques such a Poisson distribution can be used to analyze the collision rates of different hash functions for different groups of data. In general there is a theoretical hash function known as the Perfect Hash Function for any specific group of data. The perfect hash function by definition states that no collisions will occur meaning no repeating hash values will arise from different elements of the group.

In reality it is very difficult to find a perfect hash function for an arbitrary set of data, and furthermore the practical applications of perfect hashing and its variant minimal perfect hashing are quite limited. So instead one may choose to pursue the concept of an Ideal Hash Function, which is commonly defined as a function that produces the least amount of collisions for a particular set of data.

One of the fundamental problems with hashing data or specifically mapping values from one domain to another, is that there are soo many permutations of types of data, some highly random, others containing high degrees of patterning or structure that it is difficult to generalize a hash function for all data types or even for specific data types. All one can do is via trial and error and utilization of formal hash function construction techniques derive the hash function that best suites their needs. Some factors to take into account when choosing hash functions are:  
 
 Data Distribution.

This is the measure of how well the hash function distributes the hash values of elements within a set of data. Analysis in this measure requires knowing the number of collisions that occur with the data set meaning non-unique hash values, If chaining is used for collision resolution the average length of the chains (which would in theory be the average of each bucket's collision count) analyzed, also the amount of grouping of the hash values within ranges should be analyzed.

In the following diagram there are five unique messages to be hashed (M0,...,M4) and inserted into a hash-table. Each message is hashed using two different hash functions H1 and H2. The diagram depicts how H1 generally distributes the hash values for the messages evenly over the given bucket-space (table), where as H2 returns the same value for each message causing numerous collisions. 

Hash Function Efficiency.

This is the measure of how efficiently the hash function produces hash values for elements within a set of data. When algorithms which contain hash functions are analyzed it is generally assumed that hash functions have a complexity of O(1), that is why look-ups for data in a hash-table are said to be "on average of O(1) time complexity", where as look-ups of data in other associative containers such as maps (typically implemented as Red-Black trees) are said to be of O(logn) time complexity.

A hash function should in theory be a very quick, stable and deterministic operation. A hash function may not always lend itself to being of O(1) complexity, however in general the linear traversal through a string or byte array of data that is to be hashed is so quick and the fact that hash functions are generally used on primary keys which by definition are supposed to be much smaller associative identifiers of larger blocks of data implies that the whole operation should be quick, deterministic and to a certain degree stable.

The hash functions in this essay are known as simple hash functions or General Purpose Hash Functions. They are typically used for data hashing (string hashing). They are used to create keys which are used in associative containers such as hash-tables. These hash functions are not cryptographically safe, they can easily be reversed and many different combinations of data can be easily found to produce identical hash values for any combination of data. 
