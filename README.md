# Awesome Perturbation Omics [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated, **technology-forward** map of single-cell and spatial perturbation omics — the assays, the library design, the analysis, and the models — kept current.

Most existing lists in this space are computational/model-centric. This one foregrounds the **experimental technologies** (Perturb-seq, Perturb-multiome, Perturb-spatial, sgRNA library design, cell→guide assignment) alongside analysis and prediction, and aims to stay up to date. It picks up where the excellent but now-dormant [theislab/sc-pert](https://github.com/theislab/sc-pert) (last updated 2022) left off.

Maintained by [Xiangjie Zhao](https://cadenzhao.github.io), who builds perturbation-enabled single-cell and spatial multi-omics technologies.

> **Status: v0 scaffold.** Entries below are real, established methods/tools; some links are still being verified and filled in. Contributions welcome — see [Contributing](#contributing).

## Contents

- [Reviews & Perspectives](#reviews--perspectives)
- [Experimental Methods](#experimental-methods)
  - [Transcriptome (Perturb-seq family)](#transcriptome-perturb-seq-family)
  - [Chromatin & Epigenome](#chromatin--epigenome)
  - [Multimodal](#multimodal)
  - [Spatial Perturbation](#spatial-perturbation)
  - [Scalable & Targeted Variants](#scalable--targeted-variants)
- [sgRNA Design & Libraries](#sgrna-design--libraries)
- [Computational Analysis](#computational-analysis)
- [Perturbation Prediction & Models](#perturbation-prediction--models)
- [Foundation Models](#foundation-models)
- [Datasets & Databases](#datasets--databases)
- [Related Lists](#related-lists)
- [Contributing](#contributing)
- [License](#license)

## Reviews & Perspectives

- **A new era in functional genomics screens** — Przybyla & Gilbert, *Nat Rev Genet* 2022.
- **Mapping genome-wide genetic interactions with single-cell readouts** — overview of pooled CRISPR + single-cell.
- **Perturbation-based single-cell genomics: assays, scale, and analysis** — survey of the design space.

## Experimental Methods

### Transcriptome (Perturb-seq family)

- **Perturb-seq** — pooled CRISPR screens with single-cell RNA-seq readout. Dixit et al. & Adamson et al., *Cell* 2016.
- **CRISP-seq** — CRISPR pooled screen with scRNA-seq in immune cells. Jaitin et al., *Cell* 2016.
- **CROP-seq** — guide captured directly in the polyadenylated transcript. Datlinger et al., *Nat Methods* 2017.
- **Direct-capture Perturb-seq** — capture sequences enabling multiplexed guide detection. Replogle et al., *Nat Biotechnol* 2020.
- **Genome-scale Perturb-seq** — whole-genome single-cell perturbation atlas. Replogle et al., *Cell* 2022.

### Chromatin & Epigenome

- **Perturb-ATAC** — CRISPR perturbation with single-cell ATAC readout. Rubin et al., *Cell* 2019.
- **Spear-ATAC** — scalable scATAC-based perturbation screening.
- **CRISPR-sciATAC** — combinatorial-indexing ATAC with perturbation.

### Multimodal

- **Perturb-CITE-seq** — perturbation with joint transcriptome + surface protein. Frangieh et al., *Nat Genet* 2021.
- **ECCITE-seq** — CRISPR + CITE-seq + clonal/hashing readouts. Mimitou et al., *Nat Methods* 2019.
- **Perturb-multiome** — joint RNA + ATAC readout of perturbations.

### Spatial Perturbation

- **Perturb-map** — spatially resolved pooled CRISPR screening in tissue. Dhainaut et al., *Cell* 2022.
- **In situ / imaging-based perturbation readouts** — optical pooled screening (Feldman et al., *Cell* 2019) and successors.

### Scalable & Targeted Variants

- **TAP-seq** — targeted Perturb-seq, sensitive readout of focused gene panels. Schraivogel et al., *Nat Methods* 2020.
- **CaRPool-seq** — Cas13-based combinatorial perturbation.
- **MOSAIC-seq / others** — enhancer-focused pooled perturbation.

## sgRNA Design & Libraries

- **CRISPOR** — guide design with off-target and efficiency scoring. <http://crispor.tefor.net>
- **CHOPCHOP** — web tool for CRISPR/Cas guide selection. <https://chopchop.cbu.uib.no>
- **GuideScan2** — genome-wide gRNA design and specificity.
- **FlashFry** — fast, scriptable off-target discovery.
- **Brunello / Brie / Bassik libraries** — widely used genome-scale knockout/CRISPRi/a libraries.

## Computational Analysis

- **Mixscape** — identify and remove cells that escaped perturbation (in Seurat). Papalexi et al., *Nat Genet* 2021.
- **MIMOSCA** — regression framework from the original Perturb-seq paper.
- **scMAGeCK** — link guides to single-cell phenotypes.
- **SCEPTRE** — rigorously calibrated association testing for single-cell CRISPR screens.
- **Normalisr** — association testing with proper normalization for pooled screens.

## Perturbation Prediction & Models

- **GEARS** — graph-based prediction of transcriptional response to (combinatorial) perturbations. Roohani et al., *Nat Biotechnol* 2023. <https://github.com/snap-stanford/GEARS>
- **CPA (Compositional Perturbation Autoencoder)** — disentangle and predict perturbation responses. Lotfollahi et al., *Mol Syst Biol* 2023.
- **scGen** — latent-space prediction of perturbation response. Lotfollahi et al., *Nat Methods* 2019. <https://github.com/theislab/scgen>
- **chemCPA** — generalize to unseen drug perturbations.
- **Biolord / SAMS-VAE / PerturbNet** — disentanglement and generative approaches.

## Foundation Models

- **scGPT**, **Geneformer**, **scFoundation** — single-cell foundation models with perturbation-prediction tasks.
- See also: [OmicsML/awesome-foundation-model-single-cell-papers](https://github.com/OmicsML/awesome-foundation-model-single-cell-papers).

## Datasets & Databases

- **scPerturb** — harmonized collection of single-cell perturbation datasets with standardized metrics. Peidli et al., *Nat Methods* 2024.
- **Genome-scale Perturb-seq atlas** — Replogle et al. 2022 dataset.
- **PerturBase** and similar portals — searchable perturbation datasets.

## Related Lists

- [theislab/sc-pert](https://github.com/theislab/sc-pert) — models & datasets for perturbational single-cell omics (dormant since 2022; this list aims to continue its mission).
- [OmicsML/awesome-foundation-model-single-cell-papers](https://github.com/OmicsML/awesome-foundation-model-single-cell-papers)
- [xianglin226/Benchmarking-Single-Cell-Perturbation](https://github.com/xianglin226/Benchmarking-Single-Cell-Perturbation)
- [seandavi/awesome-single-cell](https://github.com/seandavi/awesome-single-cell)

## Contributing

PRs welcome. Add an entry as `**Name** — one-line description. Author et al., *Journal* Year. <link>`. Keep it to genuinely useful, established or notable resources; prefer a primary link (repo or paper). Group by the existing sections.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE) — to the extent possible under law, the maintainer has waived all copyright to this curated list (CC0 1.0).
