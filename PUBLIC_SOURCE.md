# PhantomCurrents: Counterfactual Intervention Prediction in Hidden Dynamical Networks — Dataset Source

This page is the canonical source reference for the **PhantomCurrents**
dataset as distributed through the Eris/Shipd platform.

## What this dataset is

A **fully synthetic** sequence-transduction dataset generated
programmatically with a fixed random seed by an original generator script
authored for this dataset. No sensor data, third-party text, or external
annotations were used. Each episode is an observed trace of a fictional
10-entity dynamical network (noisy level/inflow readings) followed by an
intervention specification; each label is the per-entity counterfactual
outcome class sequence computed by simulating the hidden system past the
intervention relative to a no-intervention baseline. The system's
parameters, coupling graph, and clean latent states are never distributed
— the dynamics can only be learned from the training episodes.

Contents:

| Item | Count | Description |
|---|---|---|
| Episodes | 8,120 | Observed traces + intervention specs (~515 tokens each) |
| Train | 5,800 | Labeled episode -> outcome class sequence pairs |
| Test | 2,320 | Unlabeled episodes across 7 hidden families |

The task is sequence transduction: given the trace and intervention, emit
the 10-entity outcome class sequence (`E01=mid|...`) or `absent`. Hidden
test families isolate unseen intervention types, unseen intervention
targets, a high-noise observation regime, and abstention calibration.

## License

**CC0 1.0 Universal (Public Domain Dedication)**
https://creativecommons.org/publicdomain/zero/1.0/

The generator script and all generated artifacts are original work released
under CC0. There are no restrictions on redistribution, modification, or
commercial use.

## Provenance

- Generation: deterministic scripted simulation (fixed seed); reproducible
  byte-for-byte from the generator.
- No personal data, no sensor data, no scraped content, no third-party
  intellectual property. All entities, traces, and interventions are
  fictional and machine-generated.
- Contact: dataset author via the Eris/Shipd platform.
