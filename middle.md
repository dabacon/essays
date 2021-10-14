# Quantum Computing's Middle Way

Length: *~2000 words, approximately 8 minutes*

Status: *Draft*

The crazy thing about computing is that there are so many ways to do it.
One way is to use transistors, like our modern CPUs, but systems as diverse 
as strands of DNA, molecules, and 
[Tinker Toys](http://ix.cs.uoregon.edu/~michaelh/110/ttoy/ttoy.html)
can be made to compute.  Of course, you don't necessarily want to build a 
computer out of Tinker Toys. The costs, power consumption, and mean time between
failure make such a computer fairly useless as a *technology*.  As a toy, 
of course, it is fantastic.

Back when I was a graduate student (1997 to 2001, Go Bears!), it seemed
like every week there was a paper published in Physical Review Letters showing
that "hey my favorite quantum system can be made into a quantum computer."
There are also many ways to quantum compute!  But so far, what has been
much harder is to find a quantum computing *technology*.

The primary reason for this is that our quantum technologies seem to
be far more suspectable to the effects of noise and imprecise control.
This is not a fundamental reason.  We have known since the mid 1990s that
there is a way to take systems that are noisy and which we cannot precisely
control, and put them together into a machine where these issues are of
a magnitude that they don't matter anymore (for a sufficient definition of
not mattering).  This is the done using the theory of fault-tolerant 
quantum computing, a prescription for the gadgetry necessary to reduce 
errors and increase control.  Long may fault-tolerance live, and
far may she sail!

As far as technologies, most people segment quantum hardware by the different 
substrates out of which one can build a quantum computer, superconducting 
circuits, ions, electron or nuclear spins, photons, and more.  But there is an 
more  fundamental schism in quantum computing.  This is between the 
*brute forcers* and the *naturalists*.

The brute force approach is essentially the idea that we already have our
qubit substrate defined, and it is "just" a matter of scaling these up.
With some amount of increase in gate fidelities and qubit lifetimes, brute
force approaches will eventually execute fault-tolerant protocols and this
will be the point where quantum computers become a technology.  Brute 
forcers don't necessary believe that there won't be necessary improvements 
and innovations to get to the fault-tolerant scaling regime (or at least 
the non-hype-saturated brute forcers don't believe this).  But they do believe 
that existing qubits or slight variations of these will be the
qubits executing in fault-tolerant protocols of a future quantum 
computing technology.

The naturalist approach, on the other hand believes that not all qubits 
are created equal and that it is possible for there to exist qubits 
that are fault-tolerant without having to actively engineer 
fault-tolerant protocols.  In analogy with classical computing 
where transistors are fault-tolerant because of the physics of how 
they work, naturalists think that finding the correct fault-tolerant 
substrate is the way quantum computing will be a technology. The main 
approach here is that of topological quantum computing, where qubits
exist as a global protected state in a many-body quantum system. In 
this approach the properties of the materials out of which one builds 
the quantum computer are the key ingredient (just as semiconductors 
were key to the transistor).

Today, the brute force approach is ascendent, most of the companies that
are trying to scale up quantum computing are on a path to brute force
their way to a technology.  The major exception to this is Microsoft's
decade plus effort in topological quantum computing.  

It is uncontroversial to say that the naturalist approach, so far, 
has not been successful.  There is currently no (publicly) known 
working topological qubits that have done even small computations.
But is also pretty obvious that if there was a qubit that had the 
properties predicted for topological quantum computing, that 
technology would leap to the front of the pack for quantum computing 
technologies.  Which is not to say that it would  obviously leapfrog 
the brute force approaches, as there are many complexities to what 
makes a technology work than just the basic properties of the 
topological quantum computer (cost, yield, power, etc.  All the stuff 
companies leave off in their glossy investor presentations.)

Given this state of affairs, where the brute force approach has 
made tremendous progress in controlling individual and coupled quantum 
systems, and yet we know that there should exist physical systems that 
are better qubits, one question to ask is whether there is some way in 
which these two can be brought together.  Is there a quantum middle way?  

Of course no essay asks a question like this in the middle of the essay
without believing that the answer is "yes".  What would this middle
way look like?

To answer this it is useful to understand the two major advances 
presented by topological quantum computing. The first of these is that
there exist realistic physical models whose ground states are quantum 
error correcting code states, and these models also have an energy gap 
between these states and their excited  states. This means, roughly, 
that if you could build a system that matches this physical model, 
at a temperature well below the energy gap, the  quantum system can
be frozen into this ground state. Any quantum error will need to 
overcome this energetic barrier to create an error. In  addition 
any small perturbative quantum error, even when spread out 
over the entire system, does not change the properties of the ground 
state.  This is the first lesson of topological quantum computing:
physical systems whose energy eigenstates are quantum error correcting
code states should be robust to errors.

The second part of topological quantum computing that makes them
natural quantum computing systems, which is I think less widely 
appreciated, is the way in which one computes on these systems.
If the information is encoded into the ground states, and any small
local operation cannot disturb this information, how does one get
at this information.  There are actually a variety of answers to 
this question, but one of the important facts about these methods is
that they "set their own clock".

In the brute force approach, a common thread (though there are exceptions)
is that the qubits are energy levels of a system, and therefore the
qubit is constantly undergoing evolution which phases between
these two energy levels.  This means that in order to precisely control
this qubit, you really need to be precisely keeping track of this
phase.  This is very challenging, and effectively means you need 
something like a clock to keep track of this.  One can contrast
this with classical transistors.  There are rising and falling signal 
triggers the computations. CPUs have a clock which is distributed 
to its computing elements and the rising and falling of that clock
triggers the computation.  (Side note: an additional difference being that 
in the classical computing world, the data moves across the device as the
computation is enacted, whereas in quantum computing we most often
bring the control to qubits fixed in space.)

What topological quantum computing offers is something similar. In
one form of how to compute on topological quantum computers, one 
can apply localized fields to a part of the system, and then then 
by adiabatically moving these fields around, one can enact a gate.
The topological part of this is that the gate that is implemented 
only depends on the space-time braid that moving such localized
objects around induces.  To do a gate, one completes one of these
moves.  In this sense, these systems "set their own clock", the 
rate of their gates is set by the rate of doing these braiding
actions.  There are a variety of variations on this theme, for
example using only measurements to enact the topological quantum
computing, but similarly these allow one to not have to precisely
track phase of one's qubits.

One of the challenges of the topological approach to quantum computing
is that while it is known that some models of many-body quantum
physics give rise to the desired state of matter, it is very hard
to go from this model to the real world.  Condensed matter systems
are notoriously messy: they often have defects and disorder that
makes the system you are trying to build not exactly match the model
you want.  It remains a real challenge to go from the theoretical
model to experimental physical systems that support the desired 
topological phase of matter.

Contrasting with this, we have the brute force approach, which has
shown tremendous ability to build qubits and perform small quantum
algorithms on them. We know a lot now about how to engineer coherent
quantum systems.  The middle way then says, well can we take that
knowledge of engineering quantum systems, and turn it into the 
part that is hard for the topological systems, engineering the 
physical model that yields a topological model?  Can we build systems
that have energy eigenstates that are error correcting codes, and
which we can manipulate using methods that set their own clock?  Maybe
not gigantic many-body materials, but out of our current systems that
admit precise control?

Disclosure. I have been thinking about the middle way for a very long
time.  A full two lifetimes ago, I wrote a paper with Ken Brown and
K. Birgitta Whaley (my advisor) called "Supercoherent Quantum Bits".
Damn Physical Review Letters made us change the title to 
[Coherence-Preserving Quantum Bits](https://arxiv.org/abs/quant-ph/0012018)
(grumble grumble something about not inventing new words in titles.)
The basic idea of that paper is that there is a four qubit system,
that when you turn on exchange interactions between all four qubits
has a ground state that is two-fold degenerate, and which is also
a single qubit error detecting code. That latter code property means
that single qubit errors necessarily require energy in order to 
excite out of the ground state, much in the same way that
topological quantum systems do with many many more qubits.  One 
interesting challenge of this approach is that one of the important
properties of topological quantum computing is that there is a 
constant energy gap, regardless of system size.  But there is a 
lot of wiggle room here, if we make a 9 qubit system, and have
strong enough interactions, does this offer a gap that is large
enough for protection?

When we were thinking about supercoherent qubits (and related ideas in
compass model qubits), one thing we really didn't know was how to 
manipulate these systems in a manner similar to how the topological
quantum computers set their own clock. But one day I was riding on a
ski lift with Steve Flammia and Carl Caves, and I realized that 
I had a big problem.  I wasn't getting papers rejected.  (Biggest
humble brag ever here, could not resist.) Was this an indication that
I was playing it too safe?  So Steve agreed that we would work together
and make sure we got papers that were rejected. This lead to
[Adiabatic Gate Teleportation](https://arxiv.org/abs/0905.0901),
[Adiabatic Cluter State Quantum Computing](https://arxiv.org/abs/0912.2098),
and [Adiabatic Topological Quantum Computing](https://arxiv.org/abs/1406.2690)
(with C. Cesare, A. Landahl and A. Neels).  And yes some of these
got rejected!  For me it became clear that there were ways to 
build adiabatic protocols that yield gate based actions, in a manner 
very similar to that of the topological quantum computing. 

There are a small number of people thinking about this sort of
approach to quantum computing.  It's certainly not mainstream, yet
I think it is a viable approach.  If I was Bill Gates rich, I'd fund
it.  Ok, even if I was minor celebrity rich, I'd fund it.

The middle way is a Buddhist term with a couple of meanings.  One is 
to describe a path that steers between a lifestyle of abstinence of 
sensual pleasure and a lifestyle of sensual overindulgence.  The other 
is to describe a view between eternalism, the idea that there is an
eternal self, and annihilationism, the idea that the self is utterly
annihilated at death.  (Apologies for the condensation of a much more
nuanced and complicated concept into two short paragraphs.)  I will
leave it as an exercise to the reader to map each of these to the
brute force and naturalist factions, but am hopeful that some 
attention can be given to the quantum middle way.
