# Who's Afraid of the Church of the Larger Hilbert Space?

Length: *1465 words, approximately 6 minutes*

Status: *Draft*

What, exactly, is a measurement?  This is a seemly innocuous question.  Obviously,
you get your tape measure out, wrap it round you waist, and count off how many inches
you've added to your girth over the holiday season.  But in the world of quantum theory,
the theory that seems to be the operating system of our universe, when exactly a 
measurement occurs and it exactly what it is only very oddly defined. For our waist lines this could be a benefit, but as a scientific theory this is quite disconcerting.

There are many ways to present quantum theory. For example, one approach is to
start with wave functions and add the Schrodinger wave equation which governs the
time evolution of these wave functions. An equally valid starting point 
emphasizes linear algebra (which my friend David Hogg likes to remind 
us is [not an algebra](https://twitter.com/davidwhogg/status/1440105703692247042)).
But one of the clearest ways to get at the basics of quantum theory is through a simple
set of a basic axioms.  Probably my favorite version of these are from John Preskill's 
[lecture notes](http://theory.caltech.edu/~preskill/ph219/chap2_15.pdf). Here are 
rough paraphrases of these axioms, without the measurement axiom.
* **Axiom 1** States are rays in Hilbert space.
* **Axiom 2** Observables are self-adjoint operators.
* **Axiom 4** Dynamics of a state, evolution in time, is a unitary operator.
* **Axiom 5** When you take two systems and form a composite, the state space of
the composite system is the tensor product of the two system's Hilbert spaces.

The missing axiom here is **Axiom 3** which describes measurement. Here it is in full:
> A measurement is a process in which information about the state of a physical
> system is acquired by an observer. In quantum mechanics, the measurement of an 
> observable $\bf A$ prepares and eigenstate of $\bf A$, and the observer learns
> the value of the corresponding eigenvalue. If the quantum state just prior to
> the measurement is $|\psi\rangle$, then the outcome $a_n$ is obtained with
> *a priori probability* $${\rm Prob}(a_n) = ||{\bf E}_n|\psi\rangle||^2 = \langle \psi |{\bf E}_n |\psi \rangle$$
> (ed note: here ${\bf E}_n$ is the projector onto the eigenvectors, of $\bf A$ labeled,
> by the outcome $n$.) if the outcome $a_n$ is attained, then the (normalized) quantum 
> state just after the measurement is 
> $$\frac{{\bf E}_n|\psi\rangle}{||{\bf E}_n |\psi\rangle ||}$$

This axiom takes up more length on the page than the other axioms, but it also
throws out a lot of terminology.  First of all there is an observer.  What is that?
And it describes measurement as a process, but what makes it a different process than
the normal unitary dynamics of axiom 4?  All of this should make you a little uncomfortable.  The great thing about quantum theory, however, is that even with these
sort of ambiguities, there has always been a way to just make them work, when you 
hit the real world of experiments.

For the experts in this area, I'm sure what I am saying is naive, but
I believe even they will have a feeling of encountering something that is somehow
mysterious when encountering the measurement axiom. The measurement axiom is somehow
how things become, how they transition into something more permanent, existing as
*records* of *what happened*.

There are a group of physicists, loosely we would call them quantum foundations 
researchers, who spend a lot of time thinking hard about quantum theory and what it
means or what it tells us or how to live with quantum theory and not go insane.  What 
is a measurement and how does it mesh with the other axioms of quantum theory is one 
of the areas in which quantum founds folk have spent a lot of time investigating. I've 
been lucky enough to work a bit on this back in my 
[younger days](https://arxiv.org/abs/quant-ph/0304076). In my spare time, I still think 
a lot about this.  Nothing says crank like being a software engineer thinking about the 
foundations of quantum theory! People whose papers I will read whenever they come out 
include [Matthew Leifer](https://scirate.com/search?q=au:Leifer_M+in:quant-ph), 
[Robert Spekkens](https://scirate.com/search?utf8=%E2%9C%93&q=au%3ASpekkens_R+#results), 
[Chris Fuchs](https://scirate.com/search?q=au:Fuchs_C), and more.  Down those links is a 
lot of head scratching and some well earned moments of clarity.

In reading that literature, and thinking about some of these problems myself, one 
thing that strikes me is that there is a good deal of work in that arena which
works very directly with a sort of variation on the axiom-ized version of quantum
theory. In this approach, one considers preparations of states, evolutions, and
measurements as separate processes (sometimes measurement and preparation are 
combined).  In this approach one thinks a lot about the measurement results, and 
how they correspond to the reality or unreality of the quantum state, contextuality,
and quantum non-locality.  There is a lot to be said for this approach.  It leads 
to Bell inequalities, Kochen-Specker experiments on contextuality, and results
about the epistimic or non-epistimic nature of quantum theory.  But it does make
a particular slight of hand, in that it does make one think about preparation, dynamics, 
and measurement as sort of separate.

Enter religion to the debate. In quantum information there is only one church and that 
church is the  *Church of the Larger Hilbert Space*.  This phrase "Going to the Church 
of the Larger Hilbert Space" was coined by John Smolin to describe a very useful 
tool. In particular it describes going from the system under study to a larger system 
that contains  the original system as a tool for proving things about the original 
system.  This can be done for both quantum states, but also for quantum channels.  And 
it turns out to be an  amazingly useful tool (All hail the Church! Amen.)

For quantum states this tool is used when working with *mixed states*.  A mixed
state is described, unlike in axiom 1 above, by a density matrix.  The interesting
thing about this density matrix is it that it can be *purified*.  That is a 
*mixed state* can be thought of as a pure state in a larger system.  

Connecting back now to those axioms, it strikes me that when one thinks about
preparations,  evolutions, and measurements separately, one has to be able to think
and make sure that your reasoning is robust to the Church of the Larger Hilbert Space.
In particular whatever one is doing for these setups, which delineate into three 
separate processes (though sometimes measurement and preparation are combined), then
one needs to be worried that these in fact are actually working in larger space.
That is, when reasoning about the these as separate objects, one needs to be careful
that these arises from the Church of the Larger Hilbert Space trick.

As a concrete example, consider measurement of a qubit in the computational basis.
One can describe this as the above axiom 3 applied to an observable with different
values for $|0\rangle$ and $|1\rangle$ eigenvectors.  If one is then reasoning
about measurement from within the context of a preparation, unitary, measurement
framework, then one will need to handle this measurement.  But one can also think 
about this measurement as a process in which one attaches another qubit to the system,
initially in the $|0\rangle$ state, and applies a controlled-NOT from the original
qubit to this qubit.  If this second qubit is never touched again, then the first system
will behave as if it was measured.  By thinking about the density matrix after the
measurement as a purification in a larger pure state, the Church trick, one has
transformed the original setup into something that doesn't really contain measurement
(assuming here that the measurement outcome isn't really used, just to keep things
simple).  So one really then needs to explain what your theory says about the
just unitary evolution part of the setup and give this measurement result.

And this, I think, is an important issue which those trying to explain quantum 
theory or see deeper into its interpretation have to overcome. They need to be
able to deal with the case of everything being unitary (or possibly everything
being a quantum operation). 

So who's afraid of the Church of the Larger Hilbert Space? I think everyone who 
wants to think about quantum theory in a theory that separates preparation, 
dynamics, and measurement and studies them separately, should be scared.  One
needs to respect the Church, that we can get much of what we do by working in
a larger state space.  And reasoning about foundations should be wary of this,
maybe even going so far as to say that we should not make these separations.
Down that path we may find the many-world interpretation of quantum theory,
but thats another discussion of religion for another day.

-*dmb*
