# Problem A
Count how many times Robo-Coder can solve a problem but BionicSolver can't, let's say this count as count10.
Count how many times Robo-Coder can't solve a problem but BionicSolver can, let's say this count as count01.
If count10 is 0 then the answer is -1, else the answer is ceil((count01 + 1)/count10).

# Problem B
Notice that Tanya can only visit cities which has the same b(c_i) - c_i. With that observation, the solution is to group the cities based on its b(c_i) - c_i and then find the group which has the maximum b sum.

# Problem C
We remove characters in order from largest to smallest, that is from 'z' to 'a'. Why is it correct? Imagine the largest character, this character can't make another character removed because it is already the largest. So it is always better to remove the largest characters first to simplify our string.

# Problem D
In order to achieve minimum number of re-routes, at each i we have to generate shortest path from p[i] to p[k] that goes through edge p[i]-p[i + 1].
In order to achieve maximum number of re-routes, at each i we have to generate shortest path from p[i] to p[k] that doesn't go through edge p[i]-p[i + 1].
In order to check if there is shortest path from p[i] to p[k] that goes through edge p[i]-p[i + 1], dist[p[i]] must be equal to dist[p[i + 1]] + 1. dist[i] is distance of node i from p[k]. We can calculate dist with BFS on this graph after all it's edges are reversed.

# Problem E
* sort all the weapons such that the attacks are non-decreasing
* sort all the armors such that the defenses are non-decreasing
* sort all the monsters such that the defenses are non-decreasing

Now let's process the weapon one by one and maintain a set S. Set S is the set of all monsters whose defense is lower than current weapon's attack.
We also maintain an array X, where X[i] = -cbj + (sum of coins of the monsters in set S whose attack is smaller than bi). Notice that whenever we add a new monster to set S, we need to update the suffix of X (because array b is sorted). The answer for current weapon is then -ca + max(X[i]).
