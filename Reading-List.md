*Note: the list of required papers beyond next week is subject to change!*

## Required Reading

### Week 1: EUSolver
Alur, Radhakrishna, Udupa. [Scaling Enumerative Program Synthesis via Divide and Conquer](https://www.seas.upenn.edu/%7Earjunrad/publications/tacas2017.pdf). TACAS'17

**Questions:**
* What does EUSolver use as behavioral constraints? Structural constraint? Search strategy?
* What are the main two pruning/decomposition techniques EUSolver uses to speed up the search? What enables these technique?
* What would be a naive alternative to decision tree learning for synthesizing branch conditions? What are the disadvantages of this alternative?

### Week 2: FlashFill
Gulwani: [Automating string processing in spreadsheets using input-output examples](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/popl11-synthesis.pdf). POPL'11

**Questions:**
* What does FlashFill use as behavioral constraints? Structural constraints? Search strategy?
* Write a program in the FlashFill string expression language that extracts conference years; the program should satisfy the following examples:
    "287 papers submitted to POPL 2018" -> "2018",
    "FM 2012 took place in Oslo" -> "2012"
* Section 3.1 explains why FlashFill restricts its regular expression language. Which lines of the algorithm in Fig. 7 in particular would not be feasible without this restriction?
* Discuss how FlashFill's condition abduction mechanism is different from the one used by EUSolver.

### Week 3: Brahma
Jha, Gulwani, Seshia, Tiwari: [Oracle-guided component-based program synthesis](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/icse10_synthesis.pdf). ICSE’10

* What does Brahma use as behavioral constraints / user interaction mode? Structural constraints? Search strategy?
* Is it possible to specify Brahma's structural constraints in the SyGuS format (as a grammar)? Is yes, show a small example. If no, explain why.
* Consider the following modification of Brahma's synthesis problem: you are given `N` components, but your program is only allowed to use any `K` of them (`K <= N`). How would you modify the SMT encoding in section 4.1 to enforce this restriction?


### Week 4: Sketch
Solar-Lezama: [Program sketching](https://link.springer.com/content/pdf/10.1007%2Fs10009-012-0249-7.pdf). STTT’13

* What does Sketch use as behavioral constraints? Structural constraints? Search strategy?
* Compare structural constraints of Sketch with those in SyGuS (i.e. CFGs) and in Brahma; which of those are more expressive?
* Consider extending the Sketch language with a new command, `abort`, that makes the program fail unconditionally. What should the denotational semantics of this command be, i.e. <a href="https://www.codecogs.com/eqnedit.php?latex=\mathcal{C}[[abort]]^{\tau}\langle&space;\sigma,&space;\Phi\rangle&space;=&space;?" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mathcal{C}[[abort]]^{\tau}\langle&space;\sigma,&space;\Phi\rangle&space;=&space;?" title="\mathcal{C}[[abort]]^{\tau}\langle \sigma, \Phi\rangle = ?" /></a>
* Give an example of a *satisfiable* synthesis constraint that violates the Bounded Observation Hypothesis, and hence cannot be efficiently solved by CEGIS. More precisely, give an example of a formula *Q(c, x)*, where *c*, *x* are bit-vectors of size *n*, such that solving the constraint <a href="https://www.codecogs.com/eqnedit.php?latex=\exists&space;c.\forall&space;x.&space;Q(c,x)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\exists&space;c.\forall&space;x.&space;Q(c,x)" title="\exists c.\forall x. Q(c,x)" /></a> in the worst case would require <a href="https://www.codecogs.com/eqnedit.php?latex=2^n" target="_blank"><img src="https://latex.codecogs.com/gif.latex?2^n" title="2^n" /></a> CEGIS iterations. 

### Week 5: VS3
Srivastava, Gulwani, Foster: [From program verification to program synthesis](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/popl10_synthesis.pdf). POPL'10

### Week 6: Leon
Kneuss, Kuraj, Kuncak, Suter: [Synthesis modulo recursive functions](http://lara.epfl.ch/~kuncak/papers/KneussETAL13SynthesisModuloRecursiveFunctions.pdf). OOPSLA’13

### Week 7: Synquid
Polikarpova, Kuraj, Solar-Lezama: [Program synthesis from Polymorphic Refinement Types](https://cseweb.ucsd.edu/~npolikarpova/publications/pldi16.pdf). PLDI’16

### Week 8: TBD

### Week 9: TBD

## Recommended Reading

### Week 0

Gulwani: [Dimensions in Program Synthesis](https://dl.acm.org/citation.cfm?id=1836091). PPDP'10

### Week 1

Alur, Bodík, Juniwal, Martin, Raghothaman, Seshia, Singh, Solar-Lezama, Torlak, Udupa: [Syntax-guided synthesis](http://sygus.seas.upenn.edu/files/sygus_extended.pdf). FMCAD'13

Albarghouthi, Gulwani, Kincaid: [Recursive Program Synthesis](http://pages.cs.wisc.edu/~aws/papers/cav13a.pdf). CAV'13

Feser, Chaudhuri, Dillig: [Synthesizing Data Structure Transformations from Input-Output Examples](http://www.cs.utexas.edu/~isil/pldi15b.pdf). PLDI 2015

### Week 2

Schufza, Sharma, Aiken: [Stochastic program optimization](https://cacm.acm.org/magazines/2016/2/197428-stochastic-program-optimization/fulltext). CACM’16

Bielik, Raychev, Vechev. [PHOG: Probabilistic Model for Code](http://www.srl.inf.ethz.ch/slides/ICML16_PHOG.pdf). ICML’16

Balog, Gaunt, Brockschmidt, Nowozin, Tarlow. [DeepCoder: Learning to Write Programs](https://arxiv.org/pdf/1611.01989). ICLR'17

Polozov, Gulwani: [FlashMeta: a framework for inductive program synthesis](https://homes.cs.washington.edu/~polozov/papers/oopsla2015-flashmeta.pdf). OOPSLA’15

Wang, Dillig, Singh: [Synthesis of Data Completion Scripts using Finite Tree Automata](http://www.cs.utexas.edu/~isil/dace.pdf). OOPSLA'17

### Week 3

Nieuwenhuis, Oliveras, Tinelli: [Solving SAT and SAT Modulo Theories: From an abstract Davis--Putnam--Logemann--Loveland procedure to DPLL(T)](https://dl.acm.org/citation.cfm?id=1217859). JACM'06

Gulwani, Jha, Tiwari, Venkatesan: [Synthesis of loop-free programs](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/pldi11-loopfree-synthesis.pdf). PLDI’11

### Week 4

Torlak, Bodik: [Growing Solver-Aided Languages with ROSETTE](https://homes.cs.washington.edu/~emina/pubs/rosette.onward13.pdf). Onward!’13

### Week 5

Qiu, Solar-Lezama: [Natural Synthesis of Provably-Correct Data-Structure Manipulations](https://engineering.purdue.edu/~xqiu/natural-synthesis.pdf). OOPSLA'17

### Week 6

Manna, Waldinger: [A Deductive Approach to Program Synthesis](https://pdfs.semanticscholar.org/ceb3/163c56465fda5fef591d0ff0a6c7f434a04d.pdf). TOPLAS'80

Itzhaky, Singh, Solar-Lezama, Yessenov, Lu, Leiserson, Chowdhury: [Deriving Divide-and-Conquer Dynamic Programming Algorithms Using Solver-Aided Transformations](http://people.csail.mit.edu/shachari/dl/oopsla2016.pdf). OOPSLA'16

### Week 7

Osera, Zdancewic: [Type-and-example-directed program synthesis](http://www.cis.upenn.edu/~stevez/papers/OZ15.pdf). PLDI'15

### Week 8

TBD

### Week 9

TBD