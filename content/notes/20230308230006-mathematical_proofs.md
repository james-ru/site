+++
title = "Mathematical Proofs"
author = ["James"]
tags = ["todo", "math"]
draft = false
+++

<span class="underline">Resources:</span>

-   **Mathematical proofs - a transition to advanced mathematics**
    started: somewhere in the first week of July 2022, Switzerland trip. One small pitfall: I skipped a lot of exercices that were a lot of work or lengthy. Not smart.

-   Slides: <https://media.pearsoncmg.com/cmg/pmmg_mml_shared/Chartrand_4e/>


## Sets {#sets}

subset
: A set \\(A\\) is called a **subset** of a set \\(B\\) if every element of \\(A\\) also belongs to \\(B\\).
    Notation: \\(A \subseteq B\\)


proper subset
: A set \\(A\\) is a **proper subset** of a set \\(B\\) if \\(A \subseteq B\\) but \\(A \neq B\\).
    Notation: \\(A \subset B\\)


subset vs proper subset
: A subset is a collection of objects from a set. A proper subset is any subset which is not the set itself.


index sets
: Index sets allow us to describe the union/intersection of some sets in a more 'specific' way as opposed to **sigma** notation.
    -   sigma way: \\(\bigcup\_{i=1}^n A\_i = A\_1 \cup A\_2 \cup \ldots \cup A\_n\\)
    -   now consider instead an **arbitrary** index set \\(I = \\{1, 2, 4, 6\\}\\)

        Suppose a set \\(S\_\alpha\\) exists for each \\(\alpha \in I\\). (alternatively, look at this as \\(A\_\alpha\\)).

        The **indexed collection of sets** (which is the collection of all sets \\(S\_\alpha\\), where \\(\alpha \in I\\)) is then \\(\\{S\_\alpha\\}\_{\alpha \in I}\\). We can now define the union and intersection:

        \\(\displaystyle \bigcup\_{\alpha \in I} S\_\alpha = \\{x : x \in S\_\alpha \text{ for some } \alpha \in I\\}\\)

        \\(\displaystyle \bigcap\_{\alpha \in I} S\_\alpha = \\{x : x \in S\_\alpha \text{ for all } \alpha \in I\\}\\)

        Index sets literally allow us to look at certain indices of sets, as if we're using a loop with specific arrays to go through specifically.

        resource for understanding: <https://www.youtube.com/watch?v=PvhRD_h7Q9I>


## Logic {#logic}

biconditional
: The biconditional \\(p \Leftrightarrow q\\) exists out of the conjunction of \\(p\\) implies \\(q\\) and its converse.

    Recall that \\(p \implies q\\) is only false when \\(p\\) is true and \\(q\\) is false. Conversely, \\(q \implies p\\) is only false when \\(q\\) is true and \\(p\\) is false. The other information is never being spoken about in these two statements (except for the implications mentioned), hence they are true.

    This means that when we have a T/F or F/T situation, the conjunction is false. Otherwise, in a T/T or F/F situation, the conjunction is true.

    also denoted as **if and only if** or **... equivalent to ...**  or **... is a necessary and sufficient condition for ...**


logically equivalent
: Two statements \\(R\\) and \\(S\\) are logically equivalent when both have the same truth values for all combinations of truth values.

    Having the same truth values means that the biconditional of these two statements are T for all truth values. Hence we can say that two statements are also logically equivalent if **the biconditional is a tautology**.

    Conversely, if the biconditional is a tautology, the statement is logically equivalent.


## Direct Proof and Proof by Contrapositive {#direct-proof-and-proof-by-contrapositive}

<span class="underline">Without loss of generality</span>

-   [Use of "without loss of generality"](https://math.stackexchange.com/questions/129137/use-of-without-loss-of-generality)
-   indicates an assumption is chosen arbitrarily, narrowing the premise to a particular case, but does not affect the validity of the proof in general


## More on Proof and Proof by Contrapositive {#more-on-proof-and-proof-by-contrapositive}

extra
: <https://faculty.nps.edu/rgera/current_classes/MA1025/Ch4.pdf>

more on congruence
: <https://www.math.nyu.edu/~hausner/congruence.pdf>


### Proofs Involving Divisibility of Integers {#proofs-involving-divisibility-of-integers}

When we say that \\(a \mid b\\), we say that there is an integer \\(c\\) such that \\(b = ac\\). This also means that \\(b\\) is a multiple of \\(a\\).

For example: \\(2 \mid x\\) iff \\(x = 2k, \exists k \in \mathbb{Z}\\). This means that the integer 2 is a factor of \\(x\\).

If \\(a\\) does not divide \\(b\\), we write \\(a \nmid b\\). Then there exists no such integer \\(c\\) for \\(b = ac\\). If for example \\(3 \nmid x\\), then we can write that \\(x = 3k + 1, x = 3k + 2, \exists k \in \mathbb{Z}\\).

\\(4 \nmid 66\\) because there is no integer \\(c\\) such that \\(66 = 4c\\). However, we do have a \\(c\\) if we write \\(66 = 4c + 2\\) (but this doesn't hold for +1, +3 like mentioned above so I'm not sure what's going on). =&gt; **this depends on what the remainder is of course!**

Apparently we will have **the division algorithm** later on in chapter 11. Let me give an example. If an integer \\(n\\) is not a multiple of 3, then we can write \\(n = 3q + 1\\) or \\(n = 3q + 2\\) for some integer \\(q\\). This is because \\(0, 1, 2\\) are the only remainders that can result when an integer is divided by 3. And for 4 we have +1, +2, +3, this goes on and on.


### Proofs Involving Congruence of Integers {#proofs-involving-congruence-of-integers}

recall what divisibility is...means that there is an integer c such that...

**Theorem**. Let \\(x, y \in \mathbb{Z}\\). Then \\(x\\) and \\(y\\) are of the same parity if and only if \\(2 \mid (x - y)\\). <br />

**Strategy**. This is a biconditional statement \\(p \iff q\\). For \\(p \implies q\\) we will consider a direct proof and for its converse, \\(q \implies p\\), we will use a proof by contrapositive such that \\(\neg p \implies \neg q\\). <br />

**Proof**. Assume that \\(x,y\\) are of the same parity. Then we have the following two cases:

1.  \\(x\\) and \\(y\\) are both even. Thus \\(x = 2a\\) and \\(y = 2b\\) for \\(a, b \in \mathbb{Z}\\). Then:
    \\[x - y = 2a - 2b = 2(a-b)\\]

    Because \\(a-b\\) is an integer, it follows that \\(2 \mid (x-y)\\).

2.  \\(x\\) and \\(y\\) are both odd. Thus \\(x = 2c + 1\\) and \\(y = 2d+1\\) for \\(c, d \in \mathbb{Z}\\). Then:
    \\[x - y = 2c + 1 - (2d + 1) = 2c - 2d = 2(c-d)\\]

    Because \\(c-d\\) is an integer, it follows that \\(2 \mid (x-y)\\).

For the converse, let us assume that \\(x\\) and \\(y\\) are not of the same parity. We must show that \\(2 \nmid (x-y)\\). We will have two cases.

1.  \\(x\\) is even, \\(y\\) is odd. Then \\(x = 2a\\) and \\(y = 2b+1\\) for some \\(a,b \in \mathbb{Z}\\). Then

    \\[(x-y) = 2a - 2b - 1 = 2(a-b) - 1\\]

    Since \\(a-b\\) is an integer, \\(2 \nmid (x-y)\\).

2.  Same procedure as above. \\(\blacksquare\\)

**Congruency**

> We say integers a and b are "congruent modulo n" if their difference is a multiple of n.


## Existence and Proof by Contradiction {#existence-and-proof-by-contradiction}

Some quantified statements of the type \\(\forall x \in S, R(x)\\) are false. In essence, this means the following:

\begin{equation}
\neg (\forall x \in S, R(x)) \equiv \exists x \in S, \neg R(x))
\end{equation}

Meaning, if the statement \\(\forall x \in S, R(x)\\) is false, then there exists some element \\(x\\) for which \\(R(x)\\) is false. This element \\(x\\) is a **counterexample** of the given statement above.

Note that this shows an underlying asymmetry. To show that this statement is false, only a single counterexample is required. It does _not_ require proving some other result. For the other way, a more in-depth approach is required (see the end of this chapter in the book).

In a **proof by contradiction**, we assume the statement is a false statement. If we then deduce a statement that contradicts a _known_ assumption (an axiom, fact, theorem, definition, ...), we know the original statement is true (because there is no way for it to be false, as it results in a contradiction). The following paragraph explores our intuition behind it.

\\(\forall x \in S, P(x) \implies Q(x)\\). Assume \\(R\\) is a false statement. Suppose this contradicts an assumption we call \\(P\\), then we have deduced \\(\neg P\\). This produces the contradiction \\(C: P \wedge (\neg P)\\). We then have found the truth of the implication \\((\neg R) \implies C\\). Because this implication is true and \\(C\\) is false, it follows that \\(\neg R\\) is false and so \\(R\\) is true (because there is no other way for the implication to be true!).

(recall the implication table)

| p | q | p &rArr; q |
|---|---|------------|
| T | T | T          |
| T | F | F          |
| F | T | T          |
| F | F | T          |


## Proof by Induction {#proof-by-induction}

check later:

-   [What exactly is the difference between weak and strong https?](https://math.stackexchange.com/questions/1184541/what-exactly-is-the-difference-between-weak-and-strong-induction)
-   [Why is mathematical induction a valid proof technique? [duplicate]​](https://math.stackexchange.com/questions/1139579/why-is-mathematical-induction-a-valid-proof-technique/1139606#1139606)

**Defs**

principle of mathematical induction
: For each positive integer \\(n\\), let \\(P(n)\\) be a statement. If:

    1.  \\(P(1)\\) is true and
    2.  the implication: if \\(P(k)\\), then \\(P(k+1)\\) is true for every positive integer \\(k\\),

    then \\(P(n)\\) is true for every positive integer \\(n\\).


principle of mathematical induction (more general)
: For a fixed integer \\(m\\), let \\(S = \\{i \in \mathbb{Z} : i \geq m\\}\\).
    For each integer \\(n \in S\\), let \\(P(n)\\) be a statement. If

    1.  \\(P(m)\\) is true and
    2.  the implication: if \\(P(k)\\), then \\(P(k+1)\\) is true for every positive integer \\(k\\),

    then \\(P(n)\\) is true for every integer \\(k \in S\\).


proof by minimum counterexample
: hybrid of induction and proof by contradiction
    Proposition. The statements \\(S\_1, S\_2, S\_3, \ldots\\) are all true.
    1.  Check that the first statement \\(S\_1\\) is true.
    2.  For the sake of contradiction, suppose not every \\(S\_n\\) is true.
    3.  Let \\(k > 1\\) be the smallest integer for which \\(S\_k\\) is **false**.
    4.  Then \\(S\_{k-1}\\) is true and \\(S\_k\\) is false. Use this to get a contradiction.

> For the universally quantified statement ∀n ∈ N, P(n), a proof by smallest counterexample assumes that P(1) is true, but that there is a smallest k &gt; 1 such that P(k) is false.
> This sets up the scenario where, because k is the smallest value for which P(k) is false, that P(k − 1) is true.
> Using P(k − 1) being true and P(k) being false, we seek a contradiction

strong principle of mathematical induction
: For each positive integer \\(n\\), let \\(P(n)\\) be a statement. If

    1.  \\(P(1)\\) is true and
    2.  the implication: if \\(P(i)\\) for every integer \\(i\\) with \\(1 \leq i \leq k\\), then \\(P(k+1)\\) is true for every positive integer \\(k\\),

    then \\(P(n)\\) is true for every positive integer \\(n\\).


strong principle of mathematical induction (more general)
: For a fixed integer \\(m\\), let \\(S = \\{i \in \mathbb{Z} : i \geq m\\}\\).
    For each integer \\(n \in S\\), let \\(P(n)\\) be a statement. If

    1.  \\(P(m)\\) is true and
    2.  the implication: if \\(P(i)\\) for every integer \\(i\\) with \\(m \leq i \leq k\\), then \\(P(k+1)\\) is true for every positive integer \\(k\\),

    then \\(P(n)\\) is true for every integer \\(n \in S\\).


## Prove or Disprove {#prove-or-disprove}


## Equivalence relations {#equivalence-relations}

**Theorem**. Let \\(R\\) be an equivalence relation on a nonempty set \\(A\\) and let \\(a\\) and \\(b\\) be elements of A. Then \\([a] = [b]\\) if and only if \\(a  R b\\).
