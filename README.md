### Maxime Coia

I left banking to build technical depth from scratch. I work under the
frameworks: C, Unix, file descriptors, memory, and the error cases tutorials
leave out. I start at 42 Marseille in November 2026, and the destination past
it is ML systems, the layer where the question is no longer whether a model is
correct but what it costs to run.

Writing code got cheap. Knowing whether the code is right did not. I would
rather be good at the second one, and that is built at the bottom.

---

#### Selected work

**[learning_tree-ML-systems](https://github.com/maximecoia/learning_tree-ML-systems)** · Python, PyTorch

The public trace of a roadmap toward ML systems: eight phases and 95
sub-modules across the 42 curriculum and the years after it, from a Python
socle through a GPT trained from a blank file to C, CUDA and a contribution to
an inference engine.

* **Constraint.** Running is not the bar. An exercise counts when it can be
  written again from a blank file, and every step is graded by a checker that
  is not its own author.
* **Where it stands.** The Python socle is complete, 26 of 26, ending in
  `releve`, an installed command with eleven tests written against what it
  prints. The twenty-one Tensor Puzzles are solved and verified outside the
  notebook. The route to the trained GPT is the live track.
* **What it cost.** A course I had written for myself, and the Zero to Hero
  track under it, both removed on one measurement: the layer meant to prepare
  for the deliverable was not teaching the object the deliverable is graded
  on. Both are in the history, and the README says why.

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

---

#### Now

**September 2026.** The Python line is finished and the tensor puzzles are
done, so the work moved up one layer and down one.

**The route to the trained GPT.** The tokenizer next, then causal attention
written rather than called, the blocks, the training loop with its two losses,
and the fifteen architecture-agnostic adapters of CS336 assignment 1 against
its public suite. The phase closes when I can draw a token's path to the
logits from memory, shapes at every step.

**The C under it.** The libft is written: 43 functions from the contracts of
the standard library, a self-test of 44 checks that goes red when a function is
broken on purpose, no leaked byte. It is a 42 subject, so it stays private by
the school's charter. After it comes the C engine that loads the trained model
and places its throughput on a roofline.

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
