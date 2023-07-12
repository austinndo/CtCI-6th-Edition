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