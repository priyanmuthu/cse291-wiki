# CSE 291: Program Synthesis

**Instructor:** [Nadia Polikarpova](https://cseweb.ucsd.edu/~npolikarpova/) <br/>
**Time:** Tuesdays and Thursdays 3:30-4:50 PM <br/>
**Location:** CSE 4140 <br/>
**Office Hours:** Tuesdays 5:00-6:00 PM <br/> 

This course is a comprehensive introduction to *program synthesis*: an emerging area that sits at the intersection of programming systems, formal methods, and artificial intelligence. The goal of program synthesis is to generate programs automatically from high-level, possibly incomplete descriptions. The course covers a wide variety of recent synthesis techniques that differ in the kind of program description they start with (from input-output examples to formal correctness specifications), the search strategy they employ (enumerative, stochastic, or symbolic search), and the kind of information they use to guide the search (counter-example guided synthesis, type-driven synthesis, synthesis with machine learning). The course involves a project, as well as reading and reviewing research papers.

The course material is organized into three modules:
* **Synthesis from Examples.** This module covers tools and techniques for generating programs that behave according to a set of input-output examples. We will look at different ways to represent and explore the large space of candidate programs, such as exhaustive enumeration, stochastic search, representation-based search, and constraint solving.
* **Synthesis from Specifications.** This module explores approaches that go beyond input-output examples, requiring the synthesized program to satisfy certain properties on all inputs. We will look at techniques that support different levels of expressiveness (loop-free vs. looping/recursive programs) and provide different levels of guarantees (bounded vs. unbounded correctness). Some techniques reduce this problem to synthesis from examples, while others directly rely on a proof/type system to guide the search.
* **Applications of Synthesis.** In this module we will see how the techniques we have covered previously can help with practical tasks, such as code completion, data wrangling, and superoptimization. We will also explore applications of synthesis in other areas of computer science (databases, graphics, machine learning, and security).

There is no Piazza page for this course. To ask a question, use the [issue tracker](https://github.com/nadia-polikarpova/cse291-program-synthesis/issues).

<img src="http://db.ucsd.edu/wp-content/uploads/2015/05/CSELogo_full.gif" height="80px">