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
