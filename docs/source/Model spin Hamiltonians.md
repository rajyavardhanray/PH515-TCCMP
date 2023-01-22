Model Hamiltonians
=======================================


We begin our journey with an introduction to model Hamiltonians. You are well-aware
that, strictly speaking, Hamiltonian represents all the knowledge we have about the 
system and involves all the degrees of freedom of the system of interest. In general, 
it involves a kinetic energy part and a potential energy (interaction) part.

However, we may not always be interested in the physics of all the degrees of freedom(DOFs). 
In fact, in many cases, the physics of different DOFs may show up at different energies, 
implying that different sources of perturbations (of different energies) will be required 
to probe these DOFs. In such cases, we are ofter interested in an 
**effective low-energy model** which involved only selected DOFs which participate 
in the low-energy excitations in response to external perturbations/probes.

## I. Model Hamiltonians with spin degrees of freedom. 

The relevant (low-energy) degrees of freedom are spins. However, this does not mean that charges are not present in the system. It only implies that the low-energy excitations (accessible quite easily in experiments) involve only the spins --- the charge degree of freedom is quenched. In physical systems (which contain both charge and spin) the charge excitations will require large energy excitations. In specific cases, one could, in-principle also probe them. However, the kind of systems we have in mind do exhibit any charge related phenomena (excitations would be somewhat precise) at low energies. Even then, one could, in principle, study electron-magnon interactions in such systems once an appropriate Hamiltonian involving both these degrees of freedom (*e.g.* the Hubbard model and/or the $t-J$ model discussed below) is available.   

Naturally, we are going to deal with cases where each atom has a partially filled valence orbital, thus, a finite spin moment. In the following, however, these spin moments will be assumed to be localized (pinned) to the sites on a lattice with proper crystallographic symmetry of the system. One should bear in mind that this is not the only types of magnetic/spin Hamiltonians. An important example would be the case of [*itinerant/band ferromagnets*](https://web.northeastern.edu/nanomagnetism/wp-content/uploads/2020/06/P-Band-Theory-of-Magnetism-in-Metals.pdf) [also look up [this discussion](https://physics.stackexchange.com/questions/479486/which-mechanism-causes-ferromagnetism-in-iron) ], where the resulting bulk magnetic moment arises due to the [Stoner instability criteria](https://en.wikipedia.org/wiki/Stoner_criterion). 

### A. Heisenberg model

One of the mostly used Hamiltonian capturing interaction between spins is the Heisenberg Hamiltonian:

$$
\begin{equation}
\mathcal{H}_{\rm Heis} = -J \sum_{\langle ij\rangle} {\bf S}_i \cdot {\bf S}_j\,,
\end{equation}
$$

where ${\bf S}_i$ represents spins (quantum spin operators to be precise) at site i, and $J$ represents the exchange coupling between the spins at nearest neighbor (NN) sites $i$ and $j$ (denoted by symbol $\langle ij\rangle$. 

    
In the present convention, $J \ge 0$ would imply that the energy $E = <\mathcal{H}_{\rm Heis}>$ will be minimized if the spin ${\bf S}_i$ and ${\bf S}_j$ align parallel to each other. Consequently, $J < 0$, would imply antiparallel spin alignments. These spin arrangements are, respectivey, called the ferromangetic and antiferromagnetic states.

**From quantum to classical spins.**   It turns out that the quantum corrections in the leading order scale $\propto 1/S$ [look up: [large S expansion](http://qpt.physics.harvard.edu/p52.pdf) ]. It is interesting to note that in general, there exists large $N$ expansion as well in both cond-mat and high-energy, where $N$ represents the degree of freedom. Could one similarly carry out a large-dimensional expansion, I wonder $\ldots$]. 

Therefore, if the magnitude of the spins are large, the quantum fluctuations are expected to be small. For such cases, the spin operators can be approximated to behave like classical operators --- vectors. Why the classical objects would behave like vectors can be understood by their interaction with the magnetic field (Zeemann coupling),

$$
\begin{equation}
\mathcal{H}_{\rm Zeeman} = {\bf B}\cdot {\bf S} = \mu {\bf H}\cdot {\bf S}
\end{equation}
$$

Being vectors, the classical spins can in principle point to any direction in the space (modeled by angles $\theta$ and $\phi$), and therefore, must lie on a sphere of radius $S$. For a detailed discussion on the relation between quantum and classical spins, perhaps it is instructive to learn about the [Bloch sphere](https://en.wikipedia.org/wiki/Bloch_sphere).

As a result, we have:

$$
\begin{eqnarray}
S_x &=& S \cos(\phi)\sin(\theta) \,, \nonumber \\
S_y &=& S \sin(\phi)\sin(\theta) \,, \nonumber \\
S_z &=& S \cos(\theta)\,. \\
\end{eqnarray}
$$

#### A1. Quantum limit


In general, experience suggests that the classical Heisenberg Hamiltonian captures the essential physics of the underlying spin system for $S \geq 1$. However, this is somewhat sensitive to the dimensionality and coordination number of the system/lattice and also on the nature of the spin interactions. 



For example, the quantum fluctuations in lower dimensions is larger than in three-dimensions (3D). ${\color{red}{\rm Why?}}$ 

Additionally, if the system is frustrated (see below), then the classical approximation may turn out to be misleading.




#### A2. SO(3) symmetry and spontaneous symmetry breaking

An interesting and important aspect of the Heisenberg Hamiltonian is the fact that the Hamiltonian is rotationally invariant since it involves dot product of spins. This is referred to as the $ SO(3)$ symmetry of the Heisenberg Hamiltonian. You have already dealt extensively with the matrix representation of the rotation operators. The only thing to remember here is the the $SO(3)$ deals with orthonormal matrices $M$ (rotations) with ${\rm det}(M) = +1$. ($O(3)$ is the collection of orthonormal matrices in 3D, with ${\rm det}(M) = \pm 1$.)

As such, both $O(3)$ and $SO(3)$ form a continuous group, implying that the result of the operations from the set, even successive, belong to the same set. The term *continuous* refers to the fact that infinitesimal rotations are also well-defined.

**Ferromagnets.** An important application of Heisenberg Hamiltonian is the description of ferromagnets (involving ions with valence $3d$ shells). Given the rotational symmetry of the Hamiltonian, one would expect that all the directions are equally likely. However, a ferromagnets has a particular orientation of spins which manifestly breaks the rotational symmetry of the Hamiltonian. In other words, the ground state wavefunction has a lower symmetry than the Hamiltonian. This is achieved via the mechanism of [spontaneous symmetry breaking](https://en.wikipedia.org/wiki/Spontaneous_symmetry_breaking) (more on this, later!).

### B. Ising model

Perhaps the simplest conceptual Hamiltonian is the Ising spin Hamiltonian:

$$
\begin{equation}
\mathcal{H}_{\rm Ising} = -J \sum_{\langle ij \rangle} S_i^z S_j^z\,,
\end{equation}
$$

where $S_i^z = \pm S$ represents the $z$ component of the spins at site i. Note that, in this case, the rotational symmetry is absent in the Hamiltonian. In this case, there exist a natural direction ($z$) for the spin to align. In this sense, these are $S=1/2$ states.


### C. Anisotropic exchange models

**XXZ Model.**
Between the fully rotational symmetric Heisenberg and the symmetry-broken Ising model, one can imagine that there are systems where while the rotational symmetry is broken, all the three ($x,y,z$) components of the spins are still relevant at low energies. Such models are referred to as **anisotropic spin models**. 

One example would the **XXZ model** where the anisotropy is manifested via the exchange couplings:

$$
\begin{equation}
\mathcal{H}_{\rm XXZ} = J[S_i^x S_j^x + S_i^y S_j^y ] + J' S_i^z S_j^z\,.
\end{equation}
$$

The above hamiltonian maps to the Heisenberg model for $J'=J$. One could guess that in the limit of $J'/J >> 1$, this would behave more like the Ising model. ${\color{red}{\text{Any guess on how large should $J'/J$ be to reach the Ising limit?}}}$.

$\hspace{0.1cm}$

**Heisenberg model with single-ion anisotropy**

$$
\begin{equation}
\mathcal{H}_{\rm sia} = - J \sum_{\langle ij \rangle} {\bf S}_i \cdot {\bf S}_j + D\sum_{i} (S_i^z)^2 + E\sum_{i} [(S_i^x)^2 - (S_i^y)^2].
\end{equation}
$$

$D$ and $E$ are the single ion anisotropy terms, respectively, favoring out-of-plane (perpendicular, $z$) and in-plane ($x$,$y$) orientation for the spins. Note that the anisotropy terms are on-site terms as would be expected from their origin (single ion anisotropy). 

${\color{red}{\text{It would be an interesting project to highlight the different between the $XXZ$ and the single-ion anisotropy models}}}$


$\hspace{0.1cm}$

**XY Model.** Note that in all the cases discussed above, the spin is assumed to live in 3D independent of the dimensionality of the lattice (which could be 1D, 2D or 3D). An example of the 2D spin Hamiltonian is the XY model:

$$
\begin{equation}
\mathcal{H}_{\rm XY} = J[S_i^x S_j^x + S_i^y S_j^y ]\,.
\end{equation}
$$

This model shows [Kosterliz-Thouless phase transition](https://www.mit.edu/~levitov/8.334/notes/XYnotes1.pdf), distinct from the other cases. 


### Spin frustration -- geometric and quantum/energetic.

Consider a traingular lattice with localized spin $S$ per site. Each site is coordinated with 6 NN sites. To explain the idea of frustration, it would suffice to consider a simpler traingular plaquette. At the same time, lets us consider **antiferromagnetic** Ising exchange interaction between these spins.

![GeometricFrustration]( https://drive.google.com/uc?export=view&id=19l9bf1PmQgaYpt-vIJOiioUOvka8m_x00I6IMgcQ5uQ )

[GeometricFrustration (image)](https://docs.google.com/drawings/d/19l9bf1PmQgaYpt-vIJOiioUOvka8m_x00I6IMgcQ5uQ/edit?usp=sharing)

In this case, if sites/vertex 1 and 2 are up and down (satisfying the minimum energy criteria), spin at the vertex 3 cannot simultaneouly satisfy the AF exchange interaction with sites 1 and 2. This would be an example of **geometric frustration**. It arises due to underlying lattice. 

${\color{red}{\text{In contrast, one could consider a square lattice and explicitly check that no frustration arises in that case.}}}$

Note however, that I creverly (and quite conveniently) chose the exchange interaction to be Ising type. Alternatively, if one chooses Heisenberg spin interactions, the situation turns out to be quite interesting as well. 

Even in this case, the spin cannot be aligned *completely* parallel or antiparallel to each other. However, ${\color{red}{\text{analytical energy minimization principle would lead to a 120-AF state as the ground state for classical spins}}}$. (This is what MF also results!)

For the 120-AF state, it is possible to place spins at each vertex unambiguously. This state therefore is not frustrated in the same sense as was the case for Ising spins (**Geometric frustration**). However, note that the energy per bond in this case turns out to be: 

$$
\begin{equation}
E_{\rm 120-AF} = JS^2 \cos(2\pi/3) = -JS^2/2\,,
\end{equation}
$$

which is not the minimum possible energy per bond. This would represent the case of **Energetic frustration**, whereby the minimum energy cannot be obtained simultaneously for each bond.

### D. Kitaev exchange Hamiltonian [Extra, for completeness]

At the cross-roads of anisotropy and frustration, lies a very interesting Hamiltonian for $S=1/2$ spins on a honeycomb lattice. Here, the anisotropy is direction dependent. Depending on the bond (coordination number per site is $z=3$), different component of the Ising-like spin interactions exist. This is the celebrated [Kitaev Hamiltonian](https://www.thp.uni-koeln.de/trebst/Lectures/Seminar14/Handout9.pdf) at the forefront of current cond-mat research.

$$
\begin{eqnarray}
\mathcal{H}_{\rm Kitaev} &=& J_{xx} \sum_{xx-{\rm links}} S_i^{x}S_j^{x} \nonumber \\
    &+&J_{yy} \sum_{yy-{\rm links}} S_i^{y}S_j^{y} \nonumber \\
    &+&J_{zz} \sum_{zz-{\rm links}} S_i^{z}S_j^{z} \,.\nonumber
\end{eqnarray}
$$

Note that the bond-directions are simply labeled as $\mu\mu$-links and need not lie along $x$, $y$ or $z$ directions.
