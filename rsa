#!/usr/bin/python3
import sys

def is_prime(n):
    # Check if n is less than 2
    if n < 2:
        return False
    # Check if n is 2 or 3
    if n == 2 or n == 3:
        return True
    # Check if n is divisible by 2 or 3
    if n % 2 == 0 or n % 3 == 0:
        return False
    # Check if n is divisible by any number in the range from 5 to the square root of n, incrementing by 6
    for i in range(5, int(n ** 0.5) + 1, 6):
        if n % i == 0 or n % (i + 2) == 0:
            return False
    # If none of the above checks passed, then n is prime
    return True

def factorize(n):
    # Try to find a factor of n by starting at 2 and incrementing by 1
    for i in range(2, n):
        # If n is evenly divisible by i and i is prime, then we found a factor
        if n % i == 0 and is_prime(i):
            return (i, n // i)
    # If we didn't find a factor, then n is prime and cannot be further factorized
    return (n, 1)

def main():
    # Open the input file for reading
    with open(sys.argv[1], 'r') as f:
        # Read the first (and only) line of the file
        line = f.readline()
        # Strip the newline character from the end of the line
        n = int(line.strip())
        # Factorize the number
        p, q = factorize(n)
        # Print the result in the required format
        print(f'{n}={p}*{q}')

if __name__ == '__main__':
    main()
