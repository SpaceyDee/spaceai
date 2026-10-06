# SpaceAI

**Australian-made AI, trained only on Australian text.**

SpaceAI is an independent Australian AI project founded by M Davis, currently a private passion project (company coming soon). Everything is built in-house in Australia:
- the training corpus;
- the tokenizer;
- the model;
- the distributed training system that ties home GPUs together.

No third-party model weights, tokenizers or training frameworks are used.

## What exists today

| | Status |
|---|---|
| **SpaceAI Australian Corpus v1** | 53,337 documents, about 484 million tokens, 100% Australian. CC BY 4.0 / public domain. [Dataset on Hugging Face](https://huggingface.co/datasets/MrSpaceCommander/spaceai-australian-corpus) |
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

## Swag

Swag ("everything you need, carried between camps") is SpaceAI's own system for training one model across the ordinary consumer GPUs Australians already own. It is proprietary and not published.

## Roadmap

1. **Now:** SpaceAI-0.1B trained on the corpus; public corpus v1 released.
2. **Next:** SpaceAI-0.1B public weights for Australian users under the SpaceAI Community Licence (gated download).
3. **Then:** Swag v0.2. Larger SpaceAI models. Corpus v1.1 (more Year Book Australia issues, more public-domain Australian literature).
4. **Later:** commercial SpaceAI offerings for Australian organisations.

## Licensing

| Part | Licence |
|---|---|
| Corpus | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) plus public domain. See the dataset's `ATTRIBUTION.md`. |
| Model weights (when released) | [SpaceAI Community Licence](LICENCES/SpaceAI-Community-Licence.md): Australian users only, approved on request |
| Training code, Swag, tokenizer training pipeline | Proprietary, not published |
| This repository (text, roadmap, brand) | © 2026 M Davis. All rights reserved. |

"SpaceAI" and "Swag" are trade marks of M Davis (registration coming soon). See [TRADEMARKS.md](TRADEMARKS.md).

## Contact

Questions, collaboration and licensing: via [mrspacecadet.com.au](https://mrspacecadet.com.au), [GitHub](https://github.com/SpaceyDee) or [Hugging Face](https://huggingface.co/MrSpaceCommander).
