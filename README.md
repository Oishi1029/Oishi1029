## Bong Bin Yong

Undergraduate in Malaysia. working on quantum optimal control at the pulse level, and on the
classical electronics sitting between the optimizer and the qubit.

**Merged upstream**

- [harmoniqs/Piccolo.jl#238](https://github.com/harmoniqs/Piccolo.jl/pull/238) — dual-rail encoding
  and `EmbeddedOperator` utilities: sparse subspace reduction, logical-ordered subspaces,
  operator/target consistency checks, 10 testitems. unitaryHACK 2026.
- [harmoniqs/Legato.jl#27](https://github.com/harmoniqs/Legato.jl/pull/27) — FFT pulse-spectrum
  analyzer. unitaryHACK 2026.

**My own**

- [predistort](https://github.com/Oishi1029/predistort) — a differentiable model of a superconducting
  control line (DAC zero-order hold, line response, IQ imbalance, amplifier compression) wired to a
  three-level transmon in JAX, with every stage adjoint derived by hand.

  The composed Julia↔JAX gradient agrees with central finite differences to 1.09e-06 worst-case, and
  `make env && make build && make verify` reproduces that from a clean clone (verified on Apple
  silicon).

  The headline result is negative. Below roughly 131 MHz of drive bandwidth the linear inverse demands
  DAC codes outside the box, and a clipped inverse is not an inverse — the corrected gate (3.76e-03)
  comes out worse than no pre-distortion at all (2.40e-03).

I use AI assistance when I write code, and I disclose it where the work is published. Nothing goes out
that I have not read, run and tested myself.

I came to this from embedded and storage systems: STM32/FreeRTOS firmware, an automotive radar
project, and a ZNS emulation result (1st runner-up, Sandisk symposium).
