---
layout: default
title: Home
order: 1
---
<script type="text/javascript"
src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

## Harvard-MIT Homotopy Theory Seminar Summer 2022

### Introduction to Stable and Chromatic Homotopy Theory

<b>Overview:</b>

Chroma is a joint Harvard-MIT summer seminar primarily focused at undergraduates interested in algebraic topology and homotopy theory. If you're an undergraduate or graduate student and are interested in these subjects, fill out the <b>[interest form](interest.html)</b> in the top-right!

This summer, subject to the interests of the participants, we will try to define the stable homotopy category, understand its desirable properties for computational and abstract homotopy theory, and present some results from chromatic homotopy theory. Roughly, we will follow Ravenal's [Nilpotence and Periodicity in Stable Homotopy Theory](https://people.math.rochester.edu/faculty/doug/mybooks/nilpb2020.pdf), but will spend some time reviewing preliminaries to this book. The goal is to develop an intuituion and appreciation for the machinery of stable homotopy theory without getting bogged down by technicalities and computation.

Ideally, familiarity with algebraic topology at the level of Hatcher chapters 1-4 (_sans_ the additional sections) will be helpful, but everyone is welcome to participate!

Tentatively, we will meet once a week on Zoom from early June to late August. Each meeting will consist of a talk given by one of the participants, followed by a question/discussion session. As we're in the early stages of organizing, the dates and times will be shifted to be accomodating of everyone!

<b>What is "Stable Homotopy Theory"?</b> (10 minute version)

The main objects of study in classical algebraic topology are (sufficiently nice, e.g. CW) spaces. The general perspective is that while understanding a space (say, up to homeomorphism) is too hard in general, we _can_ attempt to look at spaces up to homotopy equivalence, which really means going from trying to understand the space $$\text{Maps}(X,Y)$$ to considering homotopy classes of maps, denoted by $$[X,Y]$$ (these are equivalent by the Yoneda lemma).

But even here we are stuck, because in general $$[X,Y]$$ might just be a set. However, if $$X\simeq \Sigma X'$$ (assume everything is based), then we can identify $$[X,Y]$$ with $$\pi_1\text{Maps}(X',Y)$$, which is a group. If $$X$$ is a double suspension, then this becomes an _abelian_ group. Thus, we might want to look at the tower

$$
[X,Y] \xrightarrow{\Sigma} [\Sigma X, \Sigma Y] \xrightarrow{\Sigma} [\Sigma^2 X, \Sigma^2 Y] \xrightarrow{\Sigma} \cdots
$$

as a kind of approximation of $$[X,Y]$$, which is _a priori_ just a set, by things which _do_ have tangible algebraic structures to latch onto. From this point of view, what we _really_ should be studying, as in the thing which we have the best chance of getting a handle on, is the direct limit of this tower, which we call the _stable homotopy classes of maps_ $$[X,Y]_s$$, because these are precisely the maps $$f\colon X\to Y$$ which are invariant under suspension (this is what it means to be "stable"). Our takeaway should be this ethos to what we call "stable homotopy theory":

<p align="center">
	The simplest things are stable things
</p>

Let's take this analogy one step further: why is topology hard and algebra easy? (If this wasn't at least somewhat, then we'd hardly want to study topological spaces via algebraic invariants!) In some sense, it's because $$\mathbf{Ab}$$, the category of abelian groups, is _really_ nice (e.g. it's abelian, closed symmetric monoidal, etc.), while $$\mathbf{Spaces}$$ (or even $$\text{ho}\mathbf{Spaces}$$) aren't, well, anything much in general. By our stated ethos, one way to think about the transition from classical homotopy theory to stable homotopy theory is to think of $$\mathbf{Spaces}$$ not being "nice" as a bug instead of a feature.

To fix this, what we want is a new _category_, $$\mathbf{SHC}$$, called the "stable homotopy category," which is nicer in the sense of giving us more algebraic structure to work with. In the stable category, the morphisms between objects given precisely by the stable classes of maps. The objects are called _spectra_. What are the spectra? We want these to be "spaces which are suspension-invariant," and while there are many ways of actually constructing the category of spectra (the homotopy category of which is precisely $$\mathbf{SHC}$$), a straightforward one is that a spectrum $$E$$ is a sequence of spaces $$E_0, E_1, E_2, \ldots$$ and _structure maps_ $$\Sigma E_n \to E_{n+1}$$.

A good source of examples of spectra is _suspension spectra_, where we start with a space $$X$$, set $$E_n=\Sigma^n X$$, and make the structure maps the identity. Applying this to the 0-sphere, we get the sphere spectrum $$\mathbb{S}$$, the homotopy groups of which (in the stable category) are the stable homotopy groups of the spheres. Another good source of examples are _generalized cohomology theories_ — a result called Brown Representability says that given any spectra $$E$$, the axioms of a spectra are *exactly* what we need for the functor $$E^n(X) = [Y,E_n]$$ to be a generalized cohomology theory; i.e. a functor from $$\text{ho}\mathbf{Spaces}$$ to $$\textbf{Ab}$$ satisfying the Eilenberg-Steenrod axioms (if this reminds you of Eilenberg-Mac Lane spaces, you'll be delighted to know that the sequence $$K(A,0),K(A,1),K(A,2),\ldots $$ forms a spectrum called $$HA$$, which represents ordinary cohomology with $$A$$ coefficients).

Historically, much of the formalism of stable homotopy and spectra arose when Frank Adams was working on the Hopf invariant one problem, but there are echos of this idea throughout classical homotopy theory, such as via the Freudenthal suspension theorem or the aforementioned connection between spectra and generalized cohomology theories. On the other hand, modern perspectives on spectra — which are often phrased in the language of $$\infty$$-categories — treat spectra as the final step in the effort to make working in $$\text{ho}\mathbf{Spaces}$$ more like doing algebra, and approach stable homotopy theory from the lens of "homotopy-theoretic algebra." Our goal for Chroma is to take a middle ground — we'll start by defining the stable category and understanding just what makes it such a nice place to do homotopy theory, and then apply this background to understanding some classical results, such as the nilpotence theorem.

<b>What is "Chromatic Homotopy Theory"?</b>?

\[In Progress — I'll add more!\]

<b>Schedule:</b>

| Date | Speaker | Topic | References |
| ---- | ------- | ----- | ---------- |
| May 27th | | Organizational Meeting | |
| June 2nd | Dora Woodruff | Outline & Main Results <br /> Intro to Spectra | Orange Book Ch. 1 <br /> Barnes-Roitzheim Ch. 1 |
| June 9th | Keita Allen | Categories of Spectra <br /> Monoidal Structures | Barnes-Roitzheim Ch. 2,5,6 |
| June 16th | Jonathan Buchanan | Vector Bundles, Thom spaces <br /> Thom Isomorphism Theorem | Miller Ch. 6,8 |
| June 23rd | Merrick Cai | Bousfield Localization | Barnes-Roitzheim Ch. 7 <br /> Ravenel Ch. 7 |
| Week 5 | TBD | Morava $$K$$-theory <br /> Chromatic Filtration | Ravenel Ch. 1,2 |
| Week 6 | TBD | Formal Group Laws <br /> Morava Stabilizer Groups | Ravenel Ch. 3,4 |
| Week 7 | TBD | The Periodicity Theorem <br /> Chromatic Convergence | Ravenel Ch. 6,8 | 
| Week 8 | TBD | Proof of the Nilpotence Theorem | Ravenel Ch. 8,9 | 
| Week 9 | TBD | Adams Spectral Sequence | TBD |
| Week 10 | TBD | Stable $$\infty$$-Categories <br /> Glimpse of Higher Algebra | (Groth/Gepner?) |

<b>Resources:</b>

A collection of some books, papers, and reference material.

Intros:
* [Algebraic Topology](https://pi.math.cornell.edu/~hatcher/AT/AT.pdf) by Hatcher.
* [Lectures on Algebraic Topology](https://math.mit.edu/~hrm/papers/lectures-905-906.pdf) by Miller.
* [A Concise Course in Algebraic Topology](https://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf) by May.
* [Differential Forms in Algebraic Topology](
https://www.maths.ed.ac.uk/~v1ranick/papers/botttu.pdf) by Bott and Tu.
* [Algebraic Topology](https://www.maths.ed.ac.uk/~v1ranick/papers/diecktop.pdf) by tom Dieck.

Category Theory and Simplicial Stuff:
* [Category Theory in Context](https://math.jhu.edu/~eriehl/context.pdf) by Riehl.
* [More Concise Algebraic Topology](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf) by May (Good model category stuff).
* [The Quillen Model Category of Topological Spaces](https://arxiv.org/pdf/1508.01942.pdf) by Hirschhorn.
* [An Elementary Illustration Introduction to Simplicial Sets](https://arxiv.org/pdf/0809.4221.pdf) by Friedman.
* [Calculus of Fractions and Homotopy Theory](https://web.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf) by Gabriel and Zisman.
* [Homotopical Algebra](https://link.springer.com/book/10.1007/BFb0097438) by Quillen.
* [Simplicial Homotopy Theory](http://dodo.pdmi.ras.ru/~topology/books/goerss-jardine.pdf) by Goerss and Jardine.


Homological Algebra and Spectral Sequences:
* [Introduction to Homological Algebra](https://people.math.rochester.edu/faculty/doug/otherpapers/weibel-hom.pdf) by Weibel.
* [Spectral Sequences in Algebraic Topology](https://pi.math.cornell.edu/~hatcher/AT/ATch5.pdf) by Hatcher.
* Miller's notes above are also very readable.
* [You Could Have Invented Spectral Sequences](https://www.ams.org/notices/200601/fea-chow.pdf) by Chow.
* [A User's Guide to Spectral Sequences](https://www-cambridge-org.ezp-prod1.hul.harvard.edu/core/books/users-guide-to-spectral-sequences/524E3BD5DDD6D387E3C609910142F6E6) by McCleary.


Spectra and Stable Homotopy Theory:
* [Modern Foundations for Stable Homotopy Theory](https://www.math.uchicago.edu/~may/PAPERS/Newfirst.pdf) by Elmendorf, Kriz, Kandell, and May
* [Cohomology Operations and Applications in Homotopy Theory](https://www.maths.ed.ac.uk/~v1ranick/papers/moshtang.pdf) by Mosher and Tangora.
* [Stable Homotopy and Generalized Homology](https://people.math.rochester.edu/faculty/doug/otherpapers/Adams-SHGH.pdf) by Adams.
* [Foundations of Stable Homotopy Theory](https://www.cambridge.org/core/books/foundations-of-stable-homotopy-theory/791C9C413A83AD7094E055E5E818D33B) by Barnes and Roitzheim.
* [Symmetric Spectra](http://www.math.uni-bonn.de/people/schwede/SymSpec.pdf) by Schwede
* [The Stable Homotopy Category](https://people.math.binghamton.edu/malkiewich/stable.pdf) by Malkiewich.
* [The Localization of Spectra with respect to Homology](https://www.sciencedirect.com/science/article/pii/0040938379900181) by Bousfield.

Chromatic Homotopy Theory:
* [(Orange Book) Nilpotence and Periodicity in Stable Homotopy Theory](https://people.math.rochester.edu/faculty/doug/mybooks/nilpb2020.pdf) by Ravenel
* [Math 252x Lecture Notes](https://people.math.harvard.edu/~lurie/252x.html) by Lurie.
* [Math 252y Lecture Notes](https://people.math.harvard.edu/~piotr/252y_notes.pdf) by Pstragowski.
* [Complex Cobordism and Stable Homotopy Groups of Spheres](https://people.math.rochester.edu/faculty/doug/mybooks/ravenel.pdf) by Ravenel.
* [Complex Oriented Cohomology Theories and the Language of Stacks](https://people.math.rochester.edu/faculty/doug/otherpapers/coctalos.pdf) by Hopkins.


<b>Questions:</b>

If you have any questions, feel free to contact any of the organizers!

* Rushil Mallarapu — Harvard — [rushil_mallarapu@college.harvard.edu](mailto:rushil_mallarapu@college.harvard.edu)
* Keita Allen — MIT — [kta@mit.edu](mailto:kta@mit.edu)
* Merrick Cai – MIT – [mercai@mit.edu](mailto:mercai@mit.edu)


