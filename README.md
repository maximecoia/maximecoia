### Maxime Coia

I left banking to build technical depth from scratch. The work sits on the layer
most people abstract away: C, Unix, processes, memory, and the failure paths that
never make it into a tutorial. Starting at 42 Marseille in November 2026.

The bet, stated plainly: depth at the bottom layer compounds upward through
everything built on top of it, and judgment about systems gets more valuable as
writing code gets cheaper, not less.

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

**[Python_Modules](https://github.com/maximecoia/Python_Modules)** · Python

Progressive exercises taken to the point where each one can be rebuilt from a
blank file instead of recognized.

---

#### Now

**August 2026.** Pre-core work ahead of November: allocation and ownership in C,
`ft_split` and its partial-failure path, gdb and valgrind until they are reflex
rather than lookup. Ordered by what does not survive being done fifteen minutes
at a time.

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
