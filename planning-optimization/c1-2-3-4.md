# Planning & Optimization - FS2016

## C1 - Delete Relaxation: Introduction

### Delete Relaxation

In positive normal form: Effects that make state variables true are good (add effects), Effects that make state variables false are bad
(delete effects).

Idea of `delete relaxation heuristics`: ignore all delete effects.

*Delete Relaxation of Operator* is the operator obtained by replacing all negative effects ¬a within eff(o) by the do-nothing effect T
*Delete Relaxation of Planning Tasks* is the planning task Π = <V , I , {o+ | o ∈ O}, γ>
*Delete Relaxation of Operator Sequences* π = <o1,...,on> is the operator sequence π+ := <o1+,...,on+>

**Terminology**
- Planning tasks in positive normal form without delete effects are called *relaxed planning tasks*
- Plans for relaxed planning tasks are called *relaxed plans*
- If Π is a planning task in positive normal form and π+ is a plan for Π+, then π+ is called a relaxed plan for Π.


### C3 - AND/OR graph

**Definition**
An AND/OR graph <N, A, type> is a directed graph <N, A> with a node label function type : N → {∧, ∨} partitioning nodes into:
- AND nodes (type(v) = ∧)
- OR nodes (type(v) = ∨)

**Forced True Nodes**
Let G be an AND/OR graph. The set of nodes of G that are forced true is defined by finite application of the following rules:
- If n is an AND node where **all successors are forced true**, then n is **forced true**.
- If n is an OR node where **at least one successor is forced true**, then n is **forced true**.

### C4 - Relaxed Task Graphs
**Construction**
A relaxed task graph has four kinds of components:
- *Variable node* represent the state variables.
- The *initial node* represent the initial state.
- *Operator subgraphs* represent the preconditions and effects of operators.
- The *goal subgraph* represents the goal.

**Variable Nodes**
- For each v ∈ V , RTG(Π+) contains an **OR** node **nv**. These nodes are called variable nodes.

**Initial Node**
- RTG(Π+) contains an **AND** node **nI**. This node is called the initial node.
- For all v ∈ V with I(v) = T, RTG(Π+) has an arc from **nv** to **nI**. These arcs are called initial state arcs.

**Operator Subgraphs**
- for each formula φ that occurs as a sub-formula of the precondition or of some effect condition of o+, a **formula node nφ**
- for each conditional effect (χ > v) that occurs in the effect of o+, an **effect node nχ**. Unconditional effects are treated as (T > v)

***Formula Nodes***
- If φ = v for some state variable v, nφ is the variable node nv (so no new node is introduced).
- If φ = T, nφ is an AND node without outgoing arcs.
- If φ = ⊥, nφ is an OR node without outgoing arcs.
- If φ = (φ1 ∧ φ2), nφ is an AND node with outgoing arcs to nφ1 and nφ2.
- If φ = (φ1 ∨ φ2), nφ is an OR node with outgoing arcs to nφ1 and nφ2.

***Effect Nodes***
- nχ is an AND node.
- It has an outgoing arc to the formula nodes npre(o+) (precondition arcs) and nχ (effect condition arcs).
- Exception: if χ = T, there is no effect condition arc.
- For every conditional effect (χ > v) in the operator, there is an arc from variable node nv to nχ (effect arcs).

**Goal Subgraph**
- Consisting of formula nodes for the goal γ and its sub-formulas.
- Constructed in the same way as formula nodes for preconditions and effect conditions.
