# Cross-Processor Microarchitecture Study

A research project of the **Cybear Security Lab**.

## What this project is

Modern processors contain internal hardware structures, such as caches and
branch predictors, that programs cannot see directly but that affect how code
runs. Security research has shown that these structures can be used in ways
their designers did not intend.

Published results in this area are usually measured on one or two processors.
This project asks how well those results hold up across different Intel and AMD
processor generations. We rebuild published techniques and measure them the
same way on every machine, so the results can be compared.

The work is defensive. Its goal is to tell defenders and hardware designers
which behaviours are general and which depend on a specific processor.

## Why we need bare-metal cloud access

Our local testbed covers a few Intel and AMD processors. To draw general
conclusions we need more processor generations, especially recent server
parts. The measurements require:

- **Bare-metal nodes.** Virtual machines add noise and hide the hardware
  behaviour we measure.
- **Root access.** We pin work to single cores, fix the CPU frequency, and read
  hardware performance counters.
- **A range of Intel and AMD CPUs.** Different generations are the point of
  the study.

## How the experiments run

- Each experiment is a small, single-node program that runs on our own
  allocated machine.
- Experiments use no network traffic beyond our own SSH access and file
  transfer.
- Nothing targets other users, other tenants, or any outside system.
- Runs are short and repeated many times for statistical confidence, so we
  expect modest, bursty use of each node.

## Status

Active, 2026–2027. Code and results will be released alongside publications.

## Contact

Cybear Security Lab — via the GitHub organization
[CybearsecurityLab](https://github.com/CybearsecurityLab).
