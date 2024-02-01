+++
title = "Real Analysis"
author = ["James"]
draft = false
+++

`Useful resources`

video
: [Prof. Francis Su](https://www.youtube.com/playlist?list=PL0E754696F72137EC) (Rudin), [Marc Renault](https://www.youtube.com/playlist?list=PLysi2xmniDSzz6xT7IzOifpoexeKccThh) (Abbott)

notes
: [Prof. Francis Su](https://app.box.com/s/azhuul04awaihmims1vcff358a3nn0s0?sortColumn=name&sortDirection=ASC) (Rudin)


extra resources
: Spivak

[MTH 320](https://users.math.msu.edu/users/chamatth/320spring19.html) has problem sets from the Abbott book with solutions. Useful to know which exercices to do optimally.


## 1. The Real Numbers <span class="tag"><span class="ATTACH">ATTACH</span></span> {#1-dot-the-real-numbers}

{{< figure src="/ox-hugo/_20230814_093218screenshot.png" >}}


### Difference upper bound, maximum and supremum (Example 1.3.5). {#difference-upper-bound-maximum-and-supremum--example-1-dot-3-dot-5--dot}

-   open interval \\((0,2) = \\{x \in \mathbb R: 0 < x < 2\\}\\)
-   closed interval \\([0,2] = \\{x \in \mathbb R: 0 \leq x \leq 2\\}\\)

The open interval has no maximum (that is, the biggest element _apart_ of the set) while the closed interval does. The supremum is the smallest possible upper bound of the set. These are both 2 for the open and closed interval. If the supremum is apart of the set, such as the case of the closed interval, it will also be the maximum.

We can now see that not every non-empty bounded set has a maximum, such as the case of the open interval \\((0,2)\\). The Axiom of Completeness states that every nonempty bounded set does have a least upper bound (infimum).

When looking at sets in other fields than \\(\mathbb R\\) such as \\(\mathbb Q\\), this axiom does not hold. Take the set \\(S = \\{r \in \mathbb Q: r^2 < 2\\}\\). The least upper bound does not exist because it is a real number \\(\sqrt 2\\) that can not be expressed in terms of \\(\mathbb Q\\). We can only get so close by finding different upper bounds (141/100, 1415/1000, ...), but never the _least_ upper bound. Then, for any upper bound we find in \\(\mathbb Q\\), there will always be a smaller one.


### Consequences of completeness {#consequences-of-completeness}

-   Archimedean property

    In analysis, it is sometimes good practice to regard a quantifier ∀𝑥 as "no matter how bad 𝑥 is, this still holds", for some notion of "bad". Here there are different notions of bad: 𝑥 is bad when it is small while 𝑦 is bad when it is large.

    It apparently gives rise to the notion of infinitesimals: a number a is said to be infinitesimal w.r.t b when an integer multiple of a can not exceed another number b.

    \\[n x < y\\]

    and a group is archimedean if there is no such number n for which the inequality holds.

<!--listend-->

-   [Planet Math - Archimedean Property](https://planetmath.org/archimedeanproperty)
-   [StackExchange - Archimedean Property and Real Numbers](https://math.stackexchange.com/questions/265384/archimedean-property-and-real-numbers)
-   [Existence of Square Roots](https://math.stackexchange.com/questions/1150808/help-explaining-the-existence-of-a-square-root-proof)


### Exercices {#exercices}


#### Exercise 1.2.1 {#exercise-1-dot-2-dot-1}

**Prove that \\(\sqrt 3 \\) is irrational. Does a similar agument work to show \\(\sqrt 6\\) is irrational?**

Proof. Assume, to the contrary, that there exists integers \\(p\\) and \\(q\\) such that \\(\sqrt 3\\) is rational. Furthermore, assume that \\(p\\) and \\(q\\) do not have common factors such that the fraction
\\[\Big(\frac{p}{q}\Big)^2 = 3\\]

can not be simplified more. This can be rewritten to
\\[p^2 = 3 q^2\\]

meaning \\(p^2\\) is a multiple of \\(3\\) and so is \\(p\\). It then holds that \\(p = 3r\\) for any integer \\(r\\). Inserting \\(3r\\) into this previous equation results in:
\\[9r^2 = 3q^2\\]
\\[3r^2 = q^2\\]

implying that \\(q^2\\) also is a multiple of \\(3\\). As we have shown that there is a common factor, we have reached a contradiction, and the original statement is true. \\(\blacksquare\\)

A similar argument will be possible for \\(\sqrt 6\\): we will then conclude that they must be a multiple of \\(2\\) and \\(3\\), and ...

**Where does the proof of Theorem 1.1.1 break down if we try to use it to prove \\(\sqrt{4}\\) is irrational?**
\\[\Big(\frac{p}{q}\Big)^2 = 4\\]
\\[p^2 = 4q^2\\]

This does not imply \\(p\\) is a multiple of four, as \\(p\\) could be \\(2\\). \\(4\\) is a perfect square.


#### Exercise 1.2.2 {#exercise-1-dot-2-dot-2}

**Show that there is no rational number \\(r\\) satisfying \\(2^r = 3\\).**

Proof. Assume, to the contrary, that there is a rational number \\(r\\) such that \\(2^r = 3\\). Then there exist integers \\(p, q\\) such that \\(r = \frac{p}{q}\\). It follows that
\\[2^{\frac{p}{q}} = 3\\]

Taking the \\(q\\)-th power on both sides yields \\(2^p = 3^q\\). This leads to a contradiction as the left-hand side is an even number while the right-hand side is an odd number. \\(\blacksquare\\)


#### _LATER_ Exercise 1.2.3 {#later-exercise-1-dot-2-dot-3}

1.  Consider \\(A\_1 = \\{1, 2, \ldots\\}, A\_2 = \\{2, 3, \ldots\\}\\) which has \\(\bigcap\_{n=1}^\infty A\_n = \emptyset\\).
    (these sets were mentioned in the chapter)
2.  True. Set \\(A\_j\\) will be reached which will have a single common element with the other sets.
    (**solution manual**: apparently this result will become more clear in chapter 3 regarding compactness. Verify this when the time is right.)
3.  False. We can show this by either generating a few sets and calculating this, or by taking \\(A = \emptyset\\) which results in the LHS being empty while the RHS is equal to C (\\(\emptyset = C\\)).
4.  True (associative)
5.  True (diagram)


#### Exercise 1.2.4 {#exercise-1-dot-2-dot-4}

**Produce an infinite collection of sets \\(A\_1, A\_2, A\_3, \ldots\\) with the property that every \\(A\_i\\) has an infinite number of elements, \\(A\_i \cap A\_j = \emptyset\\) for all \\(i \neq j\\) and \\(\bigcup\_{i=1}^{\infty} = \mathbb N\\).**

\\(A\_n = \\{n, n+1, n+2, \ldots\\}\\) does not work, because \\(A\_1\\) and \\(A\_2\\) will have \\(2, 3, \ldots\\) in the intersection. Instead, an infinite way of  **partitioning** \\(\mathbb N\\) must be found instead.

What this question is asking for us a way to find an infinite number of infinite disjoint sets that partition \\(\mathbb N\\).

-   <https://math.stackexchange.com/questions/51096/partition-of-n-into-infinite-number-of-infinite-disjoint-sets>
-   <https://math.stackexchange.com/questions/12629/partitioning-an-infinite-set/12632#12632>

Let \\(U\_1\\) be the set of positive odd numbers: {1, 3, 5, 7, 11, ...}. Let \\(U\_2\\) be the set of twice the positive odd numbers: {2, 6, 10, 14, ...}. Let \\(U\_3\\) be the set of four times the positive odd numbers (4, 12, 20, 28, ...) and so on and so on.

Then, \\(U\_n\\) = the set of \\(2^{n-1}\\) times the positive odd numbers will be the set that partitions \\(\mathbb N\\).


#### Exercise 1.2.5 {#exercise-1-dot-2-dot-5}

1.  If \\(x \in (A \cup B)^c\\), then \\(x \in A \cup B\\) so either \\(x \notin A\\) or \\(x \notin B\\) or both. This implies that \\(x \in A^c\\) or \\(x \in B^c\\) and thus \\(x \in A^c \cup B^c\\).
2.  Let \\(x \in A^c \cup B^c\\). This means that either \\(x \in A^c\\) or \\(x \in B^c\\) so \\(x \notin A\\) or \\(x \notin B\\). This implies \\(x \notin A \cap B\\) which is the same as \\(x \in (A \cap B)^c\\).
3.  We have to show \\((A \cup B)^c = A^c \cap B^c\\) by showing the inclusion both ways. This means we must show \\((A \cup B)^c \subseteq A^c \cap B^c\\) and \\(A^c \cap B^c \subseteq (A \cup B)^c\\).

    Proof.

    1.  The implication \\((A \cup B)^c \subseteq A^c \cap B^c\\)

        Assume that \\(x \in (A \cup B)^c\\), so \\(x \notin A \cup B\\). This means that \\(x \notin A\\) _and_ /\\(x \notin B\\) (it is not in both bc of the union), which further implies that \\(x \in A^c\\) and \\(x \in B^c\\) and so \\(x \in A^c \cap B^c\\).

    2.  The implication \\(A^c \cap B^c \subseteq (A \cup B)^c\\)

        Similarly, if \\(x \in A^c \cap B^c\\), we know that \\(x \in A^c\\) and a\\(x \in B^c\\). From this, \\(x \notin A\\) and \\(x \notin B\\). Furthermore, \\(x \notin A \cup B\\) and \\(x \in (A \cup B)^c\\).

    As inclusion has been shown both ways, we have that w\\((A \cup B)^c = A^c \cap B^c\\). \\(\blacksquare\\)


#### Exercise 1.2.6 {#exercise-1-dot-2-dot-6}

1.  **Verify the triangle inequality in the special case where \\(a\\) and \\(b\\) have the same sign**.
    Triangle inequality: \\(\vert a + b \vert \leq \vert a \vert + \vert b \vert\\)
    1.  Case 1. \\(a\\) and \\(b\\) are both positive. Then \\(\vert a \vert = a\\) and \\(\vert b \vert = b\\) such that \\(\vert a + b \vert = a + b = \vert a \vert + \vert b \vert\\).
    2.  Case 2. \\(a\\) and \\(b\\) are both negative. Then \\(a < 0, b < 0\\)  and so will \\(a + b < 0\\). \\(\vert a \vert = -a, \vert b \vert = -b\\) such that \\(\vert a +b \vert = - (a + b)\\). It follows that \\(\vert a + b \vert = -(a+b) = -a + (-b)= \vert a \vert + \vert b \vert\\).


#### Exercise 1.2.7 {#exercise-1-dot-2-dot-7}

**Given a function \\(f\\) and a subset \\(A\\) of its domain, let \\(f(A)\\) represent the range of \\(f\\) over the set \\(A\\): that is, \\(f(A) = \\{f(x) : x \in A\\}\\).**

1.  **Let \\(f(x) = x^2\\). If \\(A = [0, 2]\\) and \\(B = [1,4]\\), find \\(f(A)\\) and \\(f(B)\\). Does \\(f(A \cap B) = f(A) \cap f(B)\\) in this case? Does \\(f(A \cup B) = f(A) \cup f(B)\\)?**

    \\(f(A) = [0, 4]\\) and \\(f(B) = [1, 16]\\). \\(A \cap B = [1, 2]\\) and so \\(f(A \cap B) = [1, 4]\\) while \\(f(A) \cap f(B) = [1, 4]\\) so in this case they are equivalent.

    \\(A \cup B = [0, 4]\\) implies that \\(f(A \cup B) = [0, 16]\\) while \\(f(A) \cup f(B) = [0, 16] \\) so this is also equivalent.
2.  **Find two sets A and B for which \\(f(A \cap B) \neq f(A) \cap f(B)\\).**

    \\(A = [-1, 0]\\) and \\(B = [0, 1]\\) resulting in \\(A \cap B = \\{0\\}\\) and \\(f(A \cap B) = \\{0\\}\\) while \\(f(A) \cap f(B) = \\{1\\}\\).
3.  **Show that for an arbitrary function \\(g : \mathbb R \rightarrow \mathbb R\\), it is always true that \\(g(A \cap B) \subseteq g(A) \cap g(B)\\) for all sets \\(A, B \subseteq \mathbb R\\).**

    Proof. We must show that \\(y \in g(A \cap B)\\) implies \\(y \in g(A) \cap g(B)\\). If \\(y \in g(A \cap B)\\), there exists an \\(x \in A \cap B\\) such that \\(g(x) = y\\). This means that \\(x \in A\\) and \\(x \in B\\), and thus \\(g(x) \in g(A) \\) and \\(g(x) \in g(B)\\). We conclude that \\(g(x) = g(A) \cap g(B)\\). \\(\blacksquare\\)
4.  **Form and prove a conjecture about the relationship between \\(g(A \cup B)\\) and \\(g(A) \cup g(B)\\) for an arbitrary function \\(g\\).**

    My claim is that \\(g(A \cup B) = g(A) \cup g(B)\\) for any arbitrary function \\(g\\) and \\(A, B \subseteq R\\).

    Proof. We must show the following two inclusions:

    1.  \\(g(A \cup B) \subseteq g(A) \cup g(B)\\)
    2.  \\(g(A) \cup g(B) \subseteq g(A \cup B)\\)

    For (1), take an element \\(y \in g(A \cup B)\\), meaning there exists an \\(x \in A \cup B\\) such that \\(g(x) = y\\). Then, \\(x \in A\\) or \\(x \in B\\), which implies that either \\(g(x) \in g(A)\\) or \\(g(x) \in g(B)\\), revealing that \\(g(x) \in g(A) \cup g(B)\\). For the reverse inclusion (2), similarly assume that \\(z \in g(A) \cup g(B)\\). This means that either e\\(z \in g(A)\\) or \\(z \in g(B)\\) and thus there is an \\(x \in A\\) or \\(x \in B\\) such that \\(g(x) = z\\). This implies \\(x \in A \cup B\\) and hence \\(g(x) = g(A \cup B)\\). Because (1) and (2) have been shown to be true, we can conclude that \\(g(A \cup B) = g(A) \cup g(B)\\). \\(\blacksquare\\)


#### _NOTDONE_ Exercise 1.2.8 {#notdone-exercise-1-dot-2-dot-8}

**Give an example of each or state that the request is impossible**.

1.  **\\(f : \mathbb N \rightarrow \mathbb N\\) that is 1-1 but not onto**.

<!--listend-->

1.  **\\(f : \mathbb N \rightarrow \mathbb N\\) that is onto but not 1-1**.

<!--listend-->

1.  **\\(f : \mathbb N \rightarrow \mathbb \mathbb Z\\) that is 1-1 and onto**.


#### _INCOMPLETE_ Exercise 1.2.10 {#incomplete-exercise-1-dot-2-dot-10}

**Decide which of the following are true statements. Provide a short justification for those that are valid and a counterexample for those that are not:**

1.  **Two real numbers satisfy \\(a < b\\) if and only if \\(a < b + \epsilon\\) for every \\(\epsilon > 0\\)**.

    False. If \\(a = b\\) then \\(a < b + \epsilon\\) for all \\(\epsilon > 0\\) but \\(a \nless b\\).

2.  **Two real numbers satisfy \\(a < b\\) if \\(a < b + \epsilon\\) for every \\(\epsilon > 0\\)**.

    False. Consider \\(a=b\\), then \\(a < b + \epsilon\\) for all \\(\epsilon > 0\\) but this means \\(a \nless b\\).

3.  **Two real numbers satisfy \\(a \leq b\\) if and only if \\(a < b + \epsilon\\) for every \\(\epsilon > 0\\)**.

    Proof. For the inclusion, suppose \\(a < b + \epsilon\\) for every \\(\epsilon > 0\\). This results in either \\(a \leq b\\) or \\(a > b\\), but \\(a > b\\) is impossible as the


#### _NOTDONE_ Exercise 1.2.11 {#notdone-exercise-1-dot-2-dot-11}

Form the logical negation of each claim.

1.  **For all real numbers satisfying \\(a < b\\), there exists an \\(n \in \mathbb N\\) such that \\(a + 1/n < b\\)**.

2.  **There exists a real number \\(x > 0\\) such that \\(x < 1/n\\) for all \\(n \in \mathbb N\\)**.

3.  **Between every two distinct real numbers there is a rational number**.


#### Exercise 1.2.12 {#exercise-1-dot-2-dot-12}

**Let \\(y\_1 = 6\\), and for each \\(n \in \mathbb N\\) define \\(y\_{n+1} = (2y\_n -6) / 3\\)**.

**Use induction to prove that the sequence satisfies \\(y\_n > -6\\) for all \\(n \in \mathbb N\\)**.

-   Base case. Assume \\(n=1\\), then \\(y\_1 = 6\\). Because \\(6 > -6\\), the base case holds true.

-   Induction hypothesis. Assume that \\(y\_n > -6\\). We now wish to prove that this will also be true for \\(y\_{n+1}\\).

    \begin{align\*}
          y\_n &> -6 \\\\
          2y\_n &> -12 \\\\
          2y\_n - 6 &> -18 \\\\
          (2y\_n - 6)/3 &> -6 \\\\
    \end{align\*}

    Because the LHS is identical to \\(y\_{n+1}\\), we conclude that \\(y\_{n+1} > -6\\).

**Use another induction argument to show the sequence \\((y\_1, y\_2, y\_3, \ldots)\\) is decreasing**.
Induction argument: \\(y\_{n+1} \leq y\_n\\) for all values of \\(n \in \mathbb N\\).

-   Base case. For \\(n=1\\), we have \\((2\cdot 6 - 6)/3 = 2 \leq 6\\).

-   Induction hypothesis. Suppose that \\(y\_{n+1} < y\_n\\). `isn't this weird to assume, as if we already have the solution?`

-   Induction step.

    \begin{align\*}
        y\_{n+1} &\leq y\_n \\\\
        2y\_{n+1} &\leq 2y\_n \\\\
        2y\_{n+1} - 6 &\leq 2y\_n-6 \\\\
        (2y\_{n+1} - 6)/3 &\leq (2y\_n-6)/3 \\\\
        y\_{n+2} &\leq y\_{n+1}
    \end{align\*}

    so \\(y\_n\\) is decreasing. _An alternative is assuming \\(y\_{n-1} > y\_n\\), and then this will get us the induction hypothesis we have right now as the result of our induction step_.


#### Exercise 1.3.3 {#exercise-1-dot-3-dot-3}

**Let \\(A\\) be nonempty and bounded below, and define \\(B = \\{b \in \mathbb R : b \text{ is a lower bound for } A\\}\\). Show that \\(\sup B = \inf A\\)**.

B contains all real numbers that are a lower bound for \\(A\\). This means each \\(b \in B\\) satisfies \\(b \leq a\\) for every \\(a \in A\\) (_Definition 1.3.1_). By definition, \\(B\\) is nonempty and bounded above by any element in \\(A\\). This means that \\(B\\) per the _Axiom of Completeness_ has a least upper bound (supremum) and let \\(s = \sup B\\). \\(s\\) is an upper bound for \\(B\\) and if \\(b\\) is any other upper bound, then \\(s \leq b\\).

Now that we have shown that B has a supremum, we must show that this supremum is a lower bound for \\(A\\). Take any \\(a \in A\\), then by definition of \\(B\\) we have that \\(b \leq a\\) for all \\(b \in B\\). Therefore, a is an upper bound for B. Since \\(s\\) is the least upper bound for \\(A\\), we have that \\(s \leq a\\) and thus \\(s\\) is a lower bound for \\(A\\).

Next, we show that this lower bound is the greatest lower bound for \\(A\\). Let \\(l\\) be a lower bound for \\(A\\), it follows that \\(l \in B\\). Since \\(s\\) is an upper bound for \\(B\\) we have that \\(l \leq s\\). Therefore, \\(s\\) is the greatest lower bound and \\(s = \inf A\\).

**Use (a) to explain why there is no need to assert that greatest lower bounds exist as part of the Axiom of Completeness**.
All we had to show that a greatest lower bound exist is that there is another set that consists of the elements of lower bounds of another set, being bound from above. This uses the Axiom of Completeness


#### Exercise 1.3.4 {#exercise-1-dot-3-dot-4}

**Let \\(A\_1, A\_2, A\_3, \ldots\\) be a collection of nonempty sets, each of which is bounded above**.

**Find a formula for \\(\sup (A\_1 \cup A\_2)\\). Extend this to \\(\sup (\bigcup\_{k=1}^n A\_k)\\)**.

The union of two sets consist of all elements \\(a \in A\_1\\) or \\(b \in A\_2\\). The supremum must then be biggest least upper bound of the two sets: \\(\sup(A\_1 \cup A\_2) = \max (\sup A\_1, \sup A\_2)\\).

For inf: \\(\sup ( \bigcup\_{n=1}^N = \max(\sup A\_1, \sup A\_2, \ldots, \sup A\_n))\\)

**Consider \\(\sup (\bigcup\_{k=1}^n A\_k)\\). Does the formula in (a) extend to the infinite case**?

No, because \\(\bigcup\_{k=1}^\infty A\_k\\) may be unbounded. Take for example \\(A\_n = [n, n+1]\\).


#### Exercise 1.3.6 {#exercise-1-dot-3-dot-6}

**Given sets \\(A\\) and \\(B\\), define \\(A + B = \\{a + b : a \in A \text{ and } b \in B\\}\\). Follow these steps to prove that if \\(A\\) and \\(B\\) are nonempty and bounded above then \\(\sup(A+B) = \sup A + \sup B\\)**.

**Let \\(s = \sup A\\) and \\(t = \sup B\\). Show \\(s + t\\)  is an upper bound for \\(A + B\\)**.

Because \\(s=\sup A\\) we have that \\(a \leq s\\) for all \\(a \in A\\) and \\(t = \sup B\\) implies that \\(b \leq t\\) for all \\(b \in B\\). It follows that by adding these two equations we have b\\(a + b \leq s + t\\).

**Now let \\(u\\) be an arbitrary upper bound for \\(A+B\\) and temporarily fix \\(a \in A\\). Show \\(t \leq u - a\\)**.

\\(u\\) is an arbitrary upper bound for \\(A + B\\) so \\(a + b \leq u\\) for any \\(b \in B\\) (a is fixed) and so \\(b \leq u - a\\). Because \\(b\\) is fixed, \\(u-a\\) is an upper bound for \\(B\\). By the least upper bound definition for \\(B\\), \\(t \leq u - a\\).

**Finally, show \\(\sup(A+B) = s+t\\)**.

We have that \\(t \leq u - a \implies a \leq u-t\\). Since \\(a\\) was arbitrary we have by the least upper bound definition for \\(A\\) that \\(s \leq u - t \implies s + t \leq u\\) where \\(u\\) was an upper bound. Therefore, \\(s + t = \sup A + \sup B\\) is the least upper bound.

**Construct another proof of this same fact using Lemma 1.3.8**.

Let \\(\epsilon > 0\\) be given. Then, by Lemma 1.3.8, there are elements \\(a \in A, b \in B\\) such that \\(s - \epsilon/2 < a\\) and \\(t - \epsilon/2 < b\\). Adding the equations:
        \\[(s+t) - \epsilon < a + b\\]
Therefore, after applying Lemma 1.3.8, we conclude that \\(s+t = \sup A + \sup B\\).


#### Exercise 1.3.8 {#exercise-1-dot-3-dot-8}

**Compute, without proofs, the suprema and infima (if they exist) of the following sets**.

\\(\\{m/n : m, n \in \mathbb N \text{ with } m < n\\}\\)

-   sup = 1, inf = 0

\\(\\{(-1)^m/n : m, n \in  \mathbb N \\}\\)

-   sup = 1, inf = -1

ii\\(\\{n/(3n+1) : n \in  \mathbb N \\}\\)

-   sup = 1/3, inf = 1/4

\\(\\{m/(m+n) : m, n \in  \mathbb N \\}\\)

-   sup = 1, inf = 0


## 2. Sequences and Series {#2-dot-sequences-and-series}


## 3. Basic Topology of R {#3-dot-basic-topology-of-r}


## 4. Functional Limits and Continuity {#4-dot-functional-limits-and-continuity}


## 5. The Derivative {#5-dot-the-derivative}


## 6. Sequences and Series of Functions {#6-dot-sequences-and-series-of-functions}


## 7. The Riemann Integral {#7-dot-the-riemann-integral}


## 8. Additional topics {#8-dot-additional-topics}
