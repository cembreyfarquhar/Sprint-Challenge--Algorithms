Add your answers to the Algorithms exercises here.

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

a)  a = 0
    while (a < n * n * n):
      a = a + n * n

a.	O(4n) -> O(n)





b)  sum = 0
    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1


b. 	O(n) -- O(n^2) -- O(n^3) -- O(10n^3) => O(n^3)





c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)


c. 	O(n)






Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.


divide and conquer, binary

I would start at floor n / 2. If the egg broke, I would go to n / 4. If it still broke, I would go to n / 8. Essentially a binary search, where the most possible steps to find the solution would be n / 2



time complexity: O(log n)