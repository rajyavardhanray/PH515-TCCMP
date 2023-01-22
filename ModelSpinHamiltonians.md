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

# I. Model Hamiltonians with spin degrees of freedom. 

The relevant (low-energy) degrees of freedom are spins. However, this does not mean that charges are not present in the system. It only implies that the low-energy excitations (accessible quite easily in experiments) involve only the spins --- the charge degree of freedom is quenched. In physical systems (which contain both charge and spin) the charge excitations will require large energy excitations. In specific cases, one could, in-principle also probe them. However, the kind of systems we have in mind do exhibit any charge related phenomena (excitations would be somewhat precise) at low energies. Even then, one could, in principle, study electron-magnon interactions in such systems once an appropriate Hamiltonian involving both these degrees of freedom (*e.g.* the Hubbard model and/or the $t-J$ model discussed below) is available.   

Naturally, we are going to deal with cases where each atom has a partially filled valence orbital, thus, a finite spin moment. In the following, however, these spin moments will be assumed to be localized (pinned) to the sites on a lattice with proper crystallographic symmetry of the system. One should bear in mind that this is not the only types of magnetic/spin Hamiltonians. An important example would be the case of [*itinerant/band ferromagnets*](https://web.northeastern.edu/nanomagnetism/wp-content/uploads/2020/06/P-Band-Theory-of-Magnetism-in-Metals.pdf) [also look up [this discussion](https://physics.stackexchange.com/questions/479486/which-mechanism-causes-ferromagnetism-in-iron) ], where the resulting bulk magnetic moment arises due to the [Stoner instability criteria](https://en.wikipedia.org/wiki/Stoner_criterion). 

## A. Heisenberg model

One of the mostly used Hamiltonian capturing interaction between spins is the Heisenberg Hamiltonian:

\begin{equation}
\mathcal{H}_{\rm Heis} = -J \sum_{<ij>} {\bf S}_i \cdot {\bf S}_j\,,
\end{equation}
where ${\bf S}_i$ represents spins (quantum spin operators to be precise) at site i, and $J$ represents the exchange coupling between the spins at nearest neighbor (NN) sites $i$ and $j$ (denoted by symbol $<ij>$. 

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
