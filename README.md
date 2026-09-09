### Maxime Coia

I left banking to build technical depth from scratch. I work under the
frameworks: C, Unix, file descriptors, memory, and the error cases tutorials
leave out. I start at 42 Marseille in November 2026.

Writing code got cheap. Knowing whether the code is right did not. I would
rather be good at the second one, and that is built at the bottom.

---

#### Selected work

**[unix-toolbox](https://github.com/maximecoia/unix-toolbox)** · C99, POSIX, CI

Small Unix utilities rebuilt one mechanism at a time: `mini_echo`, `mini_cat`,
`mini_cp`, `mini_wc`.

* **Constraint.** No cloning of full GNU behavior. Each program stays small
  enough to be understood end to end, from argument parsing through every
  failure path.
* **What it covers.** File descriptors and POSIX I/O, buffers and partial
  writes, state carried across reads, resource ownership, behavioral tests
  running in CI.
* **What it cost.** Partial writes and EOF are where the naive implementation
  quietly breaks. Finding that out is most of the value of building it.

**[learning_tree-ML-systems](https://github.com/maximecoia/learning_tree-ML-systems)** · Python

Twenty-six exercises, from a first conversion to a command someone else
installs, each taken to the point where it can be rebuilt from a blank file
instead of recognized.

* **Constraint.** An exercise is not finished when it runs. It is finished when
  it can be written again from nothing.
* **What it covers.** Types and control flow, then aggregation over input that
  does not conform, then classes that carry their own invariants. Amounts held
  as integer centimes rather than floats, because the representation is the
  decision.
* **Where it ends.** `releve`, an installable tool: subcommands, a `--strict`
  mode, stdin, exit codes a shell can branch on, and tests written against the
  rendered output rather than the internals. Everything downstream in this plan,
  a measurement bench or a training script or a grader, is handed to someone who
  runs it without asking how.

---

#### Now

**September 2026.** The Python line is finished, so the work moved up one layer.

**micrograd.** Karpathy's scalar autograd, rebuilt from nothing rather than
read. Operators that record what produced a value, a loss collapsed to the one
number every gradient is taken with respect to, and backpropagation done by
hand through a `tanh` neuron before any `backward()` exists to call it. Each
gradient is checked against the same quantity measured numerically, by nudging
the input and dividing, because a chain rule you cannot falsify is a chain rule
you have memorized.

**C and C++.** Allocation and ownership, `ft_split` and its partial-failure
path, gdb and valgrind until they are reflex rather than lookup. Then
inheritance and object layout, and `sizeof` on a diamond because the number
says where the memory actually went.

Ordered by what does not survive being done fifteen minutes at a time.

---

#### How I work

* Understand the mechanism before adding the abstraction.
* Derive the implementation from the requirement instead of recalling the code.
* Test the failure paths, because that is where understanding actually gets checked.

---

#### Background

Seven months building a gamified financial-education product on my own, then
eight months at BNP Paribas as a banking advisor, across from the people making
the decisions that product was trying to teach. The layer that held my attention
in both was the one underneath.

#### Elsewhere

* Writing about leverage, judgment, and what AI changes: [@MaximeCoia](https://x.com/MaximeCoia)
* [linkedin.com/in/maxime-coia](https://www.linkedin.com/in/maxime-coia/)
* coiamaxime@gmail.com
