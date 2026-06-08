# QSOE — Quick and Secure Operating Environment

A microkernel-based operating system for 64-bit RISC-V, in the QNX Neutrino
tradition: synchronous message-passing IPC, resource managers, a small kernel,
and everything else in userspace.

QSOE comes in two variants that share one userspace and one build system:

- **QSOE/N** runs on **Skimmer**, a microkernel written from scratch for this
  project (SMP by design).
- **QSOE/L** runs on **seL4** as the kernel.

Both are assembled by the **Umbrella** build system, which selects kernel and
userspace components Kconfig-style. Userspace is shared across both variants;
only the task manager (`taskman`) differs per kernel.

**License:** Apache-2.0

## Status

QSOE/N boots on real hardware — first successful boot on the SiFive HiFive
Unmatched (FU740). Development continues on both variants.

## Target

- 64-bit RISC-V (RV64, Sv39)
- Board: SiFive HiFive Unmatched (FU740)
- QEMU for day-to-day development

## Where things live

Primary development is on GitLab. This GitHub organization mirrors a few things
and exists so GitHub-only folks can follow along.

- **Umbrella / main repo:** https://gitlab.com/qsoe/os
- **Project site (source):** https://github.com/qsoe-dev/site — served at https://qsoe.net
- **Dev log / blog:** https://qsoe-dev.blogspot.com
