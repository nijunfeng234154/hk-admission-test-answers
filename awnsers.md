**We are to prove by mathematical induction that for every positive integer \( n \):**

\[
1 \times 2 + 2 \times 3 + \dots + n \times (n + 1) = \frac{n(n + 1)(n + 2)}{3}
\]

---

### **Step 1: Base Case (n = 1)**

When \( n = 1 \):

**Left-Hand Side (LHS):**

\[
1 \times 2 = 2
\]

**Right-Hand Side (RHS):**

\[
\frac{1(1 + 1)(1 + 2)}{3} = \frac{1 \times 2 \times 3}{3} = \frac{6}{3} = 2
\]

Since LHS = RHS when \( n = 1 \), the base case holds true.

---

### **Step 2: Inductive Hypothesis**

Assume that the statement is true for some positive integer \( k \):

\[
1 \times 2 + 2 \times 3 + \dots + k \times (k + 1) = \frac{k(k + 1)(k + 2)}{3}
\]

---

### **Step 3: Inductive Step**

We need to show that the statement holds for \( n = k + 1 \):

\[
1 \times 2 + 2 \times 3 + \dots + k \times (k + 1) + (k + 1)(k + 2) = \frac{(k + 1)(k + 2)(k + 3)}{3}
\]

**Starting from the inductive hypothesis:**

\[
\begin{align*}
S(k + 1) &= S(k) + (k + 1)(k + 2) \\
&= \frac{k(k + 1)(k + 2)}{3} + (k + 1)(k + 2)
\end{align*}
\]

**Factor out \( (k + 1)(k + 2) \):**

\[
S(k + 1) = (k + 1)(k + 2) \left( \frac{k}{3} + 1 \right)
\]

**Simplify inside the parentheses:**

\[
\frac{k}{3} + 1 = \frac{k + 3}{3}
\]

So,

\[
S(k + 1) = (k + 1)(k + 2) \left( \frac{k + 3}{3} \right)
\]

**Simplify the expression:**

\[
S(k + 1) = \frac{(k + 1)(k + 2)(k + 3)}{3}
\]

---

### **Conclusion**

Since we have shown that:

\[
1 \times 2 + 2 \times 3 + \dots + (k + 1)(k + 2) = \frac{(k + 1)(k + 2)(k + 3)}{3}
\]

the statement holds true for \( n = k + 1 \) whenever it holds for \( n = k \).

---

### **Final Statement**

By the principle of mathematical induction, the formula:

\[
1 \times 2 + 2 \times 3 + \dots + n \times (n + 1) = \frac{n(n + 1)(n + 2)}{3}
\]

is true for all positive integers \( n \).

---

**Therefore, the proposition is proven by mathematical induction.**



To solve this problem, we'll use **conditional probability** and the **Law of Total Probability**.

---

### **Objective:**

Find the probability that **all balls in the bag are blue** given that **two balls drawn are blue**.

---

### **Step 1: Define Events**

Let:

- \( B_k \): The event that there are exactly \( k \) blue balls in the bag, where \( k = 0, 1, 2, 3, 4 \).
- \( E \): The event that two balls drawn at random are blue.

We need to find \( P(B_4 \mid E) \), the probability that all 4 balls are blue given that the two drawn are blue.

---

### **Step 2: Assign Prior Probabilities**

Assuming no prior information about the number of blue balls, each possible value of \( k \) is equally likely:

\[
P(B_k) = \frac{1}{5} \quad \text{for } k = 0, 1, 2, 3, 4
\]

---

### **Step 3: Compute \( P(E \mid B_k) \)**

We calculate the probability of drawing two blue balls given there are \( k \) blue balls in the bag.

#### **Case 1: \( k < 2 \) (0 or 1 blue balls)**

- It's impossible to draw two blue balls.
- \( P(E \mid B_0) = 0 \)
- \( P(E \mid B_1) = 0 \)

#### **Case 2: \( k = 2 \)**

- Total ways to choose 2 balls from 4: \( \binom{4}{2} = 6 \)
- Ways to choose 2 blue balls from 2: \( \binom{2}{2} = 1 \)
- \( P(E \mid B_2) = \frac{1}{6} \)

#### **Case 3: \( k = 3 \)**

- Ways to choose 2 blue balls from 3: \( \binom{3}{2} = 3 \)
- \( P(E \mid B_3) = \frac{3}{6} = \frac{1}{2} \)

#### **Case 4: \( k = 4 \)**

- All balls are blue, so drawing two blue balls is certain.
- \( P(E \mid B_4) = 1 \)

---

### **Step 4: Compute \( P(E) \) (Total Probability)**

Using the Law of Total Probability:

\[
P(E) = \sum_{k=0}^{4} P(E \mid B_k) \cdot P(B_k)
\]

Plugging in the values:

\[
\begin{align*}
P(E) &= P(E \mid B_0) \cdot P(B_0) + P(E \mid B_1) \cdot P(B_1) + P(E \mid B_2) \cdot P(B_2) \\
&\quad + P(E \mid B_3) \cdot P(B_3) + P(E \mid B_4) \cdot P(B_4) \\
&= 0 + 0 + \left( \frac{1}{6} \cdot \frac{1}{5} \right) + \left( \frac{1}{2} \cdot \frac{1}{5} \right) + \left( 1 \cdot \frac{1}{5} \right) \\
&= \frac{0}{5} + \frac{0}{5} + \frac{1}{30} + \frac{1}{10} + \frac{1}{5}
\end{align*}
\]

Converting all fractions to a common denominator (30):

\[
P(E) = \frac{0}{30} + \frac{0}{30} + \frac{1}{30} + \frac{3}{30} + \frac{6}{30} = \frac{10}{30} = \frac{1}{3}
\]

---

### **Step 5: Compute \( P(B_4 \mid E) \) Using Bayes' Theorem**

\[
P(B_4 \mid E) = \frac{P(E \mid B_4) \cdot P(B_4)}{P(E)} = \frac{1 \cdot \frac{1}{5}}{\frac{1}{3}} = \frac{\frac{1}{5}}{\frac{1}{3}} = \frac{3}{5}
\]

---

### **Answer:**

The probability that all balls in the bag are blue, given that two drawn balls are blue, is:

\[
P(\text{All balls are blue} \mid \text{Two drawn are blue}) = \frac{3}{5}
\]

**Therefore, the required probability is \(\dfrac{3}{5}\).**



To solve this problem, we'll use **conditional probability** and the **Law of Total Probability**.

---

### **Objective:**

Find the probability that **all balls in the bag are blue** given that **two balls drawn are blue**.

---

### **Step 1: Define Events**

Let:

- \( B_k \): The event that there are exactly \( k \) blue balls in the bag, where \( k = 0, 1, 2, 3, 4 \).
- \( E \): The event that two balls drawn at random are blue.

We need to find \( P(B_4 \mid E) \), the probability that all 4 balls are blue given that the two drawn are blue.

---

### **Step 2: Assign Prior Probabilities**

Assuming no prior information about the number of blue balls, each possible value of \( k \) is equally likely:

\[
P(B_k) = \frac{1}{5} \quad \text{for } k = 0, 1, 2, 3, 4
\]

---

### **Step 3: Compute \( P(E \mid B_k) \)**

We calculate the probability of drawing two blue balls given there are \( k \) blue balls in the bag.

#### **Case 1: \( k < 2 \) (0 or 1 blue balls)**

- It's impossible to draw two blue balls.
- \( P(E \mid B_0) = 0 \)
- \( P(E \mid B_1) = 0 \)

#### **Case 2: \( k = 2 \)**

- Total ways to choose 2 balls from 4: \( \binom{4}{2} = 6 \)
- Ways to choose 2 blue balls from 2: \( \binom{2}{2} = 1 \)
- \( P(E \mid B_2) = \frac{1}{6} \)

#### **Case 3: \( k = 3 \)**

- Ways to choose 2 blue balls from 3: \( \binom{3}{2} = 3 \)
- \( P(E \mid B_3) = \frac{3}{6} = \frac{1}{2} \)

#### **Case 4: \( k = 4 \)**

- All balls are blue, so drawing two blue balls is certain.
- \( P(E \mid B_4) = 1 \)

---

### **Step 4: Compute \( P(E) \) (Total Probability)**

Using the Law of Total Probability:

\[
P(E) = \sum_{k=0}^{4} P(E \mid B_k) \cdot P(B_k)
\]

Plugging in the values:

\[
\begin{align*}
P(E) &= P(E \mid B_0) \cdot P(B_0) + P(E \mid B_1) \cdot P(B_1) + P(E \mid B_2) \cdot P(B_2) \\
&\quad + P(E \mid B_3) \cdot P(B_3) + P(E \mid B_4) \cdot P(B_4) \\
&= 0 + 0 + \left( \frac{1}{6} \cdot \frac{1}{5} \right) + \left( \frac{1}{2} \cdot \frac{1}{5} \right) + \left( 1 \cdot \frac{1}{5} \right) \\
&= \frac{0}{5} + \frac{0}{5} + \frac{1}{30} + \frac{1}{10} + \frac{1}{5}
\end{align*}
\]

Converting all fractions to a common denominator (30):

\[
P(E) = \frac{0}{30} + \frac{0}{30} + \frac{1}{30} + \frac{3}{30} + \frac{6}{30} = \frac{10}{30} = \frac{1}{3}
\]

---

### **Step 5: Compute \( P(B_4 \mid E) \) Using Bayes' Theorem**

\[
P(B_4 \mid E) = \frac{P(E \mid B_4) \cdot P(B_4)}{P(E)} = \frac{1 \cdot \frac{1}{5}}{\frac{1}{3}} = \frac{\frac{1}{5}}{\frac{1}{3}} = \frac{3}{5}
\]

---

### **Answer:**

The probability that all balls in the bag are blue, given that two drawn balls are blue, is:

\[
P(\text{All balls are blue} \mid \text{Two drawn are blue}) = \frac{3}{5}
\]

**Therefore, the required probability is \(\dfrac{3}{5}\).**