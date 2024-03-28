# Divisible-by-sum-check
Let f(n) denote the sum of the digits of n. For example, f(101)=1+0+1=2. Given an integer N, determine if f(N) divides N. Input An integer, N. Constraints 1≤N≤10^9 Output If f(N) divides N, print "Yes"; print "No" otherwise.

def sum_of_digits(n):
    return sum(int(digit) for digit in str(n))

def divisible_by_sum(n):
    digit_sum = sum_of_digits(n)
    if digit_sum == 0:
        return False
    return n % digit_sum == 0

N = int(input())

if divisible_by_sum(N):
    print("Yes")
else:
    print("No")
