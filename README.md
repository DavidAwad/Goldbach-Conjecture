# Goldbach-Conjecture
This is a small python program and my algorithm to verify the Goldbach conjecture for all numbers below 10^7.


## The what?

The Goldbach Conjecture is that all even numbers can be expressed as the sum of two prime numbers.

This program is a proof of that conjecture for the first 10 million integers. 

It uses the Sieve of Eratosthenes in order to generate a list of all the primes under 10 million, and then proceeds to find the prime numbers that sum to each even number under 10 million. 

## Implementation Details
Generate a list of all prime numbers less than 10**7.

For every even number between 4 and 10^7, for each of these numbers (i), find a set of primes that sum to i.

For each i you then iterate through the list of prime numbers (n).

We can assert that for each i and m, i = n + m; where n and m are both prime numbers such that 0 < n, m, < 10^7.

You can then assert that m = i - n. If i - n is a prime number, then we know there is a pair of primes that sum to that i.
Becuase this is a sorted array of primes, all searches are binary searches yeilding us a final runtime of O( 10^7/2 * nlog(n) ) Or nlog(n)

###### constant of 10 million? who cares apparently! it's Big O!

Note: The time it takes to generate the list of primes at the outset using the Sieve of Eratosthenes is O(nlog(log(n)) + O(n) ). However this get's overshadowed by the algorithm to verify the conjecture anyway. 


## Usage
If you don't care about the math and just want to see the thing run, just check out the usage statistic below. 
###### note: this will take a while to generate the initial list of primes, as it's a large set, so be patient! 

```
python erato.py
```
