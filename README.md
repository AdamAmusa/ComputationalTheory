
# ComputationalTheory
## Begin
### Option 1
1. Click the `<> Code` button in the repository.
2. Select `Open with Codespaces`.
3. Once the Codespace opens open `tasks.ipynb` and execute each code cell using `Shift + Enter`.
### Option 2
1. Clone the repository `git clone https://github.com/AdamAmusa/ComputationalTheory cd ComputationalTheory`
2. Install jupyter `pip install notebook`
3. Start the notebook server: `jupyter notebook`
4. Run each cell using `Shift + Enter`.

## Binary Representations
### Bit Rotation
`rotl(x, n)`: Rotates bits to the left using [bitwise operations](https://wiki.python.org/moin/BitwiseOperators) from python.
`rotr(x, n)`: Rotates bits to the right using bitwise operations.
### Bit Choose
`ch(x, y, z)`: Each of the bits in x acts as a selector for and selects a bit from y if the selector bit is `1` or z if it is `0`. The conditional behavior of the function follows the principles of diffusion and confusion in cryptographic design because its outputs are unpredictable and non-linear.
### Bit Majority Vote
`maj(x, y, z)`:  This method takes a majority vote of the bits from x, y, and z. If the majority of the bits from a position is 1's or 0's, the corresponding position of the bit is set to the majority.

## Hash Functions
`hash(s)`: Produces a unique hash value (digest) from a single input string, in ways in which the same input always produces the same output and different inputs are unlikely to produce the same output (collision).

## SHA256
`sha256(path)`: This method showcases the SHA-256 padding requirements, abiding by the steps specified from [LNCS 3006 - Security Analysis of SHA-256 and Sisters](https://link.springer.com/content/pdf/10.1007/978-3-540-24654-1_13.pdf), The method takes a file path as input, then reads the file's contents and calculates the SHA256 padding for it.

## Prime Numbers
`eratosthenes_sieve()`: The algorithm is referred to as the  [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes). The method Creates a list of integers from 2 to 100 (n).  At first, p is assigned to 2, which is the smallest prime number. It loops through the list and enumerates the multiples of 2 within it, for example (2p, 3p, 4p), and marks them in the list; in the function, this is done by filtering the multiples from the list of numbers. You then find the smallest number in the newly appended list, overwrite p with that number, and repeat the algorithm until there is no number in the list greater than p. Finally, when the algorithm finishes, the output should be all prime numbers below 100 (n).
 
 `sundaram_sieve()`: This method uses the [Sieve of Sundaram](https://en.wikipedia.org/wiki/Sieve_of_Sundaram) algorithm, Is similar to the [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes), but even numbers are not considered in the sieve process and are skipped, then towards the end it transforms numbers using the formula `i + j + 2ij` to generate primes.

## Roots
`roots()`: Uses the Sundaram Sieve to produce 100 prime numbers, calculates its square root, and then converts its fractional part to binary. Its output is used as initial hash values in cryptographic algorithms like SHA-256.

## Turing Machines
`turing(tape):`This method is a [Turing](https://plato.sydney.edu.au/entries/turing-machine/#TuriDefi) inspired machine which performs a binary operation. It iterates over a tape starting from the right-most bit which is the least significant bit, then switches `1` to `0` when it is encountered or `0` to `1` if encountered. When the tape reaches its first 0 it finally exits the operation.

## Computational Complexity
`permutations(generated_permutations,current_permutation, elements_to_permute)`: Is a recursive algorithm specialised in creating a list of possible permutations of the array `[1, 2, 3, 4, 5]`.

`bubble_sort()`: Is an algorithm used to sort elements in a list, It works through iterating through each element in the list and swapping the adjacent element if it is less than, and repeats until all the elements are sorted.