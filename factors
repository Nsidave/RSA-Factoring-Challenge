#!/usr/bin/python3
import sys

def factorize(n):
    # Try to find a factor of n by starting at 2 and incrementing by 1
    for i in range(2, n):
        # If n is evenly divisible by i, then we found a factor
        if n % i == 0:
            return (i, n // i)
    # If we didn't find a factor, then n is prime and cannot be further factorized
    return (n, 1)

def main():
    # Open the input file for reading
    with open(sys.argv[1], 'r') as f:
        # Read each line of the file
        for line in f:
            # Strip the newline character from the end of the line
            n = int(line.strip())
            # Factorize the number
            p, q = factorize(n)
            # Print the result in the required format
            print(f'{n}={p}*{q}')

if __name__ == '__main__':
    main()
