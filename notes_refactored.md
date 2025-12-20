# Master GATE CS Notes: Comprehensive Reference Guide

## 📚 **COMPREHENSIVE INDEX**

### **Volume 1: Engineering Mathematics, Discrete Mathematics, and General Aptitude**

#### **1. Discrete Mathematics**
- **1.1 Set Theory & Algebra**
  - Set Theory
  - Relations
  - Countable Uncountable Set
  - Partial Order
  - Lattice
  - Identity Function
  - Mathematical Induction
  - Number Theory
  - Onto
  - Polynomials
  - Functions
  - Binary Operation
  - Group Theory

- **1.2 Mathematical Logic**
  - First Order Logic
  - Logical Reasoning
  - Propositional Logic

- **1.3 Graph Theory**
  - Counting
  - Degree of Graph
  - Graph Coloring
  - Graph Connectivity
  - Graph Isomorphism
  - Graph Matching
  - Graph Planarity

- **1.4 Combinatory**
  - Balls In Bins
  - Combinatory
  - Counting
  - Generating Functions
  - Modular Arithmetic
  - Pigeonhole Principle
  - Recurrence Relation
  - Summation

#### **2. Engineering Mathematics**
- **2.1 Calculus**
  - Limits and Continuity
  - Differentiation
  - Integration
  - Differential Equations

- **2.2 Linear Algebra**
  - Matrices and Determinants
  - Eigenvalues and Eigenvectors
  - Vector Spaces
  - Linear Transformations
  - LU Decomposition

- **2.3 Probability and Statistics**
  - Probability Theory
  - Random Variables
  - Distributions
  - Statistical Inference

#### **3. General Aptitude**
- **3.1 Verbal Ability**
- **3.2 Numerical Ability**
- **3.3 Logical Reasoning**

### **Volume 2: Core Computer Science Subjects**

#### **1. Theory of Computation**
- **1.1 Finite Automata**
- **1.2 Regular Languages**
- **1.3 Context-Free Languages**
- **1.4 Turing Machines**
- **1.5 Computability**
- **1.6 Complexity Theory**

#### **2. Algorithms and Data Structures**
- **2.1 Algorithm Analysis**
- **2.2 Sorting and Searching**
- **2.3 Graph Algorithms**
- **2.4 Dynamic Programming**
- **2.5 Data Structures**

#### **3. Computer Organization and Architecture**
- **3.1 Number Systems**
- **3.2 Boolean Algebra**
- **3.3 Processor Design**
- **3.4 Memory Hierarchy**
- **3.5 I/O Systems**
- **3.6 Ethernet Bridging**

#### **4. Operating Systems**
- **4.1 Process Management**
- **4.2 Memory Management**
- **4.3 File Systems**
- **4.4 Synchronization**
- **4.5 CPU Scheduling**

#### **5. Database Management Systems**
- **5.1 ER Model**
- **5.2 Relational Model**
- **5.3 SQL**
- **5.4 Normalization**
- **5.5 Transactions**
- **5.6 File Organization**

#### **6. Computer Networks**
- **6.1 Network Models**
- **6.2 Physical Layer**
- **6.3 Data Link Layer**
- **6.4 Network Layer**
- **6.5 Transport Layer**
- **6.6 DHCP**
- **6.7 ICMP**
- **6.8 NAT**

#### **7. Software Engineering**
- **7.1 SDLC Models**
- **7.2 Requirements Engineering**
- **7.3 Software Design**
- **7.4 Testing**

#### **8. Compiler Design**
- **8.1 Lexical Analysis**
- **8.2 Syntax Analysis**
- **8.3 Semantic Analysis**
- **8.4 Code Generation**
- **8.5 Constant Propagation**

---

## 🔍 **Quick Navigation Guide**
- **Search**: Use Ctrl+F to find specific topics instantly
- **Formulas**: Look for $ delimiters around mathematical expressions
- **GATE Tips**: Search for "GATE trap" and "Common pattern" annotations
- **Cross-references**: Follow "(See X.Y)" links to related sections
- **Examples**: Each section includes worked problems and solutions

---

This master note is a compiled, exhaustive reference designed specifically for solving problems from the provided GATE question banks (Volume 1: Engineering Math, Discrete Math, General Aptitude; Volume 2: Core CS Subjects). It covers **every topic and subtopic** from the Tables of Contents in both volumes, drawing from standard GATE syllabus knowledge, key formulas, theorems, proofs, algorithms, examples, and common problem-solving patterns. The structure mirrors the TOCs for easy navigation. Each subtopic includes:

- **Key Concepts**: Core definitions and ideas.
- **Formulas/Theorems**: Essential equations, rules, and proofs (with brief derivations where closed-ended math is involved).
- **Problem-Solving Tips**: Strategies for typical GATE questions, with recall triggers.
- **Examples**: Quick illustrative problems (inspired by bank patterns).

Use this as a "one-stop recall sheet"—scan for keywords from a problem, review formulas, and apply tips. Total coverage: ~100% of listed subtopics (1,700+ questions across volumes). Organized by volume for clarity.

**How to Use These Notes:**

- **Quick Lookup**: Use Ctrl+F to find specific topics
- **Formula Reference**: All key formulas are marked with $ delimiters
- **Problem Patterns**: Look for "GATE trap" and "Common pattern" annotations
- **Cross-references**: "(See X.Y)" links to related topics
- **Practice Strategy**: Cover examples first, then attempt similar problems

---

## Volume 1: Engineering Mathematics, Discrete Mathematics, and General Aptitude

### 1. Discrete Mathematics: Combinatory (50 Questions)

### 1.1 Balls In Bins (4) {#11-balls-in-bins-4}

**Key Concepts**: Models distributing indistinguishable/distinguishable objects into bins; stars and bars for indistinguishable cases. Core decision tree: (1) Are balls distinguishable? (2) Are bins distinguishable? (3) Can bins be empty?

**Formulas/Theorems**:

- **Indistinguishable balls, distinct bins, bins can be empty**: $\binom{n+k-1}{k-1}$ (stars and bars; proof: arrange n stars and k-1 bars in a line)
- **Indistinguishable balls, distinct bins, no empty bin**: $\binom{n-1}{k-1}$ (place one in each bin first)
- **Distinct balls, distinct bins**: $k^n$ (each ball has k choices)
- **Distinct balls, distinct bins, no empty bin**: $k! \cdot S(n,k)$ where $S(n,k) = \frac{1}{k!}\sum_{i=0}^{k}(-1)^i\binom{k}{i}(k-i)^n$ (Stirling second kind)
- **Distinct balls, indistinct bins**: $\sum_{i=1}^{\min(n,k)} S(n,i)$ (Bell numbers)

**Problem-Solving Tips**:

- GATE trap: Forgetting to check if bins/balls are labeled
- Common pattern: "distribute among groups" → indistinct bins
- Quick check: For n=k=2, should get specific known values
- Inclusion-exclusion for "at most r per bin": subtract bad arrangements

**Examples**:

- 5 identical balls, 3 bins: $\binom{7}{2} = 21$
- 3 distinct balls, 2 bins (no empty): $2^3 - 2 = 6$
- 4 distinct balls, 3 indistinct bins: $S(4,1)+S(4,2)+S(4,3) = 1+7+6 = 14$
- Distribute 10 identical items, each person gets at least 2, among 3 people: $\binom{10-6+3-1}{3-1} = \binom{6}{2} = 15$

### 1.2 Combinatory (22) {#12-combinatory-22}

**Key Concepts**: Combinatorics studies finite or countable discrete structures. Core principle: systematic enumeration without explicit listing.

**Fundamental Counting Principles**:

**1. Addition Principle** (Disjoint Union):

If task A can be done in m ways and task B in n ways, and A and B are mutually exclusive, then "A OR B" can be done in m+n ways.

- Formal: If $A \cap B = \emptyset$, then $|A \cup B| = |A| + |B|$
- Extension: $|A_1 \cup A_2 \cup \cdots \cup A_k| = \sum |A_i|$ when pairwise disjoint

**2. Multiplication Principle** (Cartesian Product):

If task A can be done in m ways, and for each way, task B can be done in n ways, then "A AND B" can be done in m×n ways.

- Formal: $|A \times B| = |A| \cdot |B|$
- Extension: For k independent tasks with $n_i$ choices each: $\prod_{i=1}^{k} n_i$

**Permutations**: Ordered arrangements

**Linear Permutations of n Distinct Objects**:

- Full permutation: $P(n,n) = n!$
- Derivation: n choices for first position, (n-1) for second, ..., 1 for last
- Product: $n \cdot (n-1) \cdot (n-2) \cdots 2 \cdot 1 = n!$

**r-Permutations** (arrangements of r from n):

- Formula: $P(n,r) = \frac{n!}{(n-r)!}$
- Derivation: n choices for first, (n-1) for second, ..., (n-r+1) for r-th position
- Product: $n(n-1)(n-2)\cdots(n-r+1) = \frac{n!}{(n-r)!}$
- Alternative notation: $_nP_r$ or $A_n^r$

**Permutations with Repetitions** (Multiset Permutations):

- Given n objects where $n_1$ are type 1, $n_2$ are type 2, ..., $n_k$ are type k
- Where $n_1 + n_2 + \cdots + n_k = n$
- Formula: $\frac{n!}{n_1! n_2! \cdots n_k!}$
- **Proof**: If all objects were distinct: n! arrangements. But objects of same type are indistinguishable. Dividing by $n_i!$ for each type removes overcounting from permuting identical items.
- Example: "SUCCESS" has 7 letters: S(3), U(1), C(2), E(1)
    - Arrangements: $\frac{7!}{3! \cdot 1! \cdot 2! \cdot 1!} = \frac{5040}{12} = 420$

**Circular Permutations**:

- Arranging n distinct objects in a circle: $(n-1)!$
- **Derivation**: Fix one object to break rotational symmetry (prevents counting rotations as different). Arrange remaining (n-1) objects linearly.
- If clockwise/counterclockwise same (e.g., necklace): $\frac{(n-1)!}{2}$
- With r identical items: More complex, use Burnside's lemma

**Derangements** (!n): Permutations where no element appears in its original position

**Formula**: $D_n = n! \sum_{i=0}^{n} \frac{(-1)^i}{i!}$

**Alternative**: $D_n = n! \left(1 - \frac{1}{1!} + \frac{1}{2!} - \frac{1}{3!} + \cdots + \frac{(-1)^n}{n!}\right)$

**Recurrence**: $D_n = (n-1)[D_{n-1} + D_{n-2}]$ for $n \geq 2$, with $D_0=1, D_1=0$

**Derivation via Inclusion-Exclusion**:

Let $A_i$ = permutations where element i is in position i

- Want: $|\overline{A_1} \cap \overline{A_2} \cap \cdots \cap \overline{A_n}|$ (none in original position)
- By inclusion-exclusion: $D_n = n! - |A_1 \cup A_2 \cup \cdots \cup A_n|$
- $|A_i| = (n-1)!$ (fix element i, permute rest)
- $|A_i \cap A_j| = (n-2)!$ (fix i and j)
- $|A_{i_1} \cap \cdots \cap A_{i_k}| = (n-k)!$
- Number of k-intersections: $\binom{n}{k}$
- Therefore: $D_n = n! - \binom{n}{1}(n-1)! + \binom{n}{2}(n-2)! - \cdots + (-1)^n\binom{n}{n}0!$
- Simplify: $D_n = n! \sum_{k=0}^{n} \frac{(-1)^k}{k!}$

**Asymptotic**: $D_n \approx \frac{n!}{e}$ (since $e = \sum_{k=0}^{\infty} \frac{1}{k!}$)

**Probability**: Fraction of derangements = $\frac{D_n}{n!} \approx \frac{1}{e} \approx 0.368$ (independent of n for large n!)

**Small values**:

- $D_0 = 1$ (empty permutation)
- $D_1 = 0$ (impossible to derange 1 element)
- $D_2 = 1$ (swap)
- $D_3 = 2$ (231, 312)
- $D_4 = 9$
- $D_5 = 44$

**Applications**:

- Hat-check problem: n people check hats, retrieve randomly. Probability nobody gets own hat ≈ 1/e
- Secret Santa arrangements where nobody draws self
- Rencontres problem

**Combinations**: Unordered selections

**r-Combinations from n objects**:

- Formula: $C(n,r) = \binom{n}{r} = \frac{n!}{r!(n-r)!}$
- Derivation: $P(n,r)$ counts ordered selections. Each unordered set of r elements corresponds to r! orderings.
- Thus: $C(n,r) = \frac{P(n,r)}{r!} = \frac{n!}{r!(n-r)!}$

**Problem-Solving Tips**:

- Decide: Does order matter? (Permutation) or not? (Combination)
- For restrictions: Use complementary counting or case analysis
- Symmetry: Look for ways to reduce by symmetry
- GATE trap: Distinguishing between "at least one" vs "exactly one"
- Overcounting identical items: Divide by appropriate factorials
- Use generating functions for complex constraints

**Examples**:

1. Arrange "MISSISSIPPI" (11 letters: M(1), I(4), S(4), P(2)):
    - $\frac{11!}{1! \cdot 4! \cdot 4! \cdot 2!} = \frac{39916800}{1 \cdot 24 \cdot 24 \cdot 2} = \frac{39916800}{1152} = 34650$
2. Derangements of 4 items {1,2,3,4}:
    - $D_4 = 4! \sum_{i=0}^{4} \frac{(-1)^i}{i!} = 24(1-1+\frac{1}{2}-\frac{1}{6}+\frac{1}{24}) = 24 \cdot \frac{3}{8} = 9$
    - Explicit: 2143, 2341, 2413, 3142, 3412, 3421, 4123, 4312, 4321
3. Arrange 5 people in a circle: $(5-1)! = 24$
4. Words from "COMPUTER" with vowels together:
    - Treat OUE as one unit: 6 units (CMPTR + OUE)
    - Arrange 6 units: $6!$
    - Arrange 3 vowels within: $3!$
    - Total: $6! \cdot 3! = 720 \cdot 6 = 4320$

### 1.3 Counting (4) {#13-counting-4}

**Key Concepts**: Fundamental enumeration techniques form the basis of combinatorial analysis. Bijections establish equinumerosity between sets.

**Bijective Proofs** (Combinatorial Proofs):

- To prove $|A| = |B|$, construct bijection $f: A \to B$
- Elegant alternative to algebraic manipulation
- Example: $\binom{n}{k} = \binom{n}{n-k}$
    - Bijection: Each k-subset corresponds to its complement (n-k)-subset

**Counting Functions**:

**1. Functions from A to B** ($|A|=n, |B|=k$):

- Total functions: $k^n$ (each of n elements has k choices)
- **Proof**: By multiplication principle

**2. Injective Functions** (One-to-one):

- Requires $n \leq k$ (pigeonhole principle)
- Count: $P(k,n) = \frac{k!}{(k-n)!}$
- **Derivation**: First element: k choices, second: k-1, ..., n-th: k-n+1
- $k(k-1)(k-2)\cdots(k-n+1) = \frac{k!}{(k-n)!}$

**3. Surjective Functions** (Onto):

- Requires $n \geq k$ (can't cover k elements with fewer than k)
- Count: Uses inclusion-exclusion with Stirling numbers
- Formula: $k! \cdot S(n,k)$ where $S(n,k)$ is Stirling number of second kind
- $S(n,k) = \frac{1}{k!}\sum_{j=0}^{k}(-1)^{k-j}\binom{k}{j}j^n$

**4. Bijective Functions**:

- Requires $n = k$ (bijection exists only between equinumerous sets)
- Count: $n!$ (permutations of range)

**Inclusion-Exclusion Principle** (PIE):

**Two Sets**:

$|A \cup B| = |A| + |B| - |A \cap B|$

**Three Sets**:

$|A \cup B \cup C| = |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C|$

**General Formula** (n sets):

$\left|\bigcup_{i=1}^{n} A_i\right| = \sum_{i} |A_i| - \sum_{i<j} |A_i \cap A_j| + \sum_{i<j<k} |A_i \cap A_j \cap A_k| - \cdots + (-1)^{n-1}|A_1 \cap \cdots \cap A_n|$

**Compact notation**:

$\left|\bigcup_{i=1}^{n} A_i\right| = \sum_{\emptyset \neq S \subseteq \{1,\ldots,n\}} (-1)^{|S|-1} \left|\bigcap_{i \in S} A_i\right|$

**Complement form** (often easier):

$\left|\overline{A_1 \cup \cdots \cup A_n}\right| = |U| - \sum_{i}|A_i| + \sum_{i<j}|A_i \cap A_j| - \cdots$

**Applications**:

**1. Derangements** (as seen in 1.2):

Count permutations with no fixed point using PIE

**2. Surjective function count**:

- Map n distinct balls to k distinct bins with no empty bin
- $A_i$ = functions missing bin i
- Want: $k^n - |A_1 \cup \cdots \cup A_k|$
- $|A_i| = (k-1)^n$ (avoid one bin)
- $|A_i \cap A_j| = (k-2)^n$ (avoid two bins)
- Result: $\sum_{j=0}^{k} (-1)^j \binom{k}{j}(k-j)^n$

**3. Euler's Totient Function**:

$\phi(n)$ counts integers in $\{1,\ldots,n\}$ coprime to n

- Use PIE over prime divisors of n
- If $n = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k}$:
- $\phi(n) = n\left(1-\frac{1}{p_1}\right)\left(1-\frac{1}{p_2}\right)\cdots\left(1-\frac{1}{p_k}\right)$

**Double Counting** (Counting in two ways):

- Count same set using two different methods
- Equate results to prove identity
- Example: $\sum_{k=0}^{n} \binom{n}{k} = 2^n$
    - LHS: Count k-subsets for each k
    - RHS: Each element in/out → $2^n$ subsets

**Problem-Solving Strategy**:

1. Identify what to count (be precise about "distinct" vs "identical")
2. Check if direct formula applies (permutation/combination)
3. If restrictions exist, consider:
    - Complementary counting
    - Inclusion-exclusion
    - Case analysis
    - Bijection to simpler problem
4. For existence questions: Pigeonhole principle

**Examples**:

1. Ways to choose 2 from 5 **with order**: $P(5,2) = \frac{5!}{3!} = 20$
2. Ways to choose 2 from 5 **without order**: $\binom{5}{2} = 10$
3. Surjective functions from $\{1,2,3\}$ to $\{A,B\}$:
    - Total functions: $2^3 = 8$
    - Missing A: 1 (all to B)
    - Missing B: 1 (all to A)
    - Surjective: $8 - 2 = 6$
    - Or: $2! \cdot S(3,2) = 2 \cdot 3 = 6$
4. Integers ≤100 divisible by 2 or 3:
    - Div by 2: $\lfloor 100/2 \rfloor = 50$
    - Div by 3: $\lfloor 100/3 \rfloor = 33$
    - Div by 6: $\lfloor 100/6 \rfloor = 16$
    - By PIE: $50 + 33 - 16 = 67$

### 1.4 Generating Functions (6) {#14-generating-functions-6}

**Key Concepts**: Generating functions transform counting problems into algebraic manipulations of formal power series. They encode sequences as coefficients of polynomials or infinite series.

**Philosophy**: Instead of finding closed form directly, encode the sequence as a function, manipulate algebraically, then extract coefficients.

**Ordinary Generating Functions (OGF)**:

For sequence $\{a_0, a_1, a_2, \ldots\}$, the OGF is:

$G(x) = a_0 + a_1x + a_2x^2 + \cdots = \sum_{n=0}^{\infty} a_n x^n$

**Key OGFs**:

1. **Geometric series**: $\frac{1}{1-x} = 1 + x + x^2 + x^3 + \cdots = \sum_{n=0}^{\infty} x^n$
    - Valid for $|x| < 1$ (but we treat as formal series)
2. **Binomial series**: $(1+x)^n = \sum_{k=0}^{n} \binom{n}{k} x^k$
    - For negative/fractional n: $(1+x)^{-n} = \sum_{k=0}^{\infty} \binom{n+k-1}{k} (-1)^k x^k$
3. **Generalized geometric**: $\frac{1}{(1-x)^k} = \sum_{n=0}^{\infty} \binom{n+k-1}{k-1} x^n$
    - **Proof**: Differentiate $\frac{1}{1-x}$ repeatedly
    - Interpretation: Ways to place n indistinguishable balls in k bins
4. **Exponential**: $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$

**Operations on Generating Functions**:

**1. Addition**: If $A(x) = \sum a_n x^n$ and $B(x) = \sum b_n x^n$:

- $A(x) + B(x) = \sum (a_n + b_n) x^n$
- Interpretation: Two independent ways to achieve outcome

**2. Multiplication (Convolution)**:

- $A(x) \cdot B(x) = \sum_{n=0}^{\infty} \left(\sum_{k=0}^{n} a_k b_{n-k}\right) x^n$
- Coefficient of $x^n$: $c_n = \sum_{k=0}^{n} a_k b_{n-k}$
- Interpretation: Sequential choices or compositions

**3. Scalar multiplication**: $c \cdot A(x) = \sum (c \cdot a_n) x^n$

**4. Differentiation**: $A'(x) = \sum n \cdot a_n x^{n-1}$

- Brings down exponent as coefficient

**5. Integration**: $\int A(x)dx = \sum \frac{a_n}{n+1} x^{n+1}$

**6. Substitution**: Replace $x$ with $f(x)$

**Coefficient Extraction**:

Notation: $[x^n]G(x)$ denotes coefficient of $x^n$ in $G(x)$

**Methods**:

1. **Series expansion**: Expand and read coefficient
2. **Partial fractions**: Decompose rational functions
3. **Binomial theorem**: For powers of binomials
4. **Residue theorem** (advanced): Complex analysis

**Applications**:

**1. Counting Compositions**:

- Compositions of n (ordered partitions): How many ways to write $n = a_1 + a_2 + \cdots + a_k$ where $a_i \geq 1$?
- Each position: Choose positive integer
- GF for one part: $x + x^2 + x^3 + \cdots = \frac{x}{1-x}$
- For k parts: $\left(\frac{x}{1-x}\right)^k$
- For any number of parts: $\sum_{k=1}^{\infty} \left(\frac{x}{1-x}\right)^k = \frac{x/(1-x)}{1-x/(1-x)} = \frac{x}{1-2x}$
- Coefficient: $[x^n]\frac{x}{1-2x} = 2^{n-1}$ for $n \geq 1$

**2. Integer Partitions**:

- Partitions of n (unordered): $n = a_1 + a_2 + \cdots$ where $a_1 \geq a_2 \geq \cdots$
- GF (Euler): $P(x) = \prod_{i=1}^{\infty} \frac{1}{1-x^i}$
- Interpretation: For each i, choose how many i's to include: $1 + x^i + x^{2i} + \cdots = \frac{1}{1-x^i}$
- No closed form, but recurrences exist

**3. Coin Change Problem**:

- Coins of denominations $d_1, d_2, \ldots, d_k$, ways to make amount n?
- GF: $\prod_{i=1}^{k} (1 + x^{d_i} + x^{2d_i} + \cdots) = \prod_{i=1}^{k} \frac{1}{1-x^{d_i}}$
- Example: Coins {1,2,5}, coefficient of $x^n$ in $\frac{1}{(1-x)(1-x^2)(1-x^5)}$

**4. Recurrence Relations**:

- Fibonacci: $F_n = F_{n-1} + F_{n-2}$, $F_0=0, F_1=1$
- Let $G(x) = \sum_{n=0}^{\infty} F_n x^n$
- Multiply recurrence by $x^n$, sum over n:
    
    $\sum_{n=2}^{\infty} F_n x^n = \sum_{n=2}^{\infty} F_{n-1} x^n + \sum_{n=2}^{\infty} F_{n-2} x^n$
    
- $G(x) - F_0 - F_1x = x(G(x) - F_0) + x^2 G(x)$
- $G(x) - x = xG(x) + x^2G(x)$
- $G(x) = \frac{x}{1-x-x^2}$
- Partial fractions: $\frac{x}{1-x-x^2} = \frac{1}{\sqrt{5}}\left(\frac{1}{1-\phi x} - \frac{1}{1-\psi x}\right)$
    
    where $\phi = \frac{1+\sqrt{5}}{2}, \psi = \frac{1-\sqrt{5}}{2}$
    
- Extract: $F_n = \frac{\phi^n - \psi^n}{\sqrt{5}}$ (Binet's formula)

**Exponential Generating Functions (EGF)**:

For sequence $\{a_0, a_1, a_2, \ldots\}$:

$\hat{G}(x) = \sum_{n=0}^{\infty} a_n \frac{x^n}{n!}$

**When to use EGF**: Problems involving **labeled** objects or **permutations**

**Key property**: Product of EGFs corresponds to labeled compositions

- If $\hat{A}(x) \cdot \hat{B}(x) = \hat{C}(x)$, then:
- $c_n = \sum_{k=0}^{n} \binom{n}{k} a_k b_{n-k}$
- The $\binom{n}{k}$ accounts for choosing which k objects get labels from first set

**Example - Permutations with restrictions**:

- Derangements: $D(x) = \sum_{n=0}^{\infty} D_n \frac{x^n}{n!}$
- Recurrence leads to: $D(x) = \frac{e^{-x}}{1-x}$
- Verifies: $D_n \approx \frac{n!}{e}$

**Problem-Solving Strategy**:

1. **Model the problem**: What choices are being made?
2. **Write GF for single choice**: Based on constraints
3. **Combine using operations**: Multiplication for sequential, addition for alternatives
4. **Simplify algebraically**: Use known series, partial fractions
5. **Extract coefficient**: Use appropriate technique

**GATE Tips**:

- OGF for unordered/unlabeled problems
- EGF for ordered/labeled problems
- Product of GFs → Convolution of sequences
- For rational GF $\frac{P(x)}{Q(x)}$: Roots of $Q(x)$ determine growth rate
- Partial fractions essential for extraction

**Examples**:

1. **Ways to make change for 5 rupees using 1,2 rupee coins**:
    - GF: $(1+x+x^2+\cdots)(1+x^2+x^4+\cdots) = \frac{1}{(1-x)(1-x^2)}$
    - $= \frac{1}{(1-x)^2(1+x)}$
    - Partial fractions: $\frac{A}{1-x} + \frac{B}{(1-x)^2} + \frac{C}{1+x}$
    - Coefficient of $x^5$: 3 ways (5×1, 3×1+1×2, 1×1+2×2)
2. **Number of binary strings of length n with no consecutive 1s**:
    - Let $a_n$ be count
    - Recurrence: $a_n = a_{n-1} + a_{n-2}$ (end in 0 or end in 01)
    - $a_0=1, a_1=2$
    - GF: $G(x) = \frac{1+x}{1-x-x^2}$ (Fibonacci-like)
3. **Partition of 5**:
    - $[x^5]\prod_{i=1}^{5} \frac{1}{1-x^i} = [x^5]\frac{1}{(1-x)(1-x^2)(1-x^3)(1-x^4)(1-x^5)}$
    - Computing: 7 partitions (5, 4+1, 3+2, 3+1+1, 2+2+1, 2+1+1+1, 1+1+1+1+1)

### 1.5 Modular Arithmetic (2) {#15-modular-arithmetic-2}

**Key Concepts**: Modular arithmetic is arithmetic "with wraparound" at a modulus. Foundation for number theory, cryptography, hashing, and algorithm design.

**Congruence Relation**:

**Definition**: $a \equiv b \pmod{m}$ if m divides (a-b)

- Notation: $m | (a-b)$ or $a-b = km$ for some integer k
- Equivalently: a and b have the same remainder when divided by m
- $a \bmod m$ denotes the remainder: unique r where $0 \leq r < m$ and $a \equiv r \pmod{m}$

**Properties** (Congruence is an equivalence relation):

1. **Reflexive**: $a \equiv a \pmod{m}$
2. **Symmetric**: If $a \equiv b \pmod{m}$, then $b \equiv a \pmod{m}$
3. **Transitive**: If $a \equiv b \pmod{m}$ and $b \equiv c \pmod{m}$, then $a \equiv c \pmod{m}$

**Arithmetic Operations** (Compatible with congruence):

If $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, then:

1. **Addition**: $a+c \equiv b+d \pmod{m}$
2. **Subtraction**: $a-c \equiv b-d \pmod{m}$
3. **Multiplication**: $ac \equiv bd \pmod{m}$
4. **Exponentiation**: $a^k \equiv b^k \pmod{m}$ for $k \geq 0$

**Division** (Careful!):

- $ac \equiv bc \pmod{m}$ does NOT imply $a \equiv b \pmod{m}$ in general
- **Cancellation law**: If $ac \equiv bc \pmod{m}$ and $\gcd(c,m)=1$, then $a \equiv b \pmod{m}$
- **Proof**: $m | c(a-b)$. Since $\gcd(c,m)=1$, by Euclid's lemma, $m | (a-b)$

**Modular Inverse**:

**Definition**: $a^{-1} \pmod{m}$ is value x where $ax \equiv 1 \pmod{m}$

**Existence**: $a^{-1}$ exists mod m ⟺ $\gcd(a,m) = 1$ (a and m are coprime)

**Finding inverse** - Extended Euclidean Algorithm:

- Given $\gcd(a,m) = 1$, extended Euclid finds integers x, y where $ax + my = 1$
- Taking mod m: $ax \equiv 1 \pmod{m}$, so $x = a^{-1}$
- Time complexity: $O(\log \min(a,m))$

**Example**: Find $3^{-1} \pmod{7}$

- Extended Euclid on (7,3):
    - $7 = 2(3) + 1$
    - $1 = 7 - 2(3)$
    - So $1 \cdot 7 + (-2) \cdot 3 = 1$
    - Thus $(-2) \cdot 3 \equiv 1 \pmod{7}$
    - $-2 \equiv 5 \pmod{7}$
    - Answer: $3^{-1} \equiv 5 \pmod{7}$
- Verification: $3 \cdot 5 = 15 = 2 \cdot 7 + 1 \equiv 1 \pmod{7}$ ✓

**Linear Congruences**:

**Problem**: Solve $ax \equiv b \pmod{m}$

**Solution**:

- Let $d = \gcd(a,m)$
- **If** $d \nmid b$: No solution
- **If** $d | b$: $d$ solutions exist
    - Divide through by d: $(a/d)x \equiv (b/d) \pmod{m/d}$
    - Now $\gcd(a/d, m/d) = 1$, so inverse exists
    - $x \equiv (b/d) \cdot (a/d)^{-1} \pmod{m/d}$
    - All solutions: $x \equiv x_0 + k(m/d)$ for $k = 0,1,\ldots,d-1$

**Chinese Remainder Theorem (CRT)**:

**Problem**: Solve system of congruences

$x \equiv a_1 \pmod{m_1}$

$x \equiv a_2 \pmod{m_2}$

$\vdots$

$x \equiv a_k \pmod{m_k}$

where $m_i$ are pairwise coprime: $\gcd(m_i, m_j) = 1$ for $i \neq j$

**Theorem**: Unique solution modulo $M = m_1 m_2 \cdots m_k$

**Construction**:

1. Let $M_i = M/m_i$ (product of all except $m_i$)
2. Find $y_i = M_i^{-1} \pmod{m_i}$ (inverse exists since $\gcd(M_i, m_i) = 1$)
3. Solution: $x \equiv \sum_{i=1}^{k} a_i M_i y_i \pmod{M}$

**Proof idea**: $M_i$ is divisible by all $m_j$ except $m_i$, so $M_i y_i \equiv 0 \pmod{m_j}$ for $j \neq i$ and $M_i y_i \equiv 1 \pmod{m_i}$

**Euler's Totient Function** $\phi(n)$:

**Definition**: $\phi(n)$ = count of integers in $\{1,2,\ldots,n\}$ coprime to n

**Values**:

- $\phi(1) = 1$
- $\phi(p) = p-1$ for prime p
- $\phi(p^k) = p^k - p^{k-1} = p^{k-1}(p-1)$ (exclude multiples of p)
- **Multiplicative**: If $\gcd(m,n)=1$, then $\phi(mn) = \phi(m)\phi(n)$

**Formula**: For $n = p_1^{a_1} p_2^{a_2} \cdots p_k^{a_k}$:

$\phi(n) = n \prod_{i=1}^{k} \left(1 - \frac{1}{p_i}\right) = n \prod_{p|n} \left(1 - \frac{1}{p}\right)$

**Derivation**: By inclusion-exclusion on prime divisors (see section 1.3)

**Properties**:

1. $\sum_{d|n} \phi(d) = n$ (sum over divisors)
2. For n>2, $\phi(n)$ is even

**Euler's Theorem**:

**Theorem**: If $\gcd(a,n) = 1$, then $a^{\phi(n)} \equiv 1 \pmod{n}$

**Proof** (Group theory):

- Consider multiplicative group $(\mathbb{Z}/n\mathbb{Z})^*$ of elements coprime to n
- This group has order $\phi(n)$
- By Lagrange's theorem, order of any element divides group order
- So $a^{\phi(n)} \equiv 1 \pmod{n}$

**Consequence - Fast modular exponentiation**:

- To compute $a^k \bmod n$ where k is large:
- Reduce exponent: $a^k = a^{k \bmod \phi(n) + q\phi(n)} = (a^{\phi(n)})^q \cdot a^{k \bmod \phi(n)} \equiv a^{k \bmod \phi(n)} \pmod{n}$

**Fermat's Little Theorem** (Special case of Euler's):

**Theorem**: If p is prime and $\gcd(a,p) = 1$, then:

$a^{p-1} \equiv 1 \pmod{p}$

Equivalently (for any a): $a^p \equiv a \pmod{p}$

**Proof 1** (Euler's theorem): $\phi(p) = p-1$ for prime p

**Proof 2** (Combinatorial):

- Consider necklaces with p beads, each colored one of a colors
- Total: $a^p$ necklaces
- Fixed under rotation: Only monochrome necklaces (a of them)
- Necklaces not fixed form orbits of size p under rotation
- So $a^p \equiv a \pmod{p}$

**Proof 3** (Elementary):

- Consider $a, 2a, 3a, \ldots, (p-1)a$ modulo p
- All distinct mod p (since $\gcd(a,p)=1$)
- So they're a permutation of $1,2,3,\ldots,p-1$
- Product: $a \cdot 2a \cdot 3a \cdots (p-1)a \equiv 1 \cdot 2 \cdot 3 \cdots (p-1) \pmod{p}$
- $a^{p-1} (p-1)! \equiv (p-1)! \pmod{p}$
- Cancel $(p-1)!$: $a^{p-1} \equiv 1 \pmod{p}$

**Applications**:

**1. Primality testing** (Fermat test):

- If $a^{n-1} \not\equiv 1 \pmod{n}$ for some a, then n is composite
- Converse not always true (Carmichael numbers!)

**2. Computing inverses mod prime**:

- $a^{-1} \equiv a^{p-2} \pmod{p}$ (from $a \cdot a^{p-2} = a^{p-1} \equiv 1$)

**3. Computing large powers**:

- $2^{100} \bmod 7$: Since $\phi(7)=6$, $2^{100} = 2^{16 \cdot 6 + 4} \equiv 2^4 = 16 \equiv 2 \pmod{7}$

**4. RSA Cryptography**:

- Choose primes p, q; let $n=pq$, $\phi(n)=(p-1)(q-1)$
- Public key: (n, e) where $\gcd(e, \phi(n))=1$
- Private key: d where $ed \equiv 1 \pmod{\phi(n)}$
- Encrypt: $c = m^e \bmod n$
- Decrypt: $m = c^d \bmod n$
- Correctness: $c^d = (m^e)^d = m^{ed} = m^{1+k\phi(n)} = m \cdot (m^{\phi(n)})^k \equiv m \pmod{n}$

**Problem-Solving Tips**:

- Fast exponentiation: Use repeated squaring $O(\log k)$ multiplications
- For modular inverse: Extended Euclid or (for prime p) use $a^{-1} \equiv a^{p-2}$
- Reduce exponents using $\phi(n)$
- CRT for systems with coprime moduli
- GATE: Often test Fermat, totient computation, inverse finding

**Examples**:

1. **Compute** $7^{222} \bmod 10$:
    - $\phi(10) = \phi(2)\phi(5) = 1 \cdot 4 = 4$
    - $\gcd(7,10)=1$, so $7^4 \equiv 1 \pmod{10}$
    - $222 = 55 \cdot 4 + 2$
    - $7^{222} = (7^4)^{55} \cdot 7^2 \equiv 1^{55} \cdot 49 \equiv 9 \pmod{10}$
2. **Solve** $3x \equiv 7 \pmod{11}$:
    - Find $3^{-1} \bmod 11$
    - Method 1: $3^{-1} \equiv 3^{11-2} = 3^9 \bmod 11$
        - $3^2=9, 3^4=81\equiv4, 3^8\equiv16\equiv5, 3^9\equiv15\equiv4 \pmod{11}$
    - Method 2: Extended Euclid gives $4 \cdot 3 - 1 \cdot 11 = 1$, so $3^{-1} \equiv 4$
    - Solution: $x \equiv 7 \cdot 4 = 28 \equiv 6 \pmod{11}$
3. **CRT example**: Solve $x \equiv 2 \pmod{3}, x \equiv 3 \pmod{5}, x \equiv 2 \pmod{7}$
    - $M = 3 \cdot 5 \cdot 7 = 105$
    - $M_1=35, M_2=21, M_3=15$
    - $35 \equiv 2 \pmod{3}$, so $y_1 = 2^{-1} \equiv 2 \pmod{3}$
    - $21 \equiv 1 \pmod{5}$, so $y_2 = 1$
    - $15 \equiv 1 \pmod{7}$, so $y_3 = 1$
    - $x \equiv 2(35)(2) + 3(21)(1) + 2(15)(1) = 140 + 63 + 30 = 233 \equiv 23 \pmod{105}$

### 1.6 Pigeonhole Principle (2) {#16-pigeonhole-principle-2}

**Key Concepts**: One of the most fundamental principles in combinatorics. Despite its simplicity, it yields powerful existence proofs. The principle guarantees existence without construction.

**Basic Pigeonhole Principle** (Dirichlet's Box Principle):

**Statement**: If n objects are placed into m containers (pigeonholes) and $n > m$, then at least one container must contain more than one object.

**Formal**: If $n > m$, then there exists a pigeonhole with at least $\lceil n/m \rceil$ pigeons.

**Proof** (by contradiction):

- Assume each pigeonhole contains at most 1 pigeon
- Then total pigeons ≤ m × 1 = m
- But we have n > m pigeons - contradiction!
- Therefore, at least one pigeonhole must contain ≥ 2 pigeons

**Generalized Pigeonhole Principle**:

**Statement**: If n objects are placed into m pigeonholes, then:

- At least one pigeonhole contains at least $\lceil n/m \rceil$ objects
- At least one pigeonhole contains at most $\lfloor n/m \rfloor$ objects

**Proof**:

- Suppose all pigeonholes contain < $\lceil n/m \rceil$ objects
- Then each contains ≤ $\lceil n/m \rceil - 1 = \lfloor n/m \rfloor$ objects
- Total: ≤ $m \cdot \lfloor n/m \rfloor < m \cdot (n/m) = n$ - contradiction!

**Strong Form**: If $n > km$, then at least one pigeonhole contains at least $k+1$ objects.

**Proof**: If all pigeonholes had ≤ k objects, total would be ≤ km < n - contradiction.

**Applications and Classic Problems**:

**1. Sock Drawer Problem**:

- 10 pairs of socks (20 socks total) in a dark drawer
- How many socks must you pull out to guarantee a matching pair?
- Answer: 11 (10 colors + 1)
- Pigeons: socks pulled out
- Pigeonholes: colors (10)
- By PHP: If pulling 11 socks, at least one color appears twice

**2. Birthday Problem** (Existence version):

- In any group of 367 people, at least two share a birthday
- Pigeons: 367 people
- Pigeonholes: 366 possible birthdays (including Feb 29)
- 367 > 366 → PHP applies

**3. Subset Sum Problem**:

- Given any n+1 integers from $\{1, 2, \ldots, 2n\}$, there exist two whose sum is $2n+1$
- Proof: Pair integers: $(1, 2n), (2, 2n-1), \ldots, (n, n+1)$
- n pairs (pigeonholes), n+1 integers (pigeons)
- Two integers from same pair sum to $2n+1$

**4. Ramsey Theory** (R(3,3) = 6):

- In any group of 6 people, there exist 3 mutual friends OR 3 mutual strangers
- Model as graph coloring problem
- Consider person A: They know or don't know each of 5 others
- By PHP: At least 3 relationships of same type (say, knows B, C, D)
- If any of B,C,D know each other → 3 mutual friends
- If none of B,C,D know each other → 3 mutual strangers

**5. Decimal Expansion**:

- Every rational number has eventually repeating decimal expansion
- When dividing, remainders are from $\{0, 1, \ldots, d-1\}$ (d pigeonholes)
- After d+1 divisions (pigeons), by PHP, a remainder repeats
- This forces cycle in decimal expansion

**6. Sequence Problem**:

- Among any n+1 positive integers ≤ 2n, there exist two where one divides the other
- Proof: Write each as $2^k \cdot m$ where m is odd
- Only n odd numbers ≤ 2n
- By PHP on n+1 integers: Two have same odd part m
- Say $2^{k_1}m$ and $2^{k_2}m$ - one divides the other

**Average Argument** (Probabilistic PHP):

**Principle**: If the average value is x, then:

- At least one value is ≥ x
- At least one value is ≤ x

**Example**: In a graph with n vertices and e edges, there exists:

- A vertex with degree ≥ $2e/n$ (average degree)
- A vertex with degree ≤ $2e/n$

**Infinite Pigeonhole Principle**:

**Statement**: If infinitely many objects are placed in finitely many pigeonholes, at least one pigeonhole contains infinitely many objects.

**Application - Bolzano-Weierstrass**: Every bounded infinite sequence has a convergent subsequence.

**Erdős-Szekeres Theorem** (Monotonic Subsequences):

**Theorem**: Any sequence of $n^2 + 1$ distinct real numbers contains either:

- An increasing subsequence of length n+1, OR
- A decreasing subsequence of length n+1

**Proof** (via PHP):

- Assign each element $a_i$ a pair $(L_i, D_i)$:
    - $L_i$ = length of longest increasing subsequence ending at $a_i$
    - $D_i$ = length of longest decreasing subsequence ending at $a_i$
- If all pairs have $L_i, D_i \leq n$, there are at most $n^2$ possible pairs
- With $n^2 + 1$ elements (pigeons) and $n^2$ pairs (pigeonholes)
- By PHP: Two elements $a_i, a_j$ have same pair
- If $i < j$ and $a_i < a_j$: Can extend increasing subseq - contradiction
- If $i < j$ and $a_i > a_j$: Can extend decreasing subseq - contradiction
- Therefore, assumption fails: some $L_i$ or $D_i$ exceeds n

**Problem-Solving Strategy**:

1. **Identify pigeons**: Objects to be distributed
2. **Identify pigeonholes**: Categories/containers
3. **Count carefully**: Ensure n > m (or n > km for strong form)
4. **Extract conclusion**: "At least one pigeonhole contains..."
5. **For impossibility**: Show any distribution violates PHP

**GATE Tips**:

- PHP proves existence, not construction
- Often combined with other principles (extremal principle, induction)
- Watch for "at least" vs "at most" conclusions
- Average argument useful for graph theory
- Strong form: To guarantee k+1 items in one hole, need km+1 total items

**Examples**:

1. **13 pigeons, 12 holes**: At least one hole has ≥ $\lceil 13/12 \rceil = 2$ pigeons
2. **Prove**: Among any 5 integers, two differ by a multiple of 4
    - Remainders mod 4: {0,1,2,3} (4 pigeonholes)
    - 5 integers (pigeons)
    - By PHP: Two have same remainder mod 4
    - Their difference is divisible by 4
3. **Social network**: In any group of n people, at least two have the same number of friends within the group
    - Possible friend counts: 0, 1, 2, ..., n-1
    - But 0 and n-1 can't coexist (if someone has 0 friends, no one has n-1)
    - So at most n-1 possible values (pigeonholes)
    - n people (pigeons)
    - By PHP: Two people have same friend count
4. **Geometric**: Place 5 points inside a unit square. Prove two points are within distance $\frac{\sqrt{2}}{2}$
    - Divide square into 4 equal subsquares (side = 1/2)
    - 5 points (pigeons), 4 subsquares (pigeonholes)
    - By PHP: One subsquare contains ≥2 points
    - Max distance in subsquare: diagonal = $\frac{\sqrt{2}}{2}$

### 1.7 Recurrence Relation (7) {#17-recurrence-relation-7}

**Key Concepts**: A recurrence relation defines a sequence recursively - each term as a function of previous terms. Essential for analyzing algorithms and counting problems.

**Definition**: A recurrence relation for sequence $\{a_n\}$ expresses $a_n$ in terms of previous terms $a_0, a_1, \ldots, a_{n-1}$, along with initial conditions.

**Types of Recurrence Relations**:

**1. Linear vs Nonlinear**:

- **Linear**: Each term appears to first power: $a_n = c_1 a_{n-1} + c_2 a_{n-2} + \cdots$
- **Nonlinear**: Products, powers of terms: $a_n = a_{n-1}^2$, $a_n = a_{n-1} \cdot a_{n-2}$

**2. Homogeneous vs Non-homogeneous**:

- **Homogeneous**: RHS only contains previous terms: $a_n = 2a_{n-1} + 3a_{n-2}$
- **Non-homogeneous**: RHS has additional function: $a_n = 2a_{n-1} + n$

**3. Order**: Highest index difference

- $a_n = a_{n-1} + a_{n-2}$ is 2nd order
- $a_n = a_{n-1} + a_{n-3}$ is 3rd order

**Linear Homogeneous Recurrence Relations (LHRR)**:

**General Form**: $a_n = c_1 a_{n-1} + c_2 a_{n-2} + \cdots + c_k a_{n-k}$

**Solution Method - Characteristic Equation**:

**Step 1**: Assume solution of form $a_n = r^n$

**Step 2**: Substitute into recurrence:

$r^n = c_1 r^{n-1} + c_2 r^{n-2} + \cdots + c_k r^{n-k}$

Divide by $r^{n-k}$:

$r^k = c_1 r^{k-1} + c_2 r^{k-2} + \cdots + c_k$

**Step 3**: Rearrange to **characteristic equation**:

$r^k - c_1 r^{k-1} - c_2 r^{k-2} - \cdots - c_k = 0$

**Step 4**: Find roots $r_1, r_2, \ldots, r_k$

**Step 5**: Construct general solution based on root types:

**Case 1: Distinct Real Roots** $r_1, r_2, \ldots, r_k$ all different:

$a_n = A_1 r_1^n + A_2 r_2^n + \cdots + A_k r_k^n$

**Case 2: Repeated Roots** - Root $r$ with multiplicity m:

$a_n = (A_1 + A_2 n + A_3 n^2 + \cdots + A_m n^{m-1}) r^n$

**Case 3: Complex Roots** $r = \rho e^{i\theta} = \rho(\cos\theta + i\sin\theta)$:

$a_n = \rho^n (A\cos(n\theta) + B\sin(n\theta))$

**Step 6**: Use initial conditions to find constants $A_1, A_2, \ldots$

**Classic Examples**:

**Fibonacci Sequence**: $F_n = F_{n-1} + F_{n-2}$, $F_0=0, F_1=1$

**Solution**:

1. Characteristic equation: $r^2 = r + 1$ → $r^2 - r - 1 = 0$
2. Roots (quadratic formula): $r = \frac{1 \pm \sqrt{5}}{2}$
    - $\phi = \frac{1+\sqrt{5}}{2} \approx 1.618$ (golden ratio)
    - $\psi = \frac{1-\sqrt{5}}{2} \approx -0.618$
3. General solution: $F_n = A\phi^n + B\psi^n$
4. Initial conditions:
    - $F_0 = 0: A + B = 0$ → $B = -A$
    - $F_1 = 1: A\phi + B\psi = 1$
    - Solving: $A = \frac{1}{\sqrt{5}}, B = -\frac{1}{\sqrt{5}}$
5. **Binet's Formula**: $F_n = \frac{\phi^n - \psi^n}{\sqrt{5}}$

**Properties**:

- Since $|\psi| < 1$, $\psi^n \to 0$
- $F_n \approx \frac{\phi^n}{\sqrt{5}}$ (nearest integer)
- $\lim_{n\to\infty} \frac{F_{n+1}}{F_n} = \phi$

**Tower of Hanoi**: $T_n = 2T_{n-1} + 1$, $T_1 = 1$

**Homogeneous part**: $T_n^{(h)} = 2T_{n-1}$ → $r = 2$ → $T_n^{(h)} = A \cdot 2^n$

**Particular solution**: Try constant $T_n^{(p)} = c$

- $c = 2c + 1$ → $c = -1$

**General**: $T_n = A \cdot 2^n - 1$

**Initial condition**: $T_1 = 1$ → $2A - 1 = 1$ → $A = 1$

**Solution**: $T_n = 2^n - 1$

**Non-homogeneous Linear Recurrences**:

**Form**: $a_n = c_1 a_{n-1} + \cdots + c_k a_{n-k} + f(n)$

**Solution**: $a_n = a_n^{(h)} + a_n^{(p)}$

- $a_n^{(h)}$: Homogeneous solution (solve characteristic equation)
- $a_n^{(p)}$: Particular solution (guess based on $f(n)$)

**Particular Solution Guesses**:

- $f(n) = \text{polynomial of degree d}$ → Try polynomial of degree d
- $f(n) = \alpha^n$ → Try $c \cdot \alpha^n$ (unless $\alpha$ is root of char. eq.)
- $f(n) = \alpha^n \cdot p(n)$ → Try $\alpha^n \cdot q(n)$ where deg($q$) = deg($p$)

**If guess form matches homogeneous solution**: Multiply by $n^m$ where m is multiplicity

**Divide and Conquer Recurrences**:

Form: $T(n) = aT(n/b) + f(n)$

- a: number of subproblems
- n/b: size of each subproblem
- f(n): work outside recursive calls

**Master Theorem**: For $T(n) = aT(n/b) + f(n)$ where $a \geq 1, b > 1$:

Let $c_{crit} = \log_b a$

**Case 1**: If $f(n) = O(n^c)$ for $c < c_{crit}$:

- $T(n) = \Theta(n^{c_{crit}})$
- Tree-depth dominates

**Case 2**: If $f(n) = \Theta(n^{c_{crit}} \log^k n)$:

- $T(n) = \Theta(n^{c_{crit}} \log^{k+1} n)$
- All levels contribute equally

**Case 3**: If $f(n) = \Omega(n^c)$ for $c > c_{crit}$ AND regularity condition:

- $T(n) = \Theta(f(n))$
- Root dominates

**Examples**:

1. **Merge Sort**: $T(n) = 2T(n/2) + n$
    - $a=2, b=2, f(n)=n$
    - $c_{crit} = \log_2 2 = 1$
    - $f(n) = \Theta(n^1)$ → Case 2 with k=0
    - $T(n) = \Theta(n \log n)$
2. **Binary Search**: $T(n) = T(n/2) + O(1)$
    - $a=1, b=2, f(n)=1$
    - $c_{crit} = 0$
    - Case 2: $T(n) = \Theta(\log n)$
3. **Karatsuba Multiplication**: $T(n) = 3T(n/2) + O(n)$
    - $c_{crit} = \log_2 3 \approx 1.585$
    - $f(n) = O(n^1)$, $1 < 1.585$
    - Case 1: $T(n) = \Theta(n^{1.585})$

**Generating Function Method** (see section 1.4):

Define $G(x) = \sum_{n=0}^{\infty} a_n x^n$, manipulate recurrence algebraically

**Substitution/Iteration Method**:

Expand recurrence repeatedly:

- $a_n = f(a_{n-1}) = f(f(a_{n-2})) = \cdots$
- Look for pattern
- Prove by induction

**GATE Tips**:

- Identify recurrence type (linear homogeneous, etc.)
- For LHRR: Characteristic equation is key
- Master theorem: Compare $f(n)$ with $n^{\log_b a}$
- Common mistake: Forgetting initial conditions for constants
- Fibonacci appears frequently - memorize Binet's formula

**Examples**:

1. Solve $a_n = 2a_{n-1}, a_0 = 1$:
    - Char. eq: $r = 2$
    - Solution: $a_n = A \cdot 2^n$
    - $a_0 = 1: A = 1$
    - $a_n = 2^n$
2. Solve $a_n = 6a_{n-1} - 9a_{n-2}, a_0=1, a_1=3$:
    - Char. eq: $r^2 - 6r + 9 = 0$ → $(r-3)^2 = 0$
    - Repeated root $r=3$ (multiplicity 2)
    - $a_n = (A + Bn) \cdot 3^n$
    - $a_0=1: A=1$
    - $a_1=3: 3(1+B)=3$ → $B=0$
    - $a_n = 3^n$
3. Catalan numbers: $C_n = \sum_{i=0}^{n-1} C_i C_{n-1-i}, C_0=1$:
    - Generating function technique gives: $C_n = \frac{1}{n+1}\binom{2n}{n}$

### 1.8 Summation (3) {#18-summation-3}

**Key Concepts**: Finding closed-form expressions for sums. Essential for algorithm analysis, probability calculations, and mathematical proofs.

**Fundamental Summation Formulas**:

**1. Sum of First n Natural Numbers**:

$\sum_{k=1}^{n} k = 1 + 2 + 3 + \cdots + n = \frac{n(n+1)}{2}$

**Derivation** (Gauss method):

- Write sum forward: $S = 1 + 2 + 3 + \cdots + n$
- Write sum backward: $S = n + (n-1) + (n-2) + \cdots + 1$
- Add vertically: $2S = (n+1) + (n+1) + \cdots + (n+1)$ (n times)
- $2S = n(n+1)$
- $S = \frac{n(n+1)}{2}$

**Alternative derivation** (Visual/combinatorial):

- Counting pairs: Choose 2 from n+1 elements including 0
- Total arrangements in triangle pattern

**2. Sum of First n Squares**:

$\sum_{k=1}^{n} k^2 = 1^2 + 2^2 + 3^2 + \cdots + n^2 = \frac{n(n+1)(2n+1)}{6}$

**Derivation** (Using telescoping):

- Consider $(k+1)^3 - k^3 = 3k^2 + 3k + 1$
- Sum from k=1 to n:
    
    $\sum_{k=1}^{n} [(k+1)^3 - k^3] = \sum_{k=1}^{n} (3k^2 + 3k + 1)$
    
- LHS telescopes: $(n+1)^3 - 1^3 = n^3 + 3n^2 + 3n$
- RHS: $3\sum k^2 + 3\sum k + n$
- $n^3 + 3n^2 + 3n = 3\sum k^2 + 3\cdot\frac{n(n+1)}{2} + n$
- Solve for $\sum k^2$:
    
    $\sum k^2 = \frac{n^3 + 3n^2 + 3n - \frac{3n(n+1)}{2} - n}{3} = \frac{n(n+1)(2n+1)}{6}$
    

**3. Sum of First n Cubes**:

$\sum_{k=1}^{n} k^3 = 1^3 + 2^3 + 3^3 + \cdots + n^3 = \left[\frac{n(n+1)}{2}\right]^2$

**Remarkable property**: Sum of cubes = Square of sum!

$\sum_{k=1}^{n} k^3 = \left(\sum_{k=1}^{n} k\right)^2$

**Proof** (Induction):

- Base: n=1: $1^3 = 1^2$ ✓
- Assume true for n: $\sum_{k=1}^{n} k^3 = \left[\frac{n(n+1)}{2}\right]^2$
- Prove for n+1:
    
    $\sum_{k=1}^{n+1} k^3 = \left[\frac{n(n+1)}{2}\right]^2 + (n+1)^3$
    
    $= \frac{n^2(n+1)^2 + 4(n+1)^3}{4} = \frac{(n+1)^2[n^2 + 4(n+1)]}{4}$
    
    $= \frac{(n+1)^2(n+2)^2}{4} = \left[\frac{(n+1)(n+2)}{2}\right]^2$ ✓
    

**4. Geometric Series**:

$\sum_{k=0}^{n} r^k = 1 + r + r^2 + \cdots + r^n = \begin{cases} \frac{r^{n+1}-1}{r-1} & \text{if } r \neq 1 \\ n+1 & \text{if } r = 1 \end{cases}$

**Derivation**:

- Let $S = 1 + r + r^2 + \cdots + r^n$
- Multiply by r: $rS = r + r^2 + r^3 + \cdots + r^{n+1}$
- Subtract: $S - rS = 1 - r^{n+1}$
- $S(1-r) = 1 - r^{n+1}$
- $S = \frac{1-r^{n+1}}{1-r} = \frac{r^{n+1}-1}{r-1}$ (multiply by -1/-1)

**Infinite geometric series** ($|r| < 1$):

$\sum_{k=0}^{\infty} r^k = \frac{1}{1-r}$ (as $r^{n+1} \to 0$)

**5. Arithmetic-Geometric Series**:

$\sum_{k=0}^{n} k \cdot r^k = 0 + r + 2r^2 + 3r^3 + \cdots + nr^n = \frac{r(1 - (n+1)r^n + nr^{n+1})}{(1-r)^2}$

**Derivation** (Differentiation trick):

- Start with $\sum_{k=0}^{n} r^k = \frac{1-r^{n+1}}{1-r}$
- Differentiate both sides with respect to r
- Apply product and chain rules

**6. Harmonic Series**:

$H_n = \sum_{k=1}^{n} \frac{1}{k} = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n}$

**No closed form**, but approximation:

$H_n \approx \ln(n) + \gamma$ where $\gamma \approx 0.5772$ (Euler-Mascheroni constant)

**Growth**: $H_n = \Theta(\log n)$

**7. Power Sums (General)**:

$\sum_{k=1}^{n} k^p$ can be expressed as polynomial of degree p+1 in n

**Faulhaber's Formulas**: Use Bernoulli numbers

- For p=0: $\sum 1 = n$
- For p=1: $\sum k = \frac{n^2}{2} + \frac{n}{2}$
- For p=2: $\sum k^2 = \frac{n^3}{3} + \frac{n^2}{2} + \frac{n}{6}$
- For p=3: $\sum k^3 = \frac{n^4}{4} + \frac{n^3}{2} + \frac{n^2}{4}$

**Summation Techniques**:

**1. Telescoping Series**:

- Series where consecutive terms cancel
- $\sum_{k=1}^{n} [f(k+1) - f(k)] = f(n+1) - f(1)$

**Example**: $\sum_{k=1}^{n} \frac{1}{k(k+1)}$

- Partial fractions: $\frac{1}{k(k+1)} = \frac{1}{k} - \frac{1}{k+1}$
- Sum: $\left(\frac{1}{1} - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \cdots + \left(\frac{1}{n} - \frac{1}{n+1}\right)$
- Most terms cancel: $1 - \frac{1}{n+1} = \frac{n}{n+1}$

**2. Perturbation Method**:

- Compare S with rS (for geometric-like series)
- Used in geometric series derivation

**3. Differentiation/Integration**:

- For $\sum k \cdot r^k$, differentiate $\sum r^k$
- For $\sum \frac{r^k}{k}$, integrate $\sum r^{k-1}$

**4. Generating Functions** (see section 1.4):

- Encode sum as power series
- Manipulate algebraically
- Extract coefficient

**5. Mathematical Induction**:

- Base case: Verify for n=1
- Inductive step: Assume for n, prove for n+1
- Essential for proving formulas

**Double Summations**:

**Order exchange** (Fubini's theorem for finite sums):

$\sum_{i=1}^{m} \sum_{j=1}^{n} a_{ij} = \sum_{j=1}^{n} \sum_{i=1}^{m} a_{ij}$

**Triangular summation**:

$\sum_{1 \leq i < j \leq n} a_{ij}$ (sum over pairs)

**Example**: $\sum_{i=1}^{n} \sum_{j=1}^{i} j = \sum_{i=1}^{n} \frac{i(i+1)}{2} = \frac{1}{2}\sum_{i=1}^{n} (i^2 + i)$

$= \frac{1}{2}\left[\frac{n(n+1)(2n+1)}{6} + \frac{n(n+1)}{2}\right] = \frac{n(n+1)(n+2)}{6}$

**Binomial Sum Identities**:

1. $\sum_{k=0}^{n} \binom{n}{k} = 2^n$ (sum of binomial coefficients)
    - Proof: Expand $(1+1)^n$
2. $\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0$ (alternating sum)
    - Proof: Expand $(1-1)^n = 0$ for n≥1
3. $\sum_{k=0}^{n} k \binom{n}{k} = n \cdot 2^{n-1}$
    - Proof: Differentiate $(1+x)^n$, set x=1
4. $\sum_{k=0}^{n} \binom{n}{k}^2 = \binom{2n}{n}$ (Vandermonde's identity)

**Problem-Solving Strategy**:

1. Check if it's a standard formula (arithmetic, geometric, powers)
2. Try telescoping (partial fractions for rational terms)
3. For products with powers, try perturbation method
4. For complex sums, try generating functions
5. Verify with induction after finding pattern

**GATE Tips**:

- Memorize formulas for $\sum k, \sum k^2, \sum k^3$, geometric series
- Sum of first n odd numbers: $1+3+5+\cdots+(2n-1) = n^2$
- Sum of first n even numbers: $2+4+6+\cdots+2n = n(n+1)$
- Telescoping: Look for differences
- Geometric series: Check common ratio
- Double sums: Try changing order or substitution
- For algorithm analysis: Often need $\sum k$ or geometric sums

**Common Patterns**:

- $\sum_{k=1}^{n} (2k-1) = n^2$ (odd numbers)
- $\sum_{k=1}^{n} k^2 - (k-1)^2 = n^2$ (telescoping)
- $\sum_{k=0}^{n} k \cdot 2^k = (n-1)2^{n+1} + 2$ (arithmetic-geometric)

**Examples**:

1. **Find** $\sum_{k=1}^{100} (3k-1)$:
    - $3\sum k - \sum 1 = 3 \cdot \frac{100 \cdot 101}{2} - 100 = 15150 - 100 = 15050$
2. **Compute** $\sum_{k=1}^{n} k(k+1)$:
    - $\sum (k^2 + k) = \sum k^2 + \sum k = \frac{n(n+1)(2n+1)}{6} + \frac{n(n+1)}{2}$
    - $= \frac{n(n+1)}{6}[2n+1+3] = \frac{n(n+1)(2n+4)}{6} = \frac{n(n+1)(n+2)}{3}$
3. **Evaluate** $\sum_{k=1}^{\infty} \frac{1}{2^k}$:
    - Geometric with r=1/2: $\sum_{k=1}^{\infty} \left(\frac{1}{2}\right)^k = \frac{1/2}{1-1/2} = 1$
4. **Prove**: $1^3 + 2^3 + \cdots + n^3 = (1+2+\cdots+n)^2$:
    - LHS: $\sum k^3 = \left[\frac{n(n+1)}{2}\right]^2$
    - RHS: $\left(\sum k\right)^2 = \left[\frac{n(n+1)}{2}\right]^2$
    - Equal! ✓

### 2. Discrete Mathematics: Graph Theory (83)

### 2.1 Counting (3) {#21-counting-3}

**Key Concepts**: Enumeration problems in graph theory - counting specific graph structures and properties.

**Trees**:

- **Definition**: Connected acyclic graph
- **Properties**:
    - n vertices → exactly n-1 edges
    - Any two vertices connected by unique path
    - Adding any edge creates exactly one cycle
    - Removing any edge disconnects the graph
    - Minimum edges for connectivity

**Cayley's Formula** (Labeled Trees):

Number of labeled trees on n vertices: $n^{n-2}$

**Proof Sketch** (Prüfer Sequence):

- Each labeled tree on n vertices corresponds to unique sequence of length n-2
- Each element in sequence is from {1,2,...,n}
- Total sequences: $n^{n-2}$
- Bijection establishes formula

**Examples**:

- n=2: $2^0 = 1$ tree
- n=3: $3^1 = 3$ trees
- n=4: $4^2 = 16$ trees

**Spanning Trees** (Kirchhoff's Matrix-Tree Theorem):

For connected graph G:

- Construct Laplacian matrix L = D - A
    - D = degree matrix (diagonal)
    - A = adjacency matrix
- Number of spanning trees = any cofactor of L
- Equivalently: Determinant of any (n-1)×(n-1) submatrix obtained by deleting one row and corresponding column

**Example** - $K_3$ (Complete graph on 3 vertices):

- Laplacian: $L = \begin{bmatrix} 2 & -1 & -1 \\ -1 & 2 & -1 \\ -1 & -1 & 2 \end{bmatrix}$
- Delete row 1, column 1: $\begin{bmatrix} 2 & -1 \\ -1 & 2 \end{bmatrix}$
- Determinant: $2(2) - (-1)(-1) = 4 - 1 = 3$
- Answer: 3 spanning trees

**Complete Graph** $K_n$:

Number of spanning trees in $K_n$: $n^{n-2}$ (Cayley's formula)

**Complete Bipartite Graph** $K_{m,n}$:

Number of spanning trees: $m^{n-1} \cdot n^{m-1}$

**Eulerian Paths and Circuits**:

**Eulerian Circuit**: Path that visits every edge exactly once and returns to start

- **Exists iff**: Graph is connected AND all vertices have even degree
- **Count**: No simple closed formula (computationally hard)

**Eulerian Path**: Path that visits every edge exactly once

- **Exists iff**: Graph is connected AND exactly 0 or 2 vertices have odd degree
- If 2 odd-degree vertices: Path starts at one, ends at other

**Hamiltonian Paths and Cycles**:

**Hamiltonian Cycle**: Path that visits every vertex exactly once and returns to start

- **No simple criterion** for existence (NP-complete)
- **Sufficient conditions**:
    - Dirac: If deg(v) ≥ n/2 for all v, then Hamiltonian
    - Ore: If deg(u) + deg(v) ≥ n for all non-adjacent u,v, then Hamiltonian

**Hamiltonian Path**: Path that visits every vertex exactly once

- Also NP-complete to determine existence

**Counting in Specific Graphs**:

**1. Perfect Matchings**:

- In $K_{2n}$: $(2n-1)!! = (2n-1)(2n-3)\cdots(3)(1)$
- Double factorial notation

**2. Chromatic Polynomial** $P(G,k)$:

- Number of proper k-colorings of G
- For tree on n vertices: $P(T,k) = k(k-1)^{n-1}$
- For $K_n$: $P(K_n, k) = k(k-1)(k-2)\cdots(k-n+1)$
- For cycle $C_n$: $P(C_n, k) = (k-1)^n + (-1)^n(k-1)$

**3. Number of Walks**:

- Number of walks of length k from vertex i to vertex j: $(A^k)_{ij}$
- A = adjacency matrix
- Total walks of length k: $\text{trace}(A^k)$

**Problem-Solving Strategy**:

1. For spanning trees: Use Kirchhoff's theorem (small graphs) or formulas (special graphs)
2. For Eulerian: Check degree parity
3. For Hamiltonian: Use sufficient conditions or exhaustive search
4. For labeled counting: Consider Cayley-type formulas

**GATE Tips**:

- Tree with n vertices has n-1 edges (memorize!)
- $K_n$ has $n^{n-2}$ spanning trees
- Eulerian circuit: All even degrees
- Hamiltonian: No simple test (but know Dirac/Ore conditions)
- Matrix-tree theorem useful for small graphs

**Examples**:

1. **How many spanning trees in** $K_4$**?**
    - By Cayley: $4^{4-2} = 4^2 = 16$
2. **Does** $C_5$ **have Eulerian circuit?**
    - All vertices have degree 2 (even) ✓
    - Connected ✓
    - Yes, Eulerian circuit exists
3. **Number of labeled trees on 5 vertices:**
    - $5^{5-2} = 5^3 = 125$
4. **Spanning trees in cycle** $C_n$**:**
    - Remove any one edge from cycle → spanning tree
    - Answer: n spanning trees

### 2.2 Degree of Graph (12) {#22-degree-of-graph-12}

**Key Concepts**: The degree of a vertex is the number of edges incident to it. Fundamental for characterizing graph properties and proving theorems.

**Degree Definitions**:

**For Undirected Graphs**:

- **Degree** deg(v): Number of edges incident to vertex v
- **Loop**: An edge from v to itself contributes 2 to deg(v)
- **Isolated vertex**: deg(v) = 0
- **Pendant/Leaf vertex**: deg(v) = 1

**For Directed Graphs**:

- **In-degree** deg⁻(v): Number of edges entering v
- **Out-degree** deg⁺(v): Number of edges leaving v
- **Total degree**: deg(v) = deg⁻(v) + deg⁺(v)

**Handshaking Lemma** (Fundamental Theorem):

**Statement**: In any undirected graph G = (V, E):

$\sum_{v \in V} \text{deg}(v) = 2|E|$

The sum of all vertex degrees equals twice the number of edges.

**Proof**:

- Each edge e = {u,v} contributes exactly 1 to deg(u) and 1 to deg(v)
- Therefore, each edge contributes exactly 2 to the total sum
- With |E| edges, total contribution = 2|E|
- QED

**Alternative proof** (Counting argument):

- Count pairs (v, e) where vertex v is incident to edge e
- From vertex perspective: Each vertex v contributes deg(v) such pairs
- Total: $\sum_{v} \text{deg}(v)$
- From edge perspective: Each edge contributes 2 such pairs (its two endpoints)
- Total: $2|E|$
- These count the same set, so they're equal

**Corollaries**:

**1. Number of Odd-Degree Vertices is Even**:

- Let O = vertices with odd degree, E = vertices with even degree
- $\sum_{v \in O} \text{deg}(v) + \sum_{v \in E} \text{deg}(v) = 2|E|$
- RHS is even
- Second sum is even (sum of even numbers)
- Therefore, first sum must be even
- Sum of |O| odd numbers is even ⟺ |O| is even
- **Conclusion**: In any graph, the number of odd-degree vertices is even

**2. Average Degree**:

$\bar{d} = \frac{1}{|V|} \sum_{v} \text{deg}(v) = \frac{2|E|}{|V|}$

**For Directed Graphs**:

$\sum_{v \in V} \text{deg}^+(v) = \sum_{v \in V} \text{deg}^-(v) = |E|$

Each edge contributes 1 to in-degree sum and 1 to out-degree sum.

**Degree Sequences**:

**Definition**: List of vertex degrees in non-increasing order

- Example: Graph with degrees 3,3,2,2,2,0 has degree sequence (3,3,2,2,2,0)

**Graphic Sequence**: A sequence that can be realized as the degree sequence of some simple graph

**Necessary Conditions** (for sequence to be graphic):

1. Sum must be even (by handshaking lemma)
2. Each element ≤ n-1 (max degree in simple graph on n vertices)
3. If sorted as d₁ ≥ d₂ ≥ ... ≥ dₙ, then d₁ ≤ n-1

**Erdős-Gallai Theorem**: Sequence (d₁, d₂, ..., dₙ) with d₁ ≥ d₂ ≥ ... ≥ dₙ is graphic iff:

1. $\sum_{i=1}^{n} d_i$ is even
2. For each k ∈ {1,...,n}:
    
    $\sum_{i=1}^{k} d_i \leq k(k-1) + \sum_{i=k+1}^{n} \min(d_i, k)$
    

**Havel-Hakimi Algorithm** (Constructive test):

Given sequence S = (d₁, d₂, ..., dₙ) sorted in non-increasing order:

1. Remove d₁ from sequence
2. Subtract 1 from the next d₁ largest elements
3. Reorder resulting sequence
4. Repeat until:
    - All zeros (graphic!) OR
    - Negative number or impossible subtraction (not graphic)

**Example**: Is (4,3,3,2,2) graphic?

- Remove 4, subtract from next 4: (3,3,2,2) → (2,2,1,1)
- Remove 2, subtract from next 2: (2,1,1) → (0,0)
- All zeros ✓ Graphic!

**Regular Graphs**:

**Definition**: A graph is **k-regular** if every vertex has degree k

- All vertices have the same degree

**Properties**:

1. For k-regular graph on n vertices:
    - By handshaking: $nk = 2|E|$
    - Therefore: $|E| = \frac{nk}{2}$
    - **Consequence**: For k-regular graph to exist, nk must be even
2. **0-regular**: No edges (empty graph)
3. **1-regular**: Perfect matching (n must be even)
4. **2-regular**: Disjoint union of cycles
5. **(n-1)-regular**: Complete graph $K_n$

**Examples of Regular Graphs**:

- **Cycle** $C_n$: 2-regular
- **Complete graph** $K_n$: (n-1)-regular
- **Complete bipartite** $K_{n,n}$: n-regular
- **Hypercube** $Q_n$: n-regular (n-dimensional)
- **Petersen graph**: 3-regular (10 vertices)

**Degree Bounds and Inequalities**:

**1. Maximum Degree** Δ(G):

- Δ(G) = max{deg(v) : v ∈ V}
- In simple graph: Δ(G) ≤ n-1

**2. Minimum Degree** δ(G):

- δ(G) = min{deg(v) : v ∈ V}

**3. Relationship to Edges**:

- $δ(G) \leq \frac{2|E|}{|V|} \leq Δ(G)$
- Follows from handshaking lemma

**4. For Connected Graphs**:

- δ(G) ≥ 1 (no isolated vertices)

**Degree and Graph Properties**:

**1. Eulerian Graphs**:

- Has Eulerian circuit ⟺ Connected AND all vertices have even degree
- Has Eulerian path ⟺ Connected AND exactly 0 or 2 vertices have odd degree

**2. Hamiltonian Graphs** (Sufficient conditions):

- **Dirac's Theorem**: If δ(G) ≥ n/2 and n ≥ 3, then G is Hamiltonian
- **Ore's Theorem**: If deg(u) + deg(v) ≥ n for all non-adjacent u,v, then G is Hamiltonian

**3. Connectivity**:

- If δ(G) ≥ k, then G has a path of length at least k
- If δ(G) ≥ 2, then G contains a cycle

**4. Graph Coloring**:

- **Brooks' Theorem**: If G is connected, not complete, and not an odd cycle, then χ(G) ≤ Δ(G)
- Greedy coloring uses at most Δ(G) + 1 colors

**5. Trees**:

- Connected acyclic graph on n vertices has exactly n-1 edges
- By handshaking: $\sum \text{deg}(v) = 2(n-1)$
- Therefore: Average degree = $\frac{2(n-1)}{n} < 2$
- **Conclusion**: Every tree with n ≥ 2 has at least 2 leaves (deg 1)

**Degree Sum Formula for Directed Graphs**:

For directed graph:

- $\sum_{v} \text{deg}^+(v) = \sum_{v} \text{deg}^-(v) = |E|$
- Each directed edge contributes 1 to exactly one out-degree and one in-degree

**Tournament**: Complete directed graph (one direction for each pair)

- For tournament on n vertices: $\sum \text{deg}^+(v) = \binom{n}{2}$

**Degree Centrality** (Network Analysis):

**Normalized degree centrality**:

$C_D(v) = \frac{\text{deg}(v)}{n-1}$

Measures importance of vertex in network (0 to 1 scale)

**Problem-Solving Strategy**:

1. Use handshaking lemma to find |E| from degree sum
2. Check degree sequence realizability with Havel-Hakimi
3. Count odd-degree vertices (must be even!)
4. For regular graphs: Check if nk is even
5. Apply degree-based theorems (Dirac, Ore, Brooks)

**GATE Tips**:

- Handshaking: $\sum \text{deg} = 2|E|$ (most frequently used formula)
- Number of odd-degree vertices is always even
- Tree on n vertices: sum of degrees = 2(n-1)
- k-regular on n vertices: nk must be even for graph to exist
- Complete graph $K_n$: Each vertex has degree n-1
- For Eulerian: Check all degrees even (circuit) or exactly 2 odd (path)
- Degree sequence: Sum must be even, each element ≤ n-1

**Common Mistakes**:

- Forgetting loops count twice toward degree
- Confusing maximum degree with number of vertices
- Not checking if nk is even for regular graphs
- Assuming any even-sum sequence is graphic

**Examples**:

1. **Graph with 10 edges, 5 vertices. If 4 vertices have degree 3, what is the degree of the 5th vertex?**
    - By handshaking: $\sum \text{deg} = 2 \times 10 = 20$
    - First 4 vertices contribute: $4 \times 3 = 12$
    - Fifth vertex: $20 - 12 = 8$
    - But wait! Maximum degree in simple graph with 5 vertices is 4
    - Answer: Not possible as simple graph (or has multiple edges)
2. **Is (5,4,4,3,2,2) a graphic sequence?**
    - Sum = 20 (even) ✓
    - Havel-Hakimi:
        - Remove 5, subtract: (4,4,3,2,2) → (3,3,2,1,1)
        - Remove 3, subtract: (3,2,1,1) → (1,0,0)
        - Remove 1, subtract: (0,0) → (-1,0)
    - Negative! Not graphic ✗
3. **How many edges in a 4-regular graph on 7 vertices?**
    - $|E| = \frac{nk}{2} = \frac{7 \times 4}{2} = 14$
4. **Prove: Every tree with n ≥ 2 vertices has at least 2 leaves.**
    - Proof: Tree has n-1 edges
    - By handshaking: $\sum \text{deg} = 2(n-1)$
    - If ≤ 1 leaf, then at most 1 vertex with deg(v) = 1
    - All other n-1 vertices have deg(v) ≥ 2
    - Sum: $\sum \text{deg} \geq 1 + 2(n-1) = 2n-1$
    - But $\sum \text{deg} = 2n-2$
    - Contradiction! Must have ≥ 2 leaves ✓

### 2.3 Graph Coloring (11) {#23-graph-coloring-11}

**Key Concepts**: Assign colors to vertices so no adjacent vertices share color. Minimum colors needed = chromatic number χ(G).

**Chromatic Number χ(G)**:

- Minimum number of colors needed for proper vertex coloring
- NP-complete to compute for general graphs
- **Bounds**: $\omega(G) \leq \chi(G) \leq \Delta(G) + 1$
    - ω(G) = clique number (size of largest complete subgraph)
    - Δ(G) = maximum degree

**Special Cases**:

- **Empty graph**: χ = 1
- **Tree**: χ = 2 (bipartite)
- **Bipartite graph**: χ = 2 (no odd cycles)
- **Complete graph** $K_n$: χ = n
- **Cycle** $C_n$:
    - If n even: χ = 2
    - If n odd: χ = 3
- **Wheel** $W_n$:
    - If n even: χ = 3
    - If n odd: χ = 4
- **Planar graph**: χ ≤ 4 (Four Color Theorem)

**Important Theorems**:

**1. Brooks' Theorem**:

- For connected graph G that is neither complete nor odd cycle:
    
    $\chi(G) \leq \Delta(G)$
    
- Exception: Complete graphs and odd cycles need $\Delta(G) + 1$ colors
- Regular graph: If not complete/odd cycle, can color with degree colors

**2. Four Color Theorem**:

- Every planar graph can be colored with ≤ 4 colors
- Proof: Computer-assisted (controversial initially)
- Practical: Many planar graphs need only 3 colors

**3. Five Color Theorem**:

- Every planar graph can be colored with ≤ 5 colors
- Easier proof than 4-color
- Proof by induction on vertices

**Greedy Coloring Algorithm**:

```
Greedy(G):
    Order vertices as v1, v2, ..., vn
    For each vertex vi:
        Color vi with smallest available color
        (not used by any colored neighbor)
```

- **Time**: $O(V + E)$
- **Colors used**: At most $\Delta(G) + 1$
- **Not optimal**: Depends on vertex ordering
- **Welsh-Powell**: Order by degree (decreasing) for better results

**k-Colorable Graph**:

- Graph that can be properly colored with k colors
- **Decision problem**: "Is χ(G) ≤ k?" is NP-complete for k ≥ 3
- For k = 2: Polynomial time (check bipartiteness via BFS/DFS)

**Bipartite Graphs** (2-colorable):

- Graph is bipartite ⟺ χ(G) = 2 ⟺ No odd cycles
- **Algorithm**: BFS/DFS with alternating colors
    - If contradiction (neighbor has same color) → Not bipartite
- **Applications**: Matching problems, stable marriage

**Edge Coloring**:

- Assign colors to edges so adjacent edges have different colors
- **Edge chromatic number χ'(G)**:
    - Minimum colors needed for edge coloring
    - **Vizing's Theorem**: $\Delta(G) \leq \chi'(G) \leq \Delta(G) + 1$
    - **Class 1**: χ'(G) = Δ(G)
    - **Class 2**: χ'(G) = Δ(G) + 1
- **Bipartite graphs**: Always Class 1 (χ' = Δ)

**Graph Coloring Applications**:

1. **Register Allocation**: Variables = vertices, conflicts = edges
2. **Scheduling**: Tasks = vertices, conflicts = edges
3. **Frequency Assignment**: Radio stations avoiding interference
4. **Sudoku**: Each cell is vertex, constraints are edges
5. **Map Coloring**: Countries = vertices, borders = edges
6. **Exam Scheduling**: Students = vertices, common courses = edges

**Related Problems**:

**1. Clique**:

- Complete subgraph (all pairs connected)
- Clique number ω(G) = size of maximum clique
- ω(G) ≤ χ(G) (need at least ω colors)
- Finding maximum clique is NP-complete

**2. Independent Set**:

- Set of vertices with no edges between them
- Vertices colored with same color form independent set
- Independence number α(G) = maximum independent set size
- χ(G) ≥ $\frac{|V|}{\alpha(G)}$

**3. Vertex Cover**:

- Set of vertices covering all edges
- Complement of independent set
- In bipartite graphs: König's theorem

**Advanced Concepts**:

**1. List Coloring**:

- Each vertex has list of available colors
- **List chromatic number** χₗ(G): Minimum k such that any k-lists allow proper coloring
- Always: χₗ(G) ≥ χ(G)

**2. Fractional Coloring**:

- Generalization allowing fractional colors
- **Fractional chromatic number** χf(G) ≤ χ(G)

**3. Perfect Graphs**:

- Graph where χ(H) = ω(H) for every induced subgraph H
- **Strong Perfect Graph Theorem**: G is perfect ⟺ G and complement