# SpaceAI

**Australian-made AI, trained only on Australian text.**

SpaceAI is an independent Australian AI project founded by M Davis. Everything is built in-house in Australia:
- the training corpus;
- the tokenizer;
- the model;
- the distributed training system that ties home GPUs together.

No third-party model weights, tokenizers or training frameworks are used.

## What exists today

| | Status |
|---|---|
| **SpaceAI Australian Corpus v1** | 52,662 documents, about 466 million tokens, 100% Australian. CC BY 4.0 / public domain. [Dataset on Hugging Face](https://huggingface.co/datasets/MrSpaceCommander/spaceai-australian-corpus) |
| **spaceai-sp32k tokenizer** | 32,768-token vocabulary trained only on Australian text. It handles Australian place names and terms natively ("Wagga Wagga", "Commonwealth"). |
| **SpaceAI-0.1B** | 100.7M-parameter language model, training now from random initialisation on the Australian corpus. |
| **Swag** | SpaceAI's own distributed training system (see below). |

## The corpus

Only material that is Australian in origin and free to redistribute:
- legislation from six jurisdictions;
- Productivity Commission, AIHW, RBA and Treasury publications;
- a century of Year Book Australia;
- NSW and SA government documents;
- ABS and ACSC material;
- public-domain Australian literature.

What was kept out:
- No court decisions, Hansard, AustLII or CC BY-SA material.
- No web text after November 2022, and no AI-generated text.
- Third-party material the publishers exclude from their licences was withheld.

Full details are in the [dataset card](https://huggingface.co/datasets/MrSpaceCommander/spaceai-australian-corpus).

## Swag: training on the GPUs Australians already own

Swag ("everything you need, carried between camps") trains one model across a mixed group of ordinary consumer GPUs on a home network. Today that's an RTX 3070, an RTX 3080 Laptop and an RTX 2060 Super, which also get used for gaming and other work.

What it does:
- **Uses mismatched hardware.** Fast and slow cards contribute in proportion to the work they actually do.
- **Tolerates machines coming and going.** Nodes can join late, pause for other workloads, or drop out without stopping the run.
- **Accounts for every token.** A ledger records exactly which data has been trained into the model, so nothing is lost or counted twice.
- **Protects the best model.** The best checkpoint is always kept, and bad rounds are never saved over it.
- **Grows mid-run.** New Australian data can be added to a running training job.
- **Provides provenance.** Every training run can be traced back to the documents it used.

Swag is proprietary to SpaceAI. It builds on published research into local-update distributed optimisation (DiLoCo, Douillard et al., 2023); the implementation and protocol are SpaceAI's own.

## Roadmap

1. **Now:** SpaceAI-0.1B trained on the corpus; public corpus v1 released.
2. **Next:** SpaceAI-0.1B public weights for Australian users under the SpaceAI Community Licence (gated download).
3. **Then:** Swag v0.2 (faster, compressed and authenticated updates, adaptive work per GPU). Larger SpaceAI models. Corpus v1.1 (more Year Book Australia issues, more public-domain Australian literature).
4. **Later:** commercial SpaceAI offerings for Australian organisations.

## Licensing

| Part | Licence |
|---|---|
| Corpus | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) plus public domain. See the dataset's `ATTRIBUTION.md`. |
| Model weights (when released) | [SpaceAI Community Licence](LICENCES/SpaceAI-Community-Licence.md): Australian users only (draft) |
| Training code, Swag, tokenizer training pipeline | Proprietary, not published |
| This repository (text, roadmap, brand) | © 2026 M Davis. All rights reserved. |

"SpaceAI" and "Swag" are trade marks of M Davis. See [TRADEMARKS.md](TRADEMARKS.md).

## Contact

Partnerships, licensing and commercial enquiries: via [GitHub](https://github.com/SpaceyDee) or [Hugging Face](https://huggingface.co/MrSpaceCommander).
