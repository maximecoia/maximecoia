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

The public trace of a roadmap toward ML systems: eight phases and 93
sub-modules across the 42 curriculum and the years after it, from a Python
socle through a GPT trained from a blank file to C, CUDA and a contribution to
an inference engine.

* **Constraint.** Running is not the bar. An exercise counts when it can be
  written again from a blank file, nothing is graded by its own author alone,
  and every check was broken on purpose before it was trusted.
* **Where it stands.** The Python socle is complete, 26 of 26, ending in
  `releve`, an installed command with eleven tests written against what it
  prints. The maths are complete too, 20 of 20 in plain Python: linear algebra
  up to a 2D transformation engine, probability held against closed forms, and
  statistics that count their own error rate. The twenty-one Tensor Puzzles
  are solved, and chapters 2 to 5 of Raschka's book are answered, with tests
  written against what each chapter states, since the book ships almost none.
* **What it cost.** A course I had written for myself, and the Zero to Hero
  track under it, both removed on one measurement: the layer meant to prepare
  for the deliverable was not teaching the object the deliverable is graded
  on. Both are in the history, and
  [`DECISIONS.md`](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/DECISIONS.md)
  says why.

**[unix-toolbox](https://github.com/maximecoia/unix-toolbox)** · C99, POSIX, CI

Small Unix utilities rebuilt one mechanism at a time: `mini_echo`, `mini_cat`,
`mini_cp`, `mini_wc`.

* **Constraint.** No cloning of full GNU behavior. Each program stays small
  enough to be understood end to end, from argument parsing through every
  failure path.
* **What it covers.** File descriptors and POSIX I/O, buffers and partial
  writes, state carried across reads, resource ownership, behavioral tests
  running in CI on Linux and macOS.
* **How the tests are checked.** Each utility was broken on purpose, fourteen
  ways in all, and thirteen are caught. A shell cannot make `write()` return
  short or `read()` fail, so the utilities are rebuilt with the calls
  redirected at compile time: every write cut to one byte, and for `mini_cp`
  a read that fails with `EIO` or `EINTR` on demand.
* **What it cost.** Partial writes and EOF are where the naive implementation
  quietly breaks. Finding that out is most of the value of building it, and
  the tests now show it.

---

#### Now

**Until 31 October 2026.** The rest of the prep is done, so the work is one
object: `gpt.py`, a causal GPT in `torch` written from a blank file, with the
attention written by hand rather than called.

**How it is graded.** A
[black-box acceptance test](https://github.com/maximecoia/learning_tree-ML-systems#the-acceptance-test), written before the model:
seven gates, from the shape of the logits and a loss at initialisation near
`ln(65)`, through a drift of exactly zero when future tokens change, to trained
weights that land 0.10 below a counted bigram on held-out text. The model goes
in one piece at a time, each piece turning a gate green. Today the count is 0
of 7, and [the phase page](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/ms-00-prepa/README.md#what-to-do-in-order)
keeps it current.

**Then the write-up.** The model closes the phase, and a
[public write-up](https://github.com/maximecoia/learning_tree-ML-systems#what-closes-l1) closes L1: the corpus with its licence and the script that rebuilds its split, the run
with its seed and versions, both loss curves whole, unsorted samples, and a
report someone else can replay without asking a question.

**The C under it.** The libft is written: 43 functions from the contracts of
the standard library, a self-test of 44 checks that goes red when a function is
broken on purpose, no leaked byte. It is a 42 subject, so it stays private by
the school's charter. The C engine that generates text and places its
throughput on a roofline moved to the first phase at the school, after the
measurement tools it needs.

---

#### How I work

* Understand the mechanism before adding the abstraction.
* Derive the implementation from the requirement instead of recalling the code.
* Test the failure paths, because that is where understanding actually gets checked.
* Break a check on purpose before trusting it. A check that cannot fail proves nothing.

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
