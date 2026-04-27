# PianoCoRe: Combined and Refined Piano MIDI Dataset

> Project repository for the article [**"PianoCoRe: Combined and Refined Piano MIDI Dataset"**](https://transactions.ismir.net/articles/10.5334/tismir.333)
> 
> Published in the [Transactions of the International Society for Music Information Retrieval](https://transactions.ismir.net/)
>
> Author: Ilya Borovik
>
> [![TISMIR](https://img.shields.io/badge/TISMIR-Publication-001347)](https://transactions.ismir.net/articles/10.5334/tismir.333)
> [![Zenodo](https://img.shields.io/badge/Zenodo-Dataset-blue)](https://doi.org/10.5281/zenodo.19186016)
> [![Dataset](https://img.shields.io/badge/HuggingFace-Dataset-yellow?logo=huggingface)](https://huggingface.co/datasets/SyMuPe/PianoCoRe)

## Description

**PianoCoRe** is a large-scale piano MIDI dataset that unifies and refines major open-source piano corpora. 
It contains **250,046 performances** of **5,625 pieces** written by **483 composers**, totaling **21,763 hours** of performed music. 

**PianoCoRe** provides the most diverse composer- and composition-annotated piano MIDI data.
The metadata includes deduplication flags, MIDI quality labels and precise note-level score-performance alignments. 

The alignments are refined using a **Refined Alignment for Scores and Performances (RAScoP)** pipeline, integrated into the [Symbolic Music Performance modeling (SyMuPe)](https://github.com/ilya16/SyMuPe) Python package. 
The pipeline ensures perfect note-by-note score-performance synchronization for expressive performance modeling.

For more details, please refer to the [full article](https://transactions.ismir.net/articles/10.5334/tismir.333).

Usage examples will be added after the update of the SyMuPe package.

## Dataset Tiers

| Dataset | Composers | Pieces | Performances | Hours | Scores | Alignments |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| **PianoCoRe-C** | 483 | 5,625 | 250,046 | 21,763 | 75.3% | no |
| **PianoCoRe-B** | 478 | 5,591 | 214,092 | 18,757 | 75.0% | no |
| **PianoCoRe-A** | 151 | 1,591 | 157,207 | 12,509 | 100% | note |
| **PianoCoRe-A\*** | 137 | 1,517 | 130,275 | 10,330 | 100% | note |

To support different research applications, the dataset is organized into tiered subsets:

- **PianoCoRe-C (Combined):** a complete mixed-source piano performance collection.

  *Applications*: piano performance analysis, data cleaning algorithms.
- **PianoCoRe-B (Base):** a deduplicated and quality-filtered subset.

  *Applications*: large-scale pre-training, piano performance generation.
- **PianoCoRe-A (Aligned):** a subset containing performances aligned to score.

  *Applications*: score-performance analysis, expressive piano performance rendering.
- **PianoCoRe-A\*:** a high quality subset of the best-quality performances and note-level alignments.

  *Applications*: expressive piano performance rendering, performance-to-score transcription.

Tier flags are provided in the metadata of both the Zenodo and Hugging Face versions of the dataset.

## License

The dataset, original and processed files, metadata, and alignment annotations are published under a **[CC BY-NC-SA 4.0](LICENSE)** license.
The license respects the licenses used for the source datasets. 
The underlying MIDI transcriptions are provided strictly for **non-commercial research and educational purposes**.

## Acknowledgments

PianoCoRe is built upon the invaluable contributions of the open music information retrieval community and existing open-source datasets. 
Acknowledgements and credits are given to the creators of the following source corpora:

| Dataset             | Reference                  | Links                                                                                                                        | License                                                               |
| ------------------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **MAESTRO**         | Hawthorne et al. (2019)    | [Paper](https://openreview.net/forum?id=r1lYRjC9F7) / [Dataset](https://magenta.withgoogle.com/datasets/maestro)             | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) |
| **ASAP**            | Foscarin et al. (2020)     | [Paper](https://archives.ismir.net/ismir2020/paper/000127.pdf) / [Dataset](https://github.com/fosfrancesco/asap-dataset)     | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) |
| **(n)ASAP**         | Peter et al. (2023)        | [Paper](https://transactions.ismir.net/articles/10.5334/tismir.149) / [Dataset](https://github.com/CPJKU/asap-dataset)       | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) |
| **ATEPP**           | Zhang et al. (2022)        | [Paper](https://archives.ismir.net/ismir2022/paper/000053.pdf) / [Dataset](https://github.com/tangjjbetsy/ATEPP)             | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)             |
| **GiantMIDI-Piano** | Kong et al. (2022)         | [Paper](https://transactions.ismir.net/articles/10.5334/tismir.80) / [Dataset](https://github.com/bytedance/GiantMIDI-Piano) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)             |
| **Aria-MIDI**       | Bradshaw and Colton (2025) | [Paper](https://openreview.net/forum?id=X5hrhgndxW) / [Dataset](https://github.com/loubbrad/aria-midi)                       | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) |
| **PERiScoPe**       | Borovik et al. (2025)      | [Paper](https://dl.acm.org/doi/10.1145/3746027.3755871) / [Dataset](https://huggingface.co/datasets/SyMuPe/PERiScoPe)        | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) |
| **PDMX**            | Long et al. (2025)         | [Paper](https://ieeexplore.ieee.org/document/10890217) / [Dataset](https://github.com/pnlong/PDMX/)                          | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)             |

## Citation

If you use this dataset in your research, please cite:

> Borovik, I. (2026). **PianoCoRe: Combined and Refined Piano MIDI Dataset**. Transactions of the International Society for Music Information Retrieval, 9(1), 144-163. DOI: [10.5334/tismir.333](https://doi.org/10.5334/tismir.333)

```bibtex
@article{borovik2026pianocore,
  title={{PianoCoRe: Combined and Refined Piano MIDI Dataset}},
  author={Borovik, Ilya},
  journal={Transactions of the International Society for Music Information Retrieval},
  volume={9},
  number={1},
  pages={144--163},
  year={2026},
  doi={10.5334/tismir.333}
}
```
