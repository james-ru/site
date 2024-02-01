+++
title = "Solid-State Physics"
author = ["James"]
draft = false
+++

## 8. Electron Levels in a Periodic Potential {#8-dot-electron-levels-in-a-periodic-potential}

-   [StackExchange - Bloch's theorem](https://physics.stackexchange.com/questions/111286/blochs-theorem)

**Born-Von Karman boundary condition**

\\[ \psi(\mathbf r + N\_i \mathbf a\_i) = \psi(\mathbf r),  \hspace{1cm} i = 1, 2, 3\\]

where \\(\mathbf a\_i\\) are three primitive vectors and \\(N\_i\\) all integers where \\(N = N\_1 N\_2 N\_3\\) is the total number of primitive cells in the crystal.

-   This means that we can move our wave function towards any amount of unit cell \\(N\_i\\) in the direction of \\(\mathbf a\_i\\) and we'll get the same wave function.
-   Essentially, 'wrapping' the crystal such that the atoms on one edge of the crystal are neighbours to the atoms on the opposite edge, creating a topological loop.

Applying Bloch's theorem and this BC, it can be found that
        \\[\Delta \mathbf k = \frac{1}{N} \mathbf b\_1 \cdot (\mathbf b\_2 \times \mathbf b\_3) \\]

-   _The number of allowed wave vectors in a primitive cell of the reciprocal lattice is equal to the number of sites in the crystal_.
-   In other words, \\(\Delta \mathbf k = \frac{(2 \pi )^3}{V} \\).

**Crystal momentum**

-   Bloch's theorem introduces the wave vector \\(\mathbf k\\). In Sommerfeld theory, a similar free electron wave vector exists in the form of \\(\mathbf p/\hbar\\) where \\(\mathbf p\\) is the momentum of the electron. However, \\(\mathbf k\\) from Bloch is not proportional at all to this electronic momentum.

    If the momentum operator \\(\mathbf p = -i\hbar \mathbf \nabla \\) acts on \\(\psi\_{nk}\\) (we have \\(n\\) possible bands for the \\(k\\)-th crystal momentum but this has not yet been formally defined), we get (the nabla acts on \\(\mathbf r\\)):

\begin{align}
    -i \hbar \nabla \psi\_{n\mathbf k} &= -ih \nabla (e^{i \mathbf k \cdot \mathbf r} u\_{n \mathbf k} (\mathbf r)) \\\\
    &= \hbar \mathbf k \psi\_{n \mathbf k} - i \hbar e^{i \mathbf k \cdot \mathbf r} \nabla u\_{n \mathbf k}(\mathbf r)
\end{align}

when using Bloch's theorem. This is not just a constant times \\(\psi\_{n\mathbf k}\\), so \\(\psi\_{n\mathbf k}\\) is **not a momentum eigenstate** as this is the form that we would expect from an eigenvalue equation.

-   **However**, if \\(u\_{n\mathbf k} (\mathbf r) = \text{constant}\\) the derivative becomes 0 and it will be an eigenstate. So, for non constant potentials, we have:

    \\[\hat p \psi\_{n \mathbf k} \neq \hbar \mathbf k \psi\_{n \mathbf k}\\]
-   We emphasize it as a momentum as in some ways \\(\hbar \mathbf k\\) is a natural extension of \\(\mathbf p\\) in the case of a periodic potential (but it is not a momentum as we have just shown now).
-   Until the semiclassical model, view \\(\mathbf k\\) as a quantum number characteristic of the translational symmetry of a periodic potential, just as the momentum \\(\mathbf p\\) is a quantum number characteristic of the fuller translational symmetry of free space.

**1st Brillouin Zone**

-   Any \\(\mathbf k^\prime\\) not in the first Brillouin zone can be written as \\(\mathbf k^\prime = \mathbf k + \mathbf K\\) where \\(\mathbf K\\) is a RLV and \\(\mathbf k\\) does lie in the first zone.

**Band structure**

-   The eigenstates and eigenvalues are also periodic functions of \\(\mathbf k\\) in the reciprocal lattice:

\begin{align\*}
\psi\_{n, \mathbf k + \mathbf K} &= \psi\_{n \mathbf k}(\mathbf r) \\\\
E\_{n, \mathbf k + \mathbf K} &= E\_{n \mathbf k}
\end{align\*}

-   This leads to a description of the energy levels of an electron in a periodic potential in terms of a family of continuous functions \\(E\_{n, \mathbf k}\\) each with the periodicity of the reciprocal lattice. The information contained in these functions is referred top as the **band structure of the solid.**
-   For each \\(n\\), the set of levels specifiek by \\(E\_n(\mathbf k)\\) is called an **energy band**.
-   **Mean velocity of an electron in Bloch state** \\(\mathbf k\\): an electron in a level specified by a band index \\(n\\) and wave vector \\(E\_n(\mathbf k)\\) has a nonvanishing mean velocity given by
    \\[\mathbf v\_n(\mathbf k) = \frac{1}{\hbar} \nabla\_{\mathbf k} E\_n(\mathbf k) \\]
    -   There are _stationary/time-independent_ levels for an electron in a periodic potential in spite of the interaction of the electron with the fixed lattice of ions. It moves forever without any degradation of its mean velocity.
    -   This is in contrast to Drude's idea that collisions were simply encounters between electron and a static ion.

**On Fermi surfaces**

-   The number of states in a band is equal to the number of primitive cells in the crystal. Each level can accommodate two electrons. A configuration with a band gap can then arise **only if** the number of electrons per primitive cell is even (thought it need not arise).


## 9. Electrons in a Weak Periodic Potential <span class="tag"><span class="ATTACH">ATTACH</span></span> {#9-dot-electrons-in-a-weak-periodic-potential}

{{< figure src="/ox-hugo/_20240106_131040screenshot.png" >}}

-   The repeated-zone scheme emphasizes that a particular state at \\(k\\) can be described by any wave vector differing from \\(k\\) by a reciprocal lattice vector. It is however highly redundant: the same level is shown many times for all equivalent wave vectors \\(k, k \pm K, k \pm 2K, \dots\\).
-   The mathematical separation of the two bands is reflected in a physical separation.
    -   When the action of an external field changes an electron's wave vector, the presence of the energy gap **requires** that upon crossing the Bragg plane, the electron must emerge in a level whose energy remains in the original branch of \\(E(\mathbf k)\\).


## 12. The Semiclassical Model of Electron Dynamics <span class="tag"><span class="ATTACH">ATTACH</span></span> {#12-dot-the-semiclassical-model-of-electron-dynamics}

> An intuitive understanding of the dynamical significance of the wave vector k can only be acquired when one considers the response of Bloch electrons to externally applied electromagnetic fields (Chapter 12). Only then does its full resemblance to p/h emerge.

<!--quoteend-->

> Perhaps a suitable attitude to take is this: If there were no underlying microscopic quantum theory ofelectrons in solids, one could still imagine a semiclassical mechanics (guessed by some late nineteenth-century Newton of crystalline spaces) that was brilliantly confirmed by its account of observed electronic behavior, just as classical mechanics was confirmed by its accounting for planetary motion, and only very much later given a more fundamental derivation as a limiting form of quantum mechanics.

{{< figure src="/ox-hugo/_20240106_131946screenshot.png" >}}

-   We can't think of collisions occuring with static ions as a mechanism to degrade the velocity, because Bloch electrons have been shown to take account of the fixed periodic array of ions and still have a nonvanishing velocity.
-   This can be understood as a manifestation of the wave nature of electrons: in a periodic array of scatterers, a wave can propagate without attenuation because of coherent constructive interference of the scattered waves.

**Semiclassical model**

-   The semiclassical model predicts how, in the absence of collisions, \\(\mathbf r\\) and \\(\mathbf k\\) of each electron evolve in the presence of externally applied electric and magnetic fields.
    -   An electron having both a position and wave vector is referred to as a wave packet.
-   This prediction will be based **entirely** on our knowledge of the band structure (the function \\(E\_n(\mathbf k)\\)) and upon no other information about the periodic potential of the ions.
-   The rate of change of an electron's momentum is given by the total force on the electron. The rate of change of an electron's **crystal** momentum is given by the next equation in which forces are exerted only by the external fields and not by the periodic field of the lattice.
