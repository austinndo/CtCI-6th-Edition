# Chapter 6 - Big O

Big O, big theta, and big omega describe runtimes

O (big O): describes the upper bound

Ω (big omega): describes the lower bound

Θ (big theta): describes the tight bound. in academia, theta means both O and omega
  ex: if an algorithm is Θ(N) it is both O(N) and Ω(N)

# Multi-Part Algorithms: Add vs. Multiply

Add Runtimes: O(A + B)
for (int a : arrA) {
  print(a);
}
for (int b : arrB) {
  print(b);
}

Multiply Runtimes: O(A*B)
for (int a : arrA) {
  for (int b : arrB ) {
    print(a + "," + b);
  }
}

Essentially: 
- if your algorithm is "do this, then, when done, do that" ==> add the runtimes
- if your algorithm is "do this for each time you do that" ==> multiply the runtimes

# Log N Runtimes

O(log N) runtimes are common. Ex: binary search

In a binary search, we look for an example x in an N-element sorted array.

First, compare x to the midpoint of the array.
  If x == middle, then we return
  If x < middle, then we search the left side
  If x > middle, then we search the right side

search 9 within {1, 5, 8, 9, 11, 13, 15, 19, 21}
  compare 9 to 11 --> smaller (x < middle)
  so, search 9 within {1, 5, 8, 9, 11}
  again, compare 9 to 8 --> bigger (x > middle)
    so, search {9, 11}
    compare 9 to 9 --> equal (x == middle)
    now return