# ADAPET
If the desired K is 1, the answer is the length of the string itself. If the desired K = 2, we want to add as little characters as possible to the end of the string. How to do it? Look at the border of the string (proper prefix that is also proper suffix), assume it's length is B, then we add |S| - B characters to our initial string. These |S| - B characters are the remaining characters that we need to form S from the border. If K > 2, just repeat this procedure. For example: S = "ada" and K = 3, the length of the border is 1 ("a"), so we will repeatedly add 3 - 1 = 2 characters to the end of S. The final string would be "adadada" ("ada" + "da" + "da").

# ADASUM
For each digit, we calculate it's contribution to the final sum. Let's say we have a string of length N and we want to calculate i-th (1-based) digit's contribution to the final sum:
* It contributes s[i] i times.
* It contributes 10 * s[i] i times.
* It contributes 100 * s[i] i times.
.
* It contributes 10^(N - i) i times.

# ADATEAMS
There are C(N, A) ways to choose which school will participate. Each chosen school can send students in C(B, D) ways. So the total answer is C(N, A) * C(B, D)^A

# EC_P
Finding bridge in graph.

# GRAFFDEF
Bridge tree. Convert the given graph to bridge tree, i.e a graph where each edge is a bridge in the given graph, each node is a group of node which is biconnected in the given graph. After that, we calculate the number of ways where we win. We win when the two chosen nodes are in the same component.

# SUBMERGE
Finding articulation point in graph.
