<div align="center">

# Maxime Coia

**Learning to run models, from the bottom of the stack.**

<img src="https://skillicons.dev/icons?i=py,pytorch,c,bash,linux,git,githubactions" alt="Python, PyTorch, C, Bash, Linux, Git and GitHub Actions">

</div>

I left banking to build technical depth from scratch. I work under the
frameworks: C, Unix, file descriptors, memory, and the error cases tutorials
leave out. I start at 42 Marseille in November 2026, and the destination past
it is ML systems, the layer where the question is no longer whether a model is
correct but what it costs to run.

Writing code got cheap. Knowing whether the code is right did not. I would
rather be good at the second one, and that is built at the bottom.

---

## Selected work

**[learning_tree-ML-systems](https://github.com/maximecoia/learning_tree-ML-systems)** · Python, PyTorch

The public trace of a roadmap toward ML systems. It has eight phases, numbered
0 to 7 like their folders. They run alongside the 42 common core and the years
after it. The route goes from a Python socle, through a GPT trained from a
blank file and a measured inference server, to a contribution to the vLLM
organisation.

* **Constraint.** Running is not the bar. An exercise counts when it can be
  written again from a blank file. Nothing is graded by its own author alone.
  Every check was broken on purpose before it was trusted.
* **The phases.** `ms-00-prepa` → `ms-01-inference` → `ms-02-infrastructure` →
  `ms-03-contribution` → `ms-04-agents-reseau` → `ms-05-fin-tronc-commun` →
  `ms-06-apres-tronc` → `ms-07-alternance`. Phases 1 to 5 follow the school's
  milestones. The roadmap carries no estimated dates, and
  [the reason is written down](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/DECISIONS.md#why-the-roadmap-has-no-dates).
* **Where it stands.** Phase 0 is closed. It holds the Python socle, 26 of 26
  exercises, ending in `releve`, an installed command with eleven tests written
  against what it prints. It holds the maths, 20 of 20 in plain Python: linear
  algebra up to a 2D transformation engine, probability held against closed
  forms, and statistics that count their own error rate. It holds the
  twenty-one Tensor Puzzles, and chapters 2 to 5 of Raschka's book, answered
  with tests written against what each chapter states, since the book ships
  almost none. Phase 1 is in progress, and its 40 measurement and inference
  exercises are done.
* **The first deliverable.**
  [L1](https://github.com/maximecoia/learning_tree-ML-systems/tree/main/ms-00-prepa/l1-01-gpt-corpus)
  is a character-level GPT trained on Jules Verne, with the attention written
  by hand. It has 164,065 parameters and trained in 69 seconds on a laptop CPU.
  Its dev loss is 1.7480, against 2.3928 for a counted bigram. A
  [black-box acceptance test](https://github.com/maximecoia/learning_tree-ML-systems#the-acceptance-test),
  written before the model, grades it.
* **What it cost.** A course I had written for myself went first. In eleven
  days it produced 141,783 lines of lessons and 2,038 lines of machine learning
  code, and none of the 34 exercises that already existed had been handed in.
  The Zero to Hero track went next. Across the prep, the word `torch` appeared
  twice, while the acceptance test imports it on its first line. That work is
  kept in the history.
  [`DECISIONS.md`](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/DECISIONS.md)
  says why.
* **What moved.** The C inference engine, `c-06-moteur`, first left the prep and
  then left phase 1. It now waits until after the common core, in
  [`ms-06-apres-tronc`](https://github.com/maximecoia/learning_tree-ML-systems/tree/main/ms-06-apres-tronc).
  It grafts onto no school project, and its delay can be caught up later.
  [The decision](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/DECISIONS.md#the-c-engine-and-why-it-left-the-prep)
  is on record.

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
  redirected at compile time. Every write is cut to one byte, and `mini_cp`
  gets a read that fails with `EIO` or `EINTR` on demand.
* **What it cost.** Partial writes and EOF are where the naive implementation
  quietly breaks. Finding that out is most of the value of building it, and
  the tests now show it.
* **Where it leads.** The C continues in the libft, then in the school's C
  projects. The C inference engine comes later, after the common core.

---

## Now

**Phase 1, `ms-01-inference`.** It is in progress, and 45 of its 46 graded
exercises pass. The 40 measurement and inference exercises are done. They run
from a stopwatch that ignores warm-up to the point where a served model breaks
under load. The other six are the school's C, and five of them pass.
[The phase page](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/ms-01-inference/README.md#what-to-do-in-order)
lists the work in order.

**L2 is next.** It is the throughput and latency curve of an inference server.
It comes before the school starts on 9 November 2026. The target is the
saturation curve of an unknown server, produced in half a day. A reader grades
it, not a terminal, because the write-up is public.

**What closed.** The prep, `ms-00-prepa`, closed on 2 October 2026. L1, a
character-level GPT trained on Jules Verne with hand-written attention, was
published on 1 October 2026 and validated on 2 October. The
[write-up that closes L1](https://github.com/maximecoia/learning_tree-ML-systems#what-closes-l1)
lists what a stranger needs to replay it without asking a question.

**The C under it.** The libft, `ft_printf` and `get_next_line` pass their
graders. `push_swap` is the one left, and it follows the school's calendar. All
four stay private, because they are 42 subjects and the school's charter forbids
publishing a solution. The C inference engine waits behind the common core.

---

## How I work

* Understand the mechanism before adding the abstraction.
* Derive the implementation from the requirement instead of recalling the code.
* Test the failure paths, because that is where understanding actually gets checked.
* Break a check on purpose before trusting it. A check that cannot fail proves nothing.

---

## Background

Seven months building a gamified financial-education product on my own, then
eight months at BNP Paribas as a banking advisor, across from the people making
the decisions that product was trying to teach. The layer that held my attention
in both was the one underneath.

## Elsewhere

* Writing about leverage, judgment, and what AI changes: [@MaximeCoia](https://x.com/MaximeCoia)
* [linkedin.com/in/maxime-coia](https://www.linkedin.com/in/maxime-coia/)
* coiamaxime@gmail.com
