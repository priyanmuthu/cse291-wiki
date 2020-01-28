*Note: the list of required papers beyond next week is subject to change!*

## Required Reading

### Week 2: EUSolver
Rajeev Alur, Arjun Radhakrishna, Abhishek Udupa: [Scaling Enumerative Program Synthesis via Divide and Conquer](https://arjunradhakrishna.github.io/publications/tacas2017.pdf). TACAS'17

**Questions:**
* What does EUSolver use as behavioral constraints? Structural constraint? Search strategy?
* What are the main two pruning/decomposition techniques EUSolver uses to speed up the search? What enables these techniques?
* What would a naive alternative to decision tree learning be for synthesizing branch conditions? What are the disadvantages of this alternative?

### Week 3: Euphony

Woosuk Lee, Kihong Heo, Rajeev Alur, Mayur Naik: [Accelerating Search-Based Program Synthesis usingLearned Probabilistic Models](https://www.cis.upenn.edu/~alur/PLDI18.pdf). PLDI'18

**Questions:**
* What does Euphony use as behavioral constraints? Structural constraint? Search strategy? How are they different from EUSolver?

* Consider Fig 2b, where the synthesizer is unrolling the sentential form `Rep(x,"-",S)`. When the search is guided by a PHOG, it considers the weighted productions shown in Fig 2a (top). What would these productions look like if we replaced the PHOG with a PCGF? With 3-grams? Do you think these other probabilistic models would work as well as a PHOG?

* Consider Example 3.2. Explain in English the intuitive meaning of `h(S) = 0.1` and why it is the case.

* Consider Theorem 3.7. Give an example of sentential forms `n_i`, `n_j` and set of points `pts` such that `n_i` and `n_j` are equivalent on `pts` but not weakly equivalent.

### Week 4: BlinkFill

Rishabh Singh: [BlinkFill: Semisupervised Programming By Example for Syntactic String Transformations](http://www.vldb.org/pvldb/vol9/p816-singh.pdf). VLDB'16

**Questions:**
* What does BlinkFill use as behavioral constraints? Structural constraints? Search strategy?
* What is the main technical insight of BlinkFill wrt FlashFill?
* Write a program in the BlinkFill DSL (`L_s`) that extracts conference acronyms and years; the program should satisfy the following examples:
    "Programming Language Design and Implementation (PLDI), 2019, Phoenix AZ" -> "PLDI 2019"
    "Principles of Programming Languages (POPL), 2020, New Orleans LA" -> "POPL 2020",    
* As described in the paper, the position expressions of the BlinkFill DSL only support matching a single token from Table 1, e.g. `C`. Could we extend the algorithm to support sequences of tokens, e.g. `C ws $` to match caps followed by whitespace follows by end of string? How would this change the construction and intersection of input data graphs (use Fig 6 as an example).



### Week 5: Brahma

Sumit  Gulwani, Susmit  Jha, Ashish  Tiwari, Ramarathnam  Venkatesan: [Synthesis of loop-free programs](http://www.csl.sri.com/users/tiwari/papers/pldi2011-bitvector.pdf). PLDI'11

**Questions:**
* TBD

### Week 6: Sketch
Armando Solar-Lezama: [Program sketching](https://link.springer.com/content/pdf/10.1007%2Fs10009-012-0249-7.pdf). STTT’13

**Questions:**
* What does Sketch use as behavioral constraints? Structural constraints? Search strategy?
* Compare structural constraints of Sketch with those in SyGuS (i.e. CFGs) and in Brahma; which of those are more expressive?
* Consider extending the Sketch language with a new command, `abort`, that makes the program fail unconditionally. What should the denotational semantics of this command be, i.e. <a href="https://www.codecogs.com/eqnedit.php?latex=\mathcal{C}[[abort]]^{\tau}\langle&space;\sigma,&space;\Phi\rangle&space;=&space;?" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mathcal{C}[[abort]]^{\tau}\langle&space;\sigma,&space;\Phi\rangle&space;=&space;?" title="\mathcal{C}[[abort]]^{\tau}\langle \sigma, \Phi\rangle = ?" /></a>
* Give an example of a *satisfiable* synthesis constraint that violates the Bounded Observation Hypothesis, and hence cannot be efficiently solved by CEGIS. More precisely, give an example of a formula *Q(c, x)*, where *c*, *x* are bit-vectors of size *n*, such that solving the constraint <a href="https://www.codecogs.com/eqnedit.php?latex=\exists&space;c.\forall&space;x.&space;Q(c,x)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\exists&space;c.\forall&space;x.&space;Q(c,x)" title="\exists c.\forall x. Q(c,x)" /></a> in the worst case would require <a href="https://www.codecogs.com/eqnedit.php?latex=2^n" target="_blank"><img src="https://latex.codecogs.com/gif.latex?2^n" title="2^n" /></a> CEGIS iterations. 

### Week 7: Synquid
Nadia Polikarpova, Ivan Kuraj, Armando Solar-Lezama: [Program synthesis from Polymorphic Refinement Types](https://cseweb.ucsd.edu/~npolikarpova/publications/pldi16.pdf). PLDI’16

**Questions:**
* TBD

### Week 8: SuSLik
Nadia Polikarpova, Ilya Sergey: [Structuring the Synthesis of Heap-Manipulating Programs](https://cseweb.ucsd.edu/~npolikarpova/publications/suslik.pdf). POPL’19

**Questions:**
* TBD

### Week 9: TBD

### Week 10: TBD


<!--
### Week 3: FlashFill
Gulwani: [Automating string processing in spreadsheets using input-output examples](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/popl11-synthesis.pdf). POPL'11

**Questions:**
* What does FlashFill use as behavioral constraints? Structural constraints? Search strategy?
* Write a program in the FlashFill string expression language that extracts conference years; the program should satisfy the following examples:
    "287 papers submitted to POPL 2018" -> "2018",
    "FM 2012 took place in Oslo" -> "2012"
* Section 3.1 explains why FlashFill restricts its regular expression language. Which lines of the algorithm in Fig. 7 in particular would not be feasible without this restriction?
* Discuss how FlashFill's condition abduction mechanism is different from the one used by EUSolver.

### Week 4: Brahma
Jha, Gulwani, Seshia, Tiwari: [Oracle-guided component-based program synthesis](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/icse10_synthesis.pdf). ICSE’10

* What does Brahma use as behavioral constraints / user interaction mode? Structural constraints? Search strategy?
* Is it possible to specify Brahma's structural constraints in the SyGuS format (as a grammar)? Is yes, show a small example. If no, explain why.
* Consider the following modification of Brahma's synthesis problem: you are given `N` components, but your program is only allowed to use any `K` of them (`K <= N`). How would you modify the SMT encoding in section 4.1 to enforce this restriction?


### Week 5: Sketch
Solar-Lezama: [Program sketching](https://link.springer.com/content/pdf/10.1007%2Fs10009-012-0249-7.pdf). STTT’13

* What does Sketch use as behavioral constraints? Structural constraints? Search strategy?
* Compare structural constraints of Sketch with those in SyGuS (i.e. CFGs) and in Brahma; which of those are more expressive?
* Consider extending the Sketch language with a new command, `abort`, that makes the program fail unconditionally. What should the denotational semantics of this command be, i.e. <a href="https://www.codecogs.com/eqnedit.php?latex=\mathcal{C}[[abort]]^{\tau}\langle&space;\sigma,&space;\Phi\rangle&space;=&space;?" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mathcal{C}[[abort]]^{\tau}\langle&space;\sigma,&space;\Phi\rangle&space;=&space;?" title="\mathcal{C}[[abort]]^{\tau}\langle \sigma, \Phi\rangle = ?" /></a>
* Give an example of a *satisfiable* synthesis constraint that violates the Bounded Observation Hypothesis, and hence cannot be efficiently solved by CEGIS. More precisely, give an example of a formula *Q(c, x)*, where *c*, *x* are bit-vectors of size *n*, such that solving the constraint <a href="https://www.codecogs.com/eqnedit.php?latex=\exists&space;c.\forall&space;x.&space;Q(c,x)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\exists&space;c.\forall&space;x.&space;Q(c,x)" title="\exists c.\forall x. Q(c,x)" /></a> in the worst case would require <a href="https://www.codecogs.com/eqnedit.php?latex=2^n" target="_blank"><img src="https://latex.codecogs.com/gif.latex?2^n" title="2^n" /></a> CEGIS iterations. 

### Week 6: VS3
Srivastava, Gulwani, Foster: [From program verification to program synthesis](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/popl10_synthesis.pdf). POPL'10

**Questions:**
* What does VS3 use as behavioral constraints? Structural constraint? Search strategy?
* Consider the synthesis condition for the Bresenhams line drawing algorithm shown in Fig 1. If we removed the well-formedness constraint from the synthesis condition, what would be a trivial solution (not corresponding to any real program) that would satisfy this modified constraint?
* Give a loop invariant and a ranking function (termination metric) that are sufficient to prove that the [following program](https://rise4fun.com/Dafny/HmX3) terminates and satisfies its postcondition. The program is written in Dafny syntax; you can use Dafny to verify your solution by pressing the "play" button.

### Week 7: Leon
Kneuss, Kuraj, Kuncak, Suter: [Synthesis modulo recursive functions](http://lara.epfl.ch/~kuncak/papers/KneussETAL13SynthesisModuloRecursiveFunctions.pdf). OOPSLA’13

**Questions:**
* What does Leon use as behavioral constraints? Structural constraint? Search strategy?
* Compare Leon's Symbolic Term Exploration (STE) rule to Sketch. How would you extend STE to generating arbitrary integer constants?
* Compare Leon's Condition Abduction rule to the way conditionals are synthesized in EUSolver and FlashFill.


### Week 8: Synquid
Polikarpova, Kuraj, Solar-Lezama: [Program synthesis from Polymorphic Refinement Types](https://cseweb.ucsd.edu/~npolikarpova/publications/pldi16.pdf). PLDI’16

**Questions:**
* What does Synquid use as behavioral constraints? Structural constraint? Search strategy?
* Find a typo in the Example is Section 3.2 (recently discovered by Tristan!)
* Can Synquid's Round-Trip Type Checking discard the following incomplete terms? Explain how or why not.  
  1. `inc ?? :: {Int | ν = 5}`, where `inc :: x:Int -> {Int | ν = x + 1}`
  1. `duplicate ?? :: {List Int | len ν = 5}`, where `duplicate :: xs:List a -> {List a | len ν = 2*(len xs)}`
  1. `nats ?? :: List Pos`, where `nats :: n:Nat -> {List Nat| len ν = n}`, `Nat = {Int | ν >= 0}`, `Pos = {Int | ν > 0}` 
* Compare Synquid's condition abduction mechanism to the one in Leon.


### Week 9: Lens

Phothilimthana, Thakur, Bodik, Dhurjati: [Scaling Up Superoptimization](https://people.eecs.berkeley.edu/~mangpo/www/papers/lens-asplos16.pdf). ASPLOS’16

**Questions:**

* What is the problem the paper is trying to solve? Why is it important? What are existing approaches to this problem?
* What does Lens use as behavioral constraints? Structural constraints? Search strategy?
* Discuss the three pruning technique of Lens (incremental observational equivalence, bidirectional search, reduced bit width) and compare them with other synthesizers

### Week 10: SQLizer

Yaghmazadeh, Wang, Dillig, Dillig: [SQLizer: Query Synthesis from Natural Language](https://www.cs.utexas.edu/~isil/sqlizer.pdf). OOPSLA'17

**Questions:**

* What is the problem the paper is trying to solve? What are existing approaches to this problem?
* What does SQLizer use as behavioral constraints? Structural constraints? Search strategy?
* Discuss the following three ideas behind SQLizer and relate them to other synthesizers we have seen: 1) sketch generation via semantic parsing 2) quantitative type inhabitation and 3) sketch refinement. 

-->


## Recommended Reading

### Week 1

Gulwani: [Dimensions in Program Synthesis](https://dl.acm.org/citation.cfm?id=1836091). PPDP'10

Alur, Bodík, Juniwal, Martin, Raghothaman, Seshia, Singh, Solar-Lezama, Torlak, Udupa: [Syntax-guided synthesis](http://sygus.seas.upenn.edu/files/sygus_extended.pdf). FMCAD'13

### Week 2


Udupa, Raghavan, Deshmukh, Mador-Haim, Martin, Alur: [TRANSIT: specifying protocols with concolic snippets](http://acg.cis.upenn.edu/papers/pldi13_transit.pdf). PLDI'13

Albarghouthi, Gulwani, Kincaid: [Recursive Program Synthesis](http://pages.cs.wisc.edu/~aws/papers/cav13a.pdf). CAV'13

Phothilimthana, Thakur, Bodik, Dhurjati: [Scaling Up Superoptimization](https://people.eecs.berkeley.edu/~mangpo/www/papers/lens-asplos16.pdf). ASPLOS’16

Smith, Albarghouthi [Program Synthesis with Equivalence Reduction](http://pages.cs.wisc.edu/~aws/papers/vmcai19.pdf). VMCAI'19

Feser, Chaudhuri, Dillig: [Synthesizing Data Structure Transformations from Input-Output Examples](http://www.cs.utexas.edu/~isil/pldi15b.pdf). PLDI 2015

### Week 3

Raychev, Vechev, Yahav. [Code Completion with Statistical Language Models](http://www.cs.technion.ac.il/~yahave/papers/pldi14-statistical.pdf). PLDI'14

Pu, Narasimhan, Solar-Lezama, Barzilay: [sk_p: a neural program corrector for MOOCs](https://dl.acm.org/citation.cfm?id=2989222). SPLASH'16

Balog, Gaunt, Brockschmidt, Nowozin, Tarlow: [DeepCoder: Learning to Write Programs](https://arxiv.org/pdf/1611.01989). ICLR'17

Menon, Tamuz, Gulwani, Lampson, Kalai: [A Machine Learning Framework for Programming by Example](https://www.cse.iitk.ac.in/users/cs365/2014/_papers/menon-tamuz-13-icml_learning-to-program-by-example.pdf). ICML'13

Bielik, Raychev, Vechev. [PHOG: Probabilistic Model for Code](http://www.srl.inf.ethz.ch/slides/ICML16_PHOG.pdf). ICML’16

### Week 4

Schufza, Sharma, Aiken: [Stochastic program optimization](https://cacm.acm.org/magazines/2016/2/197428-stochastic-program-optimization/fulltext). CACM’16

Le, Gulwani: [FlashExtract: a framework for data extraction by examples](https://dl.acm.org/citation.cfm?doid=2594291.2594333). PLDI'14

Polozov, Gulwani: [FlashMeta: a framework for inductive program synthesis](https://homes.cs.washington.edu/~polozov/papers/oopsla2015-flashmeta.pdf). OOPSLA’15

Vijayakumar, Mohta, Polozov, Batra, Jain, Gulwani [Neural-Guided Deductive Search for Real-Time Program Synthesis from Examples](https://www.microsoft.com/en-us/research/uploads/prod/2018/01/main-ml2search.pdf). ICLR'18

Wang, Dillig, Singh: [Program synthesis using abstraction refinement](https://dl.acm.org/citation.cfm?doid=3158151). POPL'18

Gvero, Kuncak, Kuraj, Piskac: [Complete completion using types and weights](http://www.cs.yale.edu/homes/piskac/papers/2013GveroETALCompletion.pdf) PLDI'13

Feng, Martins, Wang, Dillig, Reps: [Component-based synthesis for complex APIs](https://www.cs.utexas.edu/~isil/sypet-popl17.pdf). POPL'17

### Week 5

Nieuwenhuis, Oliveras, Tinelli: [Solving SAT and SAT Modulo Theories: From an abstract Davis--Putnam--Logemann--Loveland procedure to DPLL(T)](https://dl.acm.org/citation.cfm?id=1217859). JACM'06

Jha, Gulwani, Seshia, Tiwari: [Oracle-guided component-based program synthesis](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/icse10_synthesis.pdf). ICSE’10

Feng, Martins, Van Geffen, Dillig, Chaudhuri: [Component-based synthesis of table consolidation and transformation tasks from examples](https://www.cs.rice.edu/~sc40/pubs/pldi17-morpheus.pdf). PLDI'17

Feng, Martins, Bastani, Dillig: [Program synthesis using conflict-driven learning](https://www.cs.utexas.edu/~isil/pldi18-neo.pdf). PLDI'18

### Week 6

Torlak, Bodik: [A Lightweight Symbolic Virtual Machinefor Solver-Aided Host Languages](https://homes.cs.washington.edu/~emina/doc/rosette.pldi14.pdf). PLDI'14

### Week 7

Osera, Zdancewic: [Type-and-example-directed program synthesis](http://www.cis.upenn.edu/~stevez/papers/OZ15.pdf). PLDI'15

Frankle, Osera, Walker, Zdancewic: [Example-directed synthesis: a type-theoretic interpretation](https://www.cs.princeton.edu/~dpw/papers/type-synthesis-popl-2016.pdf). POPL'16

Düdder, Martens, Rehof: [Staged Composition Synthesis](https://link.springer.com/chapter/10.1007%2F978-3-642-54833-8_5). ESOP'14

Scherer, Rémy: [Which simple types have a unique inhabitant?](http://gallium.inria.fr/~scherer/drafts/unique_stlc_sums.pdf). ICFP'15

Knoth, Wang, Polikarpova, Hoffman: [Resource-Guided Program Synthesis](https://cseweb.ucsd.edu/~npolikarpova/publications/pldi19.pdf). PLDI'19

### Week 8

Srivastava, Gulwani, Foster: [From program verification to program synthesis](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/12/popl10_synthesis.pdf). POPL'10

Qiu, Solar-Lezama: [Natural Synthesis of Provably-Correct Data-Structure Manipulations](https://engineering.purdue.edu/~xqiu/natural-synthesis.pdf). OOPSLA'17

Kneuss, Kuraj, Kuncak, Suter: [Synthesis modulo recursive functions](http://lara.epfl.ch/~kuncak/papers/KneussETAL13SynthesisModuloRecursiveFunctions.pdf). OOPSLA’13

Manna, Waldinger: [Synthesis: Dreams → Programs](https://ieeexplore.ieee.org/document/1702636). TSE'79

Manna, Waldinger: [A Deductive Approach to Program Synthesis](https://pdfs.semanticscholar.org/ceb3/163c56465fda5fef591d0ff0a6c7f434a04d.pdf). TOPLAS'80

Reynolds, Deters, Kuncak, Tinelli, Barrett: [Counterexample-Guided Quantifier Instantiation for Synthesis in SMT](lara.epfl.ch/~reynolds/cav15a.pdf). CAV'15


<!--

Torlak, Bodik: [Growing Solver-Aided Languages with ROSETTE](https://homes.cs.washington.edu/~emina/pubs/rosette.onward13.pdf). Onward!’13

Pu, Narasimhan, Solar-Lezama, Barzilay: [sk_p: a neural program corrector for MOOCs](https://dl.acm.org/citation.cfm?id=2989222). SPLASH'16

Itzhaky, Singh, Solar-Lezama, Yessenov, Lu, Leiserson, Chowdhury: [Deriving Divide-and-Conquer Dynamic Programming Algorithms Using Solver-Aided Transformations](http://people.csail.mit.edu/shachari/dl/oopsla2016.pdf). OOPSLA'16



### Week 9

Loncaric, Torlak, Ernst: [Fast synthesis of fast collections](https://homes.cs.washington.edu/~mernst/pubs/collection-synthesis-pldi2016.pdf). PLDI'16

Loncaric, Ernst, Torlak: [Generalized data structure synthesis](https://homes.cs.washington.edu/~mernst/pubs/generalized-synthesis-icse2018.pdf). ICSE'18


### Week 10


Inala, Singh: [WebRelate: integrating web data with spreadsheets using examples](https://dl.acm.org/citation.cfm?doid=3177123.3158090). POPL'17

Kamil, Cheung, Itzhaky, Solar-Lezama [Verified Lifting of Stencil Computations](https://people.csail.mit.edu/asolar/papers/KamilCIS16.pdf). PLDI'16

Gascón, Tiwari, Carmer, Mathur: [Look for the Proof to Find the Program: Decorated-Component-Based Program Synthesis](http://umathur3.web.engr.illinois.edu/papers/synudic-cav2017.pdf), CAV'17

Ellis, Solar-Lezama, Tenenbaum: [Unsupervised Learning by Program Synthesis](https://papers.nips.cc/paper/5785-unsupervised-learning-by-program-synthesis.pdf), NIPS'15

-->
