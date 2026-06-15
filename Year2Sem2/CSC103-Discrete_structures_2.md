$$\DeclareMathOperator{\gcd}{gcd}
\def\nequiv{\not\equiv}
$$

# Modular Arithmetic
## Divisibility
**$a$** is divisible by $b$  denoted by $b \mid a$ if there's an integer $k$ such that $$a = b \times k$$
The intuitive sense of this definition is simple (for positive a & b):
- Say we have an object
- We'd like to split 'em into groups of size $b$
- This is possible if $a$ is divisible by $b$
- $k$ is the resulting number of groups
E.g.,: $3\mid \frac{12}{= 4}$
## Division with remainders
Suppose $b$ is a positive integer. The result of the division of $a$ by $b$ is a pair of integers, $q$ called quotient & $r$ called remainder such that $$a = q \times b + r$$ and $0 \leq r \leq b$
E.g.,:
- $a = 15, b = 4$. Then $15 = 3 \times 4 + 3$ & $q=3,r=3$

## Modular Arithmetic?
- System of arithmetic for integers
- Wrap around after reaching a certain value called **_modulus_**
- Central mathematical concept in cryptography
- ~~also used in reading clock~~
## Congruence
- In cryptography, congruence ($\equiv$) instead of equality ($=$)
E.g.,
- $15 \equiv 3 \text{ mod }12$
- $23 \equiv 11 \text{ mod } 12$
- $33 \equiv 3 \text{ mod } 10$
- $10 \equiv -2 \text{ mod } 12$
	- wait, what?
	- ⬇️
	- ![[Drawing 2026-02-01 17.17.08.excalidraw]]
## Congruence Relations
We say that two numbers $a$ and $b$ are **_congruent modulo_** $m$ if they have the same remainder when divided by $m$. We write $$a \equiv b \pmod{m}$$
## Properties of Modular Arithmetic
1. **Addition:**
\[(a mod n) + (b mod n)] mod n = (a + b) mod n
2. **Subtraction:**
\[(a mod n) - (b mod n)] mod n = (a - b) mod m
3. **Mulptiplcation:**
\[(a mod n) \* (b mod n)] mod n = (a * b) mod n
### Laws & Identities
0. Format: Property
	- Expression
1. Commutative Laws
	- (a + b) mod n = (b + a) mod n
	- (a \* b) mod n = (b * a) mod n
2. Associative Laws
	- \[(a + b) + c] mod n = \[a + (b + c)] mod n
	- \[(a * b) * c] mod n = \[a * (b * c)] mod n
3. Distributive Laws
	- \[a * (b + c)] mod n = \[(a * b) + (a * c)] mod n
4. Identities
	- (0 + a) mod n = a mod n
	- (1 * a) mod n = a mod n
5. Additive Inverse
	- For each $a \in Z_n$, there exist a '$-a$' such that $a + (-a) \equiv 0$ mod n
# Congruence Relations & Modular Exponentiation
## Congruence Relation
If $a$ and $b$ are integers and $m$ is a positive integer, them $a$ is ***congruent*** to $b$ if m iff $m \mid (a-b)$
- The notation $a\equiv b \pmod{m}$ says that $a$ is congruent to $b$ modulo $m$
- We say that $a \equiv b \pmod{m}$ is a congruence and that $m$ is its modulus
- Two integers are congruent mod $m$ if and only if they have the same remainder when divided by $m$
- If $a$ isn't congruent to $b$ modulo $m$, we write $a \nequiv b \pmod{m}$
## Modular Exponentiation
- a type of exponentiation performed over a modulus
- i.e., $a^b$ mod $m$ or $a^b$ (mod $m$)
$\def\mod{\text{ mod }}$
E.g.,
- $2^{33} \pmod {30}$
- $3^{100} \pmod {29}$
- $31^{500} \pmod{30}$
	- ![[Drawing 2026-02-02 09.28.06.excalidraw]]
- $242^{329} \pmod {243}$
	- ![[CSC103-Discrete_structures_2 2026-02-02 09.32.25.excalidraw]]
- $11^7 \pmod{13}$
	- ![[CSC103-Discrete_structures_2 2026-02-02 09.40.29.excalidraw]]
- $88^7 \pmod{187}$
	- ![[CSC103-Discrete_structures_2 2026-02-02 09.46.13.excalidraw]]
- What's the last 2 digits of $29^5$?
	- ![[CSC103-Discrete_structures_2 2026-02-02 09.56.59.excalidraw]]
- $23^{16} \mod 30$

$$\begin{align}
= (((23^2)^2)^2)^2 \mod 30 \\
= (((-7^2)^2)^2)^2 \mod 30 \\
= ((49^2)^2)^2 \mod 30 \\
=((19^2)^2)^2 \mod 30 \\
= ((-11^2)^2)^2 \mod 30 \\
= 1 \mod 30 \\
= 1👍

\end{align}$$

# GCD And Euclidian Algorithm
## Greatest Common Divisor (GCD)
Let $a,b \in Z - {0}$. The largest integer $d$ such that $d\mid a$ and also $d \mid b$ is called the **greatest common divisor** of $a$ & $b$. It's denoted by gcd(a,b).
E.g., $\gcd(24,36) = 12$

The integers $a$ & $b$ are **relatively coprime** if and only if gcd(a,b) = 1.
E.g.,: 17, 22 (22 != Prime btw) ^Coprime

The integers $a_1, a_2,…a_n$ are **pairwise relatively prime** if and only if gcd($a_i,a_j$) whenever $1 \leq i \lt j \leq n$

E.g.,: 10, 17, & 21 are pairwise relatively prime, since gcd(10,17) = gcd(10,21) = gcd(17, 21) = 1.

##  Euclidian Algorithm

> [!NOTE] Lemma
> Let $a=bq+r$, where $a,b,q,$ and $r$  are integers.
> Then $\gcd(a,b) = \gcd(b,r).$

> [!NOTE] Proof
> Suppose that $d$ divides both $a$ & $b$. Then $d$ also divides $a-bq=r$.
> Hence, any common divisor of $a$ & $b$ must be also be a common divisor of $b$ & $r$.
> For the opposite direction suppose that $d$ divides both $b$ & $r$. Then $d$ also divides $bq+r=a$. Hence, any common divisor of $b$ & $r$ must be a common divisor of $a$ & $b$.
> $\therefore \gcd(a,b) = \gcd(b,r)$

This means that if $a \gt b$, then gcd(a,b), gcd(a,b, mod b), which directly yields the algorithm. (Note that both args have gotten smaller. One can show that its complexity is $O(\log b)$
**To compute gcd(a,b):**
1. Divide $a$ by $b$, get remainder $r$
2. Replace $a$ with $b$, $b$ with $r$
3. Repeat until $r=0$. The last non-zero remainder is the GCD

E.g.,
1. gcd(252,105)
	1. 252 % 105 = 42
	2. 105 % 42 = 21
	3. 42 % 21 = 0
	4. $\therefore \gcd(252,105)=21$
# Co-Prime, Phi Function & Multiplicative Inverse 
## Totient Function

> [!Info] Formula
> $$\phi(n)=n\prod_{p\, | \, n}(1-\frac{1}{p})$$

- denoted as $\phi(n)$
- $\phi (n)$ = number of positive integers less than $n$ that are relatively prime to $n$

E.g.,
- $\phi(31)=30$ since 31 is prime
##  Multiplicative Inverse

> [!NOTE] Definition
> 
>
>An integer $\bar{a}$ such that $\bar{a}a \equiv 1 (\mod m)$ is called a **multiplicative inverse** of $a (\mod m)$

Multiplicative inverses can be used to solve congruences. If $ax \equiv b (\mod m)$, then $\bar{a}ax \equiv (\bar{a}b)(\mod m)$, thus $x \equiv (\bar{a}b)(\mod m)$.
# Cryptography & RSA
**Cryptography**: practice & study of techniques for secure communication in the presence of adversarial behavior

## Foundations: Modular Arithmetic

> [!NOTE] Definition
> $$ a \equiv b \pmod{n}$$
> Two integers $a$ and $b$ are congruent modulo $n$ if their difference (a-b) is divisible by n

Think of a 12-hour clock. If it's 10:00 and 5 hours pass, it's 3:00, not 15:00.
$$10 + 5 \pmod{12} = 3$$
### Power of Modulo
In cryptography, modular arithmetic acts as a "**trapdoor**." It keeps numbers withing a fixed range, preventing overflow and making it computationally difficult to reverse keys without specific keys.
### Key Properties
[[#Properties of Modular Arithmetic|Here]] ain't writing that again

### Primes
The "atoms" of number theory. Every integer > 1 is either prime or a unique product of primes. RSA relies on the difficulty of reversing this multiplication

### Greatest Common Divisor
Largest positive integer that divides each of the integers
[[#GCD And Euclidian Algorithm|Further reading]]
- [[#Euclidian Algorithm]]
- [[#^Coprime|Coprime]]
### Euler's Totient Function $\phi\,(n)$
$\phi\,(n)$ is the count of positive integers $\leq n$ that are **coprime** to $n$
#### Critical Cases for RSA
- If $p$ is prime: $\phi(p)=p-1$
- if $n = p \cdot q$ (distinct primes): $\phi(n)=(p-1)(q-1)$
#### Euler's Theorem
If gcd(a,n) = 1, then:
$$a^{\phi(n)} \equiv 1 \pmod{n}$$
#### Why it matters
This theorem is the "trapdoor" mechanism. It allows us to "undo" the encryption exponentiation

> [!info] The RSA Connection
> If we know $\phi(n)$, we can find a decryption exponent $d$ that reverses the encryption exponent $e$, without $\phi(n)$, finding $d$ is computationally impossible.

### RSA Keygen
1. **Select primes**
Choose two (2) large distinct prime numbers, $p$ and $q$
2. **Compute modulus** ($n$)
Calculate $n = p \times q$. $n$ is the modulus for both keys
3. **Calculate totient**
Calculate $\phi(n) = (p-1)(q-1)$
4. **Choose exponent** ($e$)
Pick $e$ such that $1 \gt e \gt \phi(n)$ and $gcd(e,\phi(n))=1$
5. **Compute private key** ($d$)
Find $d$ such that $e \times d \equiv 1 \pmod{\phi(n)}$

The result is public key that uses (n,e) and private key that uses (n,d). Security depends on the difficulty of factoring $n$ to find $p$ and $q$.

1. Let $p = 5$, $q=11$, and $e=3$. Find the public and private keys

$$
\begin{align}
n = 5 \times 11 \\
n= 55\\\\
\phi(n)=(5-1)(11-1)\\
\phi(n)=40\\\\
e(d) \equiv 1 \pmod{40}\\
3(67) \equiv 1 \pmod{40}\\
201 \equiv 1 \pmod{40}
\end{align}$$
Public Key: (55, 3)
Private Key: (55, 67)

2. If the public key is ($n=35,e=5$), encrypt the message M = 2.
$$\begin{align}
C= 2^{5} \pmod{35}\\
2^5 = 32 \pmod{35}\\\\
C =32
\end{align}
$$
3. Why can't we just pick $e=2$ if $n=35$?
$\phi(35)=24$. The requirement for exponents are $1 \gt e \gt \phi(n)$ and $\gcd(e,\phi(n)) = 1$. $\gcd(2, 24) = 2$, which violates the second requirement.

# Combinatorics
Discrete math branch focused on counting, arrangement, and selection

## Multiplication Principle
## Permutation
$$P(n,r)= \frac{n!}{(n-r)!}$$
## Combination
$$C(n,r)=\frac{n!}{r!(n-r)!}$$
## Pigeonhole Principle
If $n$ items are put to $m$ containers, and $n > m$, then at least one container must contain more than one item.
### Generalized Pigeonhole Principle
$$[\,n/k\,] \text{ items}$$
# Discrete Probability 
## Probability $P(E)$
Numerical measure of the likelihood that an event occur
$$ 0 \leq P(E) \leq 1$$
0 = impossible
1 = guarantee
### Formula
$$P(E) = |E|\,/\,|S|$$
$|E|$ = # of outcomes to event e
$|S|$ = sample space
### Sample space
Possible outcomes of a rand experiment
1. Collectively exhaustive
Must cover every single possible result of the experiment
2. Mutually exclusive 
No two distinct in the set can occur simultaneously

# 
