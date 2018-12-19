## 2018

The following course projects have been completed as a result of this class in Fall 2018

### Deductive Synthesis of Layout Constraints From Examples
*Ariel Weingarten, Dylan Lukes, Cora Coleman*

There are more than 5 billion mobile devices in use in the world today. To maintain consistency across screen conformations (size and density) developers define user interfaces using constraint-based layout systems. Constraints are capable of expressing conformation-independent layout behavior but require a great deal of error-prone mechanical thinking on the part of the user. We introduce a method for synthesizing layout constraints from mockups. We apply a representation-based search over version space algebras constructed by back propagation of specifications derived from concrete examples down a restricted grammar of linear integer arithmetic constraints. We evaluate our technique on several example layouts and find that we generate equivalent constraints as the ground truth (plus a few thousand extras), and suggest several directions for future work to refine this system.

[github](https://github.com/DylanLukes/Mockdown)

### Hoogle Plus: Type-driven and Component-based Synthesis
*David Justo, Michael James*

We explore large-scale component- and type-based synthesis in Haskell. Popular open source packages contain knowledge beyond their types and natural language documentation about how functions are typically composed. Hoogle Plus seeks to generate community-inspired straight-line code snippets from a type signature and a set of components, utilizing Haskell's strong type system and common function compositions in the wild.

### PhonoSynthesis: Symbolic inference of phonological rules
*Shraddha Barke, Rose Kunkel, Qian Xiong*

Phonological rules are general principles that apply to all words of a natural class that is defined in terms of phonological properties. We propose constraint based synthesis from examples to the problem of learning phonological rules. The phonological rules are expressed as constraints over the features of speech sounds. We divide the problem into inferring the change and inferring the condition, and give an encoding of these subproblems as SAT queries. Using these SAT queries, together with Z3’s soft constraints, we synthesize Russian devoicing and Korean deaspiration rules. We conclude that constraint-based synthesis is a viable approach for synthesizing phonological rules.

[github](https://github.com/shraddhabarke/Phonosynthesis)

### Tandoph: Automated Compiler Synthesis
*John Messerly, Patrick Liu*

We explore the use of examples and specifications for building compilers. Tandoph can be given a mixture of specifications and hard examples in a novel (functional) programming language, and uses representation based search to design an x86 compiler that satisfies all constraints. It builds on the older project META II, and can synthesize most x86 compilers that use numbers, variables, conditionals and loops.

[github](https://github.com/ptliu/tandoph)

### Code Completion using Statistical Language Models
*Anirudh Shekhawat*

We explore an approach for automated completion of API calls. Given a program with holes (missing method invocations), we make use of program analysis and statistical models to predict the most likely method invocation. The project involved designing a static program analysis process to extract useful sequences of method calls from publicly available code, a statistical model to learn the likelihood of sequences, and an algorithm to choose the most optimal completion for a given hole.

## 2017

The following course projects have been completed as a result of this class in Fall 2017

### Synthesis for Liquid Types
*Ethan Chan, Alexander Lin*

Refinement types are incredibly useful in guaranteeing program correctness over all inputs in a modular fashion. However, synthesis of intermediate refinement types currently requires the user to provide unintuitive atomic qualifiers to be used as building blocks in synthesis. We propose synthesis of intermediate refinement types through exploration of the grammar of the programming language itself, removing the necessity for atomic qualifiers.

[link](https://drive.google.com/file/d/1wqgMJUBDLKWbC24udmETf9cMNQGKfAAH/view?usp=sharing)

### Disjunctive Refinement type inference using CEGIS
*Anish Tondwalkar, John Renner*

We explore using counter-example guided synthesis to infer refinement types. Current techniques compute a Cartesian
abstraction of conjunctions over an abstract domain, which fails to scale to the inference of disjunctive invariants, whose running time can be worst-case exponential in the domain. We find that such a counter-example-based approach is even slower than standard approaches, and propose several improvements that might make such an approach more practical.

### Synthesis of MVC Controllers with Spyder
*John Sarracino, Alex Gamero-Garrido*

We propose Spyder, a technique for synthesizing the Controller in MVC systems from declarative constraints. Programming for the web (and more generally, GUI programming) is hard for many reasons: programmers typically must reason about nonlocal resources (e.g. network images), multiple programming environments (e.g. the HTML DOM and the JavaScript interpreter), and asynchronous events just to develop relatively simple systems. We aim to reduce the burden of programming reactive Model-View systems by replacing tricky cross-cutting reactive logic with program synthesis and constraints. In Spyder, the programmer specifies the relationship between the Model and View as a declarative constraint. From this constraint, as well as local logic for the reactive components, Spyder spins off a correct-by-construction program. In this paper, we develop a prototype implementation of Spyder and evaluate the effectiveness and efficiency of the approach on a simplified example of SSL certificate validation in Android. In addition, we discuss how the technique can be extended to multidimensional arrays, which would allow a broad range of graphical reactive programs to be synthesized.

### Generic Stream Fusion
*Hanzheng Li, Zheng Guo*

Generic stream fusion is a problem of automatically writing a stream function equivalent to a given list function.
We present two approaches to this problem. The first is to rewrite the list function into a stream function, with the help of a set of term-rewriting rules. In the second approach, we compose the stream function via program synthesis, where we generate a program sketch and use component-based synthesis to fill in the holes. We test them on some list functions, and discuss the strengths and limitations of each approach.

### Image2Tikz
*Dhanya Ganesh, Poornav Sargur*

The aim is to make use of a Machine Learning based image recognizer to synthesize underlying tikz code from an image of flow diagrams or hand-drawn diagrams. Machine learning models generalize well to an unseen input-output example and they are robust to noisy inputs. We wish to use these advantages of Machine Learning to synthesize tikz programs from images.

### Program Synthesis for Safe Hybrid Systems
*Tristan Knoth, Gaurav Mahajan*

We present an approach to synthesizing safe control systems for hybrid systems with non-linear dynamics on continuous real domain. By simultaneously searching for both the control program and its corresponding proof of safety, our method reduces the complexity of the control synthesis problem and expresses it as a Counter-Example Guided Inductive
Synthesis (CEGIS) problem. Thus, our approach scales effectively and can provide unbounded guarantees about the system’s safety. We also present a variant of CEGIS for use on continuous real domains as well as sufficient conditions necessary for finding solutions to such a problem. We evaluate our techniques by synthesizing a provably safe control system for UAVs working as "data mules". This work, to the best of our knowledge, presents the first such use of CEGIS for non-linear systems on a continuous real-valued domain.

### GPUSyn: Synthesis of GPU Kernels
*Sourav Anand*

The last decade has seen an incredible improvement in GPUs. The major difference between a GPU and a CPU is that a
GPU can have a lot of threads which run in parallel. An ideal use case for GPU program is to perform same computations
on the elements of an array containing a lot of data points. This project looks into this aspect and proposes a method to synthesize GPU kernels using Input-Output pairs of small sized arrays.

### Synthesis of Hash Functions
*Asbjoern Lystrup*

The goal of this project is synthesis of hash functions with pseudorandom distribution. The synthesizer uses stochastic search in the form of genetic programming, with a fitness function based on tests from the NIST statistical analysis suite. The implementation is explained through a review of its components, and results are presented for
a long run of the synthesizer.
