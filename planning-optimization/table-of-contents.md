# Table of contents

**A3. Transition Systems and Propositional Logic**
- Transition Systems
- Propositional Logic

**A4. Planning Tasks**
- Planning task

**A5. Equivalent Operators and Effect Normal Form**
- Equivalent Operators
- Effect Normal Form
  - Effect condition

**A6. Positive Normal Form and STRIPS**
- Positive Normal Form
  - Planning Task in Positive Normal Form
- STRIPS

**A7. Invariants and Mutexes**
- Invariants
- Mutexes

**A8. Finite Domain Representation**
- FDR Planning Tasks: Finite-domain
  - FD variables
  - FD states
  - FD fomulars
  - FD effects
  - FDR task semantics
- SAS+ Planning Tasks
  - SAS+ vs STRIPS
- Transition Normal Form

**B1. Planning as Search**
- Search
- Planning as Search
  - Progression search
  - Regression search
  - Heuristics for classical planning
- Progression search
  - example

**B2. Regression: Introduction & STRIPS Case**
- Regression search
  - example
  - Regression for STRIPS tasks

**B3 & B4. General Regression**
- General regression
  - Regression state variables
  - Regression formulas through Effects
  - Regression formulas through Operators
    - example

**B5 & B6. Computational complexity of Planning**
- Turing Machines
  - Turing Machines transitions
- Plan Existence
  - Bounded-Cost Plan Existence
- PSPACE
  - Reduction: State variables, Initial state, Operators, Goal

**C1. Delete Relaxation: Introduction**
- Planning as Heuristic search
- Relaxed Planning Tasks
  - Delete relaxation
  - Delete-relaxed Planning Tasks
  - Relaxed Planning Tasks
- Domination Lemma
- Relaxation Lemma

**C2. Delete Relaxation: Finding Relaxed Plans**
- Greedy Algorithm
- Optimal Relaxed Planning

**C3. Delete Relaxation: AND/OR graphs**
- AND/OR graphs
- Forced nodes
  - Forced True Nodes
  - Forced False Nodes
- Most and Least Conservative Valuation

**C4. Delete Relaxation: Relaxed Task Graphs**
- Relaxed Task Graphs
  - Construction

**C5. Delete Relaxation: hmax and hadd**
- Delete Relaxation Heuristics
  - hmax Algorithm
  - hadd Algorithm

**C6. Delete Relaxation: Best Achievers and hFF**
- Choice Functions
- Best Achievers
  - Best Achiever Graphs
- The FF Heuristic
- hmax vs. hadd vs. hFF vs. h+

**C7. Abstraction: Introduction**
- Abstracting a Transition System
  - example
- Multiple Abstractions
  - Maximizing
  - Adding

**C8. Abstractions: Formal Definition and Heuristics**
- Recall: Transition System of Example Task
- Abstractions
  - Definition
  - Abstract Transition System
- Homomorphisms and Isomorphisms
  - Isomorphic Transition Systems
  - Graph-Equivalent Transition Systems
- Abstraction Heuristics
- Coarsenings and Refinements
  - Abstractions of Abstractions
  - Heuristic Quality of Refinements

**C9. Abstractions: Additive Abstractions**
- Additivity
  - Orthogonality of Abstractions
  - Orthogonality and Additivity
- Outlook
  - Using Abstraction Heuristics in Practice

**C10. Pattern Databases: Introduction**
- Projections and Pattern Database Heuristics
  - Pattern Database Heuristics
  - Projections
- Implementing PDBs: Precomputation
  - Syntactic Projections
  - Trivially Inapplicable Operators
  - Trivially Unsolvable SAS+ Tasks
- Implementing PDBs: Lookup
  - Lookup Step: Algorithm

**C11. Pattern Databases: Multiple Patterns**
- Additive Patterns
  - Canonical Heuristic Function
- Dominated Additive Sets
  - Dominated Sum Theorem
- Redundant Patterns
  - Non-Goal Patterns
  - Causal Graphs
  - Causally Connected Patterns
  - Causally Disconnected Patterns

**C12. Pattern Databases: Pattern Selection**
- Pattern Selection as Local Search
- Search Neighbourhood
  - Computing hC'(s)
- Literature

**C13. Merge-and-Shrink Abstractions: Synchronized Product**
- Merge-and-Shrink Abstractions
- Synchronized Products
  - Synchronized Product of Transition Systems
  - Synchronized Product of Functions
  - Synchronized Product of Abstractions
  - Relationship
  - Synchronized Products and Abstractions

**C14. Merge-and-Shrink Abstractions: Generic Algorithm**
- Generic Algorithm
  - Initialization step
  - Merge step
  - Shrink step

**C15. Merge-and-Shrink Abstractions: Maintaining the Mapping and Some Theory**
- Maintaining the Abstraction
  - Maintaining the Abstraction when Shrinking
- Safe and Exact Transformations
  - Collection of Transition Systems
  - Exact Transformations
  - Sequences of Transformations

**C16. Merge-and-Shrink Abstractions: Strategies and Label Reduction**
- Merging Strategies
- Shrinking Strategies
  - Bisimulations as Abstractions
  - Abstractions as Bisimulations
  - Greedy Bisimulations
- Label Reduction

**C17. Critical Path Heuristics: hm**

*we consider only STRIPS, backward search and regression*
- Set Representation of STRIPS Planning Tasks
  - STRIPS Operators in Set Representation
  - STRIPS Planning Tasks in Set Representation
  - STRIPS Regression in Set Representation
- Perfect Regression Heuristic
- Critical Path Heuristics
  - hmax Heuristic
  - hm Heuristic
- Computation

**C18. Critical Path Heuristics: Properties and Πm Compilation**
- Heuristic for Forward / Backward Search
-  Πm Compilation

**C19. Landmarks: Introduction & Minimum Hitting Set Heuristics**
- Landmarks
  - Disjunctive Action Landmark
  - Fact and Formula Landmarks
- Minimum Hitting Set Heuristic and Uniform Cost Partitioning
  - Hitting Set
  - Uniform Cost Partitioning Heuristic for Landmarks

**C20. Landmarks: Cut Landmarks & LM-cut Heuristic**
- Delete-Free STRIPS Planning Task in Normal Form
- Cut Landmarks
- The LM-Cut Heuristic

**C21. Landmarks: And/Or Landmarks**
- Landmarks from RTGs
  - Causal Formula Landmark
  - Justification
  - Landmarks in AND/OR Graphs
- Landmarks from Πm

**C22. Landmarks: LM-count Heuristic**
- Landmark Orderings
  - natural ordering
  - greedy-necessary ordering
- Landmark-count Heuristic
