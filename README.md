# Awesome Perturbation Omics [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated, **technology-forward** map of single-cell and spatial perturbation omics — the assays, the library design, the analysis, and the models — kept current.

Most existing lists in this space are computational/model-centric. This one foregrounds the **experimental technologies** (Perturb-seq, Perturb-multiome, Perturb-spatial, sgRNA library design, cell→guide assignment) alongside analysis and prediction, and aims to stay up to date. It picks up where the excellent but now-dormant [theislab/sc-pert](https://github.com/theislab/sc-pert) (last updated 2022) left off.

Maintained by [Xiangjie Zhao](https://cadenzhao.github.io), who builds perturbation-enabled single-cell and spatial multi-omics technologies.

> **Status: actively expanding (v0.2).** A broad first pass weighted toward high-impact (IF > 10) venues — *Cell*, *Nature*, *Science*, *Nat Methods / Biotechnol / Genetics*, *Genome Biology*, *Nat Rev Genet*, etc. Journals and years are sourced from PubMed/CrossRef; **a few first-author attributions and links are still being verified.** Contributions and corrections welcome — see [Contributing](#contributing).

## Contents

- [Reviews & Perspectives](#reviews--perspectives)
- [Experimental Methods](#experimental-methods)
  - [Transcriptome (Perturb-seq family)](#transcriptome-perturb-seq-family)
  - [Chromatin, Epigenome & Multiome](#chromatin-epigenome--multiome)
  - [Multimodal](#multimodal)
  - [Combinatorial, Scalable & Targeted](#combinatorial-scalable--targeted)
  - [In vivo Perturbation](#in-vivo-perturbation)
  - [Spatial Perturbation](#spatial-perturbation)
  - [Optical / Image-based Screens](#optical--image-based-screens)
- [Applications](#applications)
  - [Non-coding & GWAS Regulatory Screens](#non-coding--gwas-regulatory-screens)
  - [Coding-variant & Base-editing Screens](#coding-variant--base-editing-screens)
  - [Transcription Factors & Differentiation](#transcription-factors--differentiation)
  - [Chemical / Drug Perturbation](#chemical--drug-perturbation)
- [sgRNA Design & Libraries](#sgrna-design--libraries)
- [Computational Analysis](#computational-analysis)
- [Perturbation Prediction & Models](#perturbation-prediction--models)
- [Benchmarks & Evaluation](#benchmarks--evaluation)
- [Foundation Models](#foundation-models)
- [Datasets & Databases](#datasets--databases)
- [Related Lists](#related-lists)
- [Contributing](#contributing)
- [License](#license)

## Reviews & Perspectives

- **Genome-scale single-cell CRISPR screens** — overview of design, scale, and analysis. Przybyla & Gilbert, *Nat Rev Genet* 2022. <https://doi.org/10.1038/s41576-022-00517-1>
- **A new era in functional genomics screens** — perspective on pooled CRISPR + single-cell readouts. Przybyla & Gilbert, *Nat Rev Genet* 2022.
- **Perturbation-based single-cell genomics: assays, scale, and analysis** — survey of the design space.

## Experimental Methods

### Transcriptome (Perturb-seq family)

- **Perturb-seq** — pooled CRISPR screens with single-cell RNA-seq readout. Dixit et al. & Adamson et al., *Cell* 2016.
- **CRISP-seq** — CRISPR pooled screen with scRNA-seq in immune cells. Jaitin et al., *Cell* 2016.
- **CROP-seq** — guide captured directly in the polyadenylated transcript. Datlinger et al., *Nat Methods* 2017.
- **Direct-capture Perturb-seq** — capture sequences enabling multiplexed guide detection and dual-guide screens. Replogle et al., *Nat Biotechnol* 2020. <https://doi.org/10.1038/s41587-020-0470-y>
- **Genome-scale Perturb-seq** — whole-genome single-cell CRISPRi atlas (~2.5M cells, K562). Replogle et al., *Cell* 2022.
- **Scalable pooled CRISPR scRNA profiling** — dissecting regulators of transcriptome kinetics at scale. *Nat Biotechnol* 2023. <https://doi.org/10.1038/s41587-023-01948-9>

### Chromatin, Epigenome & Multiome

- **Perturb-ATAC** — CRISPR perturbation with single-cell ATAC readout. Rubin et al., *Cell* 2019.
- **Spear-ATAC** — scalable scATAC-based perturbation screening.
- **CRISPR-sciATAC** — combinatorial-indexing ATAC with perturbation.
- **Multiome Perturb-seq** — scalable joint RNA + ATAC readout of perturbations (transcriptome + epigenome). *Cell Systems* 2024. <https://www.cell.com/cell-systems/fulltext/S2405-4712(24)00366-1>

### Multimodal

- **Perturb-CITE-seq** — perturbation with joint transcriptome + surface protein; immune-evasion screen in melanoma. Frangieh et al., *Nat Genet* 2021.
- **ECCITE-seq** — CRISPR + CITE-seq + clonal/hashing readouts. Mimitou et al., *Nat Methods* 2019.
- **Multimodal immune-checkpoint screen** — multimodal single-cell screens of inhibitory checkpoints (introduces the Mixscape workflow). Papalexi et al., *Nat Genet* 2021. <https://doi.org/10.1038/s41588-021-00778-2>

### Combinatorial, Scalable & Targeted

- **TAP-seq** — targeted Perturb-seq, sensitive readout of focused gene panels. Schraivogel et al., *Nat Methods* 2020.
- **CaRPool-seq** — Cas13d RNA-targeting, efficient combinatorial perturbation with multimodal readout. Wessels et al., *Nat Methods* 2022. <https://doi.org/10.1038/s41592-022-01705-x>
- **Compressed Perturb-seq** — random multiplexed perturbations decompressed via sparse regulatory structure; ~10× cheaper, more power for genetic interactions. *Nat Biotechnol* 2023. <https://doi.org/10.1038/s41587-023-01964-9>
- **MOSAIC-seq** — enhancer-focused pooled perturbation with single-cell readout. Xie et al., *Mol Cell* 2017.

### In vivo Perturbation

- **In vivo Perturb-Seq (autism risk genes)** — neuronal/glial abnormalities of 35 ASD/ND risk genes in the developing mouse brain. Jin et al., *Science* 2020.
- **AAV-Perturb-seq** — transcriptional linkage analysis with in vivo AAV-delivered Perturb-seq. Santinha et al., *Nature* 2023.
- **Massively parallel in vivo Perturb-seq** — AAV + transposon scaling; cell-type-specific networks in cortical development. *Cell* 2024. <https://pubmed.ncbi.nlm.nih.gov/37790302/>

### Spatial Perturbation

- **SPAC-seq** — high-throughput spatial CRISPR screen sequencing; paired with **TARDIS**, a statistical toolkit for spatial perturbation analysis. Zhang et al. (Zeng lab), *Cell* 2026. <https://doi.org/10.1016/j.cell.2026.04.049>
- **Spatial Perturb-seq** — in vivo single-cell CRISPR readout within intact tissue architecture (Stereo-seq based), demonstrated in mouse brain. Shen et al. (Chew lab), *Nat Commun* 2026. <https://doi.org/10.1038/s41467-026-69677-6>
- **Perturb-Multimodal (Perturb-MM)** — pooled genetic screens with joint imaging + sequencing readout in intact mammalian tissue. Saunders et al. (Zhuang lab), *Cell* 2025. <https://doi.org/10.1016/j.cell.2025.05.022>
- **Spatial CRISPR screening + transcriptomics** — simultaneous pooled screening and spatial transcriptomics revealing intra-/intercellular transcriptional circuits. Binan et al. (Farhi lab), *Cell* 2025. <https://doi.org/10.1016/j.cell.2025.02.012>
- **Perturb-map** — spatially resolved pooled CRISPR screening in tissue. Dhainaut et al., *Cell* 2022.

### Optical / Image-based Screens

- **Optical pooled screening (OPS)** — in situ sequencing of guide barcodes linked to imaging phenotypes at single-cell scale. Feldman et al., *Cell* 2019.
- **High-content imaging-based pooled CRISPR screens** — genome-scale subcellular-localization/morphology screens. Funk et al., *J Cell Biol* 2021.
- **Perturb-FISH** — MERFISH imaging spatial transcriptomics with in situ guide RNA detection; recovers intra- and intercellular effects.

## Applications

### Non-coding & GWAS Regulatory Screens

- **Genome-wide enhancer Perturb-seq** — framework for mapping enhancer→gene regulation via CRISPRi single-cell screens (~6k enhancers). Gasperini et al., *Cell* 2019.
- **STING-seq** — single-cell CRISPRi of GWAS noncoding loci to nominate target genes (blood-trait loci). Morris et al., *Science* 2023.
- **Single-cell CRISPR screen for GWAS loci** — mapping target genes/pathways at GWAS loci. *Nat Genet* 2023. <https://doi.org/10.1038/s41588-023-01432-9>

### Coding-variant & Base-editing Screens

- **Variant Perturb-seq (TP53/KRAS)** — massively parallel phenotyping of cancer coding variants with single-cell readout. Ursu et al., *Nat Biotechnol* 2022.
- **Base-editing scRNA (hematopoiesis)** — massively parallel base editing to map variant effects in human hematopoiesis. Martin-Rufino et al., *Cell* 2023.

### Transcription Factors & Differentiation

- **TF Atlas of directed differentiation** — overexpression of 1,836 TFs in hESCs with scRNA-seq readout. Joung et al., *Cell* 2023. <https://www.cell.com/cell/fulltext/S0092-8674(22)01470-2>
- **In vivo gain-of-function Perturb-seq (astrocytes)** — mapping TF functions in astrocytes in vivo. *Science* 2025. <https://doi.org/10.1126/science.adw2156>
- **TF perturbations → fibroblast states** — comprehensive TF perturbations recapitulate fibroblast transcriptional states. *Nat Genet* 2025. <https://doi.org/10.1038/s41588-025-02284-1>
- **Atlas-guided TF discovery for T-cell programming** — *Nature* 2025. <https://doi.org/10.1038/s41586-025-09989-7>

### Chemical / Drug Perturbation

- **sci-Plex** — nuclear hashing for massively multiplexed chemical transcriptomics at single-cell resolution (~5k samples, 188 compounds). Srivatsan et al., *Science* 2020. <https://doi.org/10.1126/science.aax6234>

## sgRNA Design & Libraries

- **CRISPOR** — guide design with off-target and efficiency scoring. <http://crispor.tefor.net>
- **CHOPCHOP** — web tool for CRISPR/Cas guide selection. <https://chopchop.cbu.uib.no>
- **GuideScan2** — genome-wide gRNA design and specificity.
- **FlashFry** — fast, scriptable off-target discovery.
- **Brunello / Brie / Bassik libraries** — widely used genome-scale knockout/CRISPRi/a libraries.

## Computational Analysis

- **Mixscape** — identify and remove cells that escaped perturbation (in Seurat). Papalexi et al., *Nat Genet* 2021.
- **SCEPTRE** — calibrated association testing for single-cell CRISPR screens via conditional resampling. Barry et al., *Genome Biol* 2021. <https://doi.org/10.1186/s13059-021-02545-2>
- **SCEPTRE (low-MOI)** — robust differential-expression testing at low multiplicity of infection. *Genome Biol* 2024. <https://doi.org/10.1186/s13059-024-03254-2>
- **MIMOSCA** — regression framework from the original Perturb-seq paper.
- **scMAGeCK** — link guides to single-cell phenotypes.
- **Normalisr** — association testing with proper normalization for pooled screens.
- **Differential expression in perturbation atlases** — transcriptome-wide DE testing across large perturbation atlases. *Nat Genet* 2025. <https://doi.org/10.1038/s41588-025-02169-3>

## Perturbation Prediction & Models

- **GEARS** — graph-based prediction of transcriptional response to (combinatorial) perturbations. Roohani et al., *Nat Biotechnol* 2023. <https://doi.org/10.1038/s41587-023-01905-6>
- **CPA (Compositional Perturbation Autoencoder)** — predict responses to complex/combinatorial perturbations. Lotfollahi et al., *Mol Syst Biol* 2023. <https://doi.org/10.15252/msb.202211517>
- **scGen** — latent-space prediction of perturbation response. Lotfollahi et al., *Nat Methods* 2019.
- **chemCPA** — transfer learning to generalize to unseen drug perturbations.
- **Biolord** — disentangled representations for chemical and genetic perturbation prediction. *Nat Biotechnol* 2024.
- **PerturbNet** — predict single-cell responses to unseen chemical and genetic perturbations. *Mol Syst Biol* 2025. <https://doi.org/10.1038/s44320-025-00131-3>
- **Causal combinatorial prediction** — causally inspired neural networks for therapeutic perturbation combinations. *Nat Biomed Eng* 2025. <https://doi.org/10.1038/s41551-025-01481-x>
- **Deep generative drug-response model** — predict transcriptional responses to novel chemicals. *Nat Commun* 2024. <https://doi.org/10.1038/s41467-024-53457-1>

## Benchmarks & Evaluation

- **Generalizable prediction benchmark** — 27 methods × 29 datasets × 6 metrics, including foundation models. *Nat Methods* 2025. <https://doi.org/10.1038/s41592-025-02980-0>
- **Linear-baseline benchmark** — deep-learning perturbation prediction does not yet beat simple linear baselines. *Nat Methods* 2025. <https://doi.org/10.1038/s41592-025-02772-6>
- **Systema** — evaluating perturbation-response prediction beyond systematic variation. *Nat Biotechnol* 2025. <https://doi.org/10.1038/s41587-025-02777-8>
- **scPerturBench** — single-cell perturbation-effect prediction benchmark. <https://github.com/bm2-lab/scPerturBench>

## Foundation Models

- **Geneformer** — transfer-learning transcriptomic foundation model with in silico perturbation. Theodoris et al., *Nature* 2023.
- **scGPT** — generative foundation model for single-cell multi-omics; perturbation-prediction tasks. Cui et al., *Nat Methods* 2024. <https://doi.org/10.1038/s41592-024-02201-0>
- **scFoundation** — large-scale pretrained model for single-cell expression. Hao et al., *Nat Methods* 2024.
- See also: [OmicsML/awesome-foundation-model-single-cell-papers](https://github.com/OmicsML/awesome-foundation-model-single-cell-papers).

## Datasets & Databases

- **scPerturb** — 44+ harmonized single-cell perturbation datasets (transcriptomics/proteomics/epigenomics) with E-distance metrics. Peidli et al., *Nat Methods* 2024. <https://doi.org/10.1038/s41592-023-02144-y>
- **Genome-scale Perturb-seq atlas** — Replogle et al. 2022 dataset (K562 / RPE1 genome-wide).
- **TF Atlas** — Joung et al. 2023 overexpression atlas (1,836 TFs), GEO GSE216481.
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
