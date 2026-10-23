<div align="center">

# Maxime Coia

**Learning to run models, from the bottom of the stack.**

<img src="https://skillicons.dev/icons?i=py,pytorch,c,bash,linux,git,githubactions" alt="Python, PyTorch, C, Bash, Linux, Git and GitHub Actions">

</div>

I left banking to build technical depth from scratch. I am heading to ML
systems, the layer where the question is no longer whether a model is correct
but what it costs to run. I start at 42 Marseille on 9 November 2026.

Writing code got cheap. Knowing whether the code is right did not. So every
check I write is broken on purpose before I trust it.

## Selected work

**[learning_tree-ML-systems](https://github.com/maximecoia/learning_tree-ML-systems)** · Python, PyTorch

A public roadmap toward ML systems, from a GPT written by hand to measured
inference and a contribution to the vLLM organisation.

* **L1, a GPT trained by hand.** A character-level model trained on Jules
  Verne, attention written from scratch. 164,065 parameters, 69 seconds on a
  laptop CPU. [Write-up](https://github.com/maximecoia/learning_tree-ML-systems#phase-0-a-gpt-trained-by-hand)
* **Graded before it existed.** Its dev loss is 1.7480, against 2.3928 for a
  counted bigram. A [black-box acceptance test](https://github.com/maximecoia/learning_tree-ML-systems#the-acceptance-test),
  written before the model, decides.
* **Measured inference.** 40 exercises, from timing that ignores warm-up to
  prefill and decode, the KV cache, quantisation, and the point where a served
  model breaks under load. [Phase page](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/ms-01-inference/README.md)

**[unix-toolbox](https://github.com/maximecoia/unix-toolbox)** · C99, POSIX, CI

Unix utilities rebuilt in C, small enough to read end to end: `mini_echo`,
`mini_cat`, `mini_cp`, `mini_wc`.

* **Where naive C breaks.** Partial writes, EOF and failing reads, tested in CI
  on Linux and macOS.
* **Tests that can fail.** The utilities were broken on purpose fourteen ways,
  and thirteen are caught. [What the tests prove](https://github.com/maximecoia/unix-toolbox#what-the-tests-prove)
* **Faults a shell cannot cause.** System calls are redirected at compile time,
  so every write is cut to one byte and `mini_cp` reads fail with `EIO` or
  `EINTR`.

## Now

L2: the throughput and latency curve of an inference server, published as a
write-up before school starts. In parallel, the 42 C projects, kept private
under the school's charter. [Live progress](https://github.com/maximecoia/learning_tree-ML-systems/blob/main/ms-01-inference/README.md#what-to-do-in-order)

## Background

Seven months building a financial-education product on my own, then eight
months as a banking advisor at BNP Paribas.

[LinkedIn](https://www.linkedin.com/in/maxime-coia/) ·
[X](https://x.com/MaximeCoia) ·
coiamaxime@gmail.com
