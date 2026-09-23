# HUPO-2026-C-HPP-Bioinformatics-tools-glycosylation-PTM-and-protein-function
## HUPO Bioinformatics HUB, September 30, 2026

*Time*: **10:30-12:00**
*Location*: **room 330**
Organizers: Heeyoun Hwang (KBSI), Peter Horvatovich (UG)

## Title: C-HPP Bioinformatics tools, glycosylation, PTM and protein function

## Program

| Time | Speaker | Talk |
|:-----|:--------|:-----|
| **10:30–10:31** | **Heeyoun Hwang / Peter Horvatovich** | **Welcome and session introduction** *(1 slide)* |
| 10:31–10:51 | Gong Zhang *(Jinan University)* | The HPP Portal and resources for protein function characterisation |
| 10:51–11:06 | Ju-Yeon Lee *(KBSI)* or Yuan Li *(TBC)* | Glycopeptide identification (IQ-GPA) |
| 11:06–11:21 | Peter Horvatovich *(University of Groningen)* | GlycoGenius: Automated and High-Throughput Analysis of Glycomics Mass Spectrometry Data |
| 11:21–11:31 | Arthur Declercq *(VIB-UGent, CompOmics)* | Mumble and MS²Rescore: localizing mass shifts using modification-aware peptide property predictions |
| 11:31–11:41 | Pathmanaban Ramasamy *(VIB-UGent, CompOmics)* | Scop3PTM: integrating proteomics evidence, structural biology and residue-level biophysical properties for mechanistic interpretation of post-translational modifications |
| 11:41–12:00 | All speakers; moderated by Heeyoun Hwang and Peter Horvatovich | Panel discussion: how completely can we characterise protein function? |

## Abstracts
**Peter Horvatovich**
Glycan analysis remains challenging because of the high structural complexity of glycans, including isobaric monosaccharides, branching, linkage and positional isomers, and extensive heterogeneity. Consequently, interpretation of CE/LC-MS(/MS) data often relies on labor-intensive manual inspection, expert-defined rules, and the integration of multiple software tools. GlycoGenius was developed to streamline and automate this workflow, enabling glycan analysis directly from raw mass spectrometry data within a single, user-friendly platform [1].
GlycoGenius automatically constructs customizable glycan composition search spaces, traces extracted ion chromatograms/electropherograms, detects and quantifies individual glycan peaks, evaluates isotopic-pattern and peak-shape quality, and filters identifications according to user-defined criteria. Quantification is based on peak areas from the original data, allowing multiple coexisting or non-coeluting isobaric species to be evaluated separately. The software also supports automated MS/MS fragment annotation and provides interactive visualization of raw spectra, chromatograms/electropherograms, isotopic envelopes, and quality metrics, facilitating rapid visual verification of assignments. Results can be explored across multiple samples and exported as quantitative tables and publication-ready figures, including SNFG representations. The platform supports N- and O-glycans, glycosaminoglycans, and chemically modified glycans, including different reducing-end labels and sulfation/phosphorylation.
In the validation presented in the 2025 Nature Communications study, GlycoGenius reproduced expert-generated glycomic profiles while reducing analysis time. For a human plasma CE-MS/MS dataset, it identified 174 N-glycan compositions meeting predefined quality criteria, including 59 compositions not reported in the original study; 46 of these were not found in the literature examined. Analysis of an O-glycan dataset identified 25 compositions meeting the quality criteria, including nine not reported previously.
GlycoGenius therefore provides an integrated, transparent and scalable workflow from raw CE/LC-MS(/MS) data to validated quantitative glycomic profiles and publication-ready visualizations, reducing manual data processing while facilitating expert inspection and biological interpretation.

**Arthur Declercq**
Post-translational modifications (PTMs) regulate protein function, yet standard proteomics searches only identify modifications specified before the search, and even for expected modifications such as phosphorylation, deciding which residue carries the modification remains error-prone. Open modification searching lifts the first restriction by allowing unrestricted precursor mass shifts, but leaves each shift unexplained and its site unknown. Turning these shifts into confidently identified and correctly localized peptidoforms is the main obstacle to data-driven PTM discovery.
We present the integration of Mumble into MS²Rescore. Mumble enumerates all Unimod modifications, amino acid substitutions, and their combinations that explain an observed mass shift within tolerance, and localizes each to its chemically valid sites, expanding every shifted peptide-spectrum match (PSM) into explicit candidate peptidoforms. MS²Rescore then scores all candidates with modification-aware predictors of fragment ion intensity, retention time, and collisional cross section, together with fragment-level features that only become informative once the modification is explicit, such as modification-specific neutral losses and the ions flanking the modified residue. Candidates that differ only in modification or in site therefore receive different predictions. Lastly, all candidates of a spectrum compete in a final ranking step that assigns confidence to each candidate, both for the modification and its localisation.
Applied to phosphopeptide-enriched data, this ranking selects plausible sites, provides a confidence estimate per site, and reduces false identifications such as near-isobaric sulfation hits, while leaving the number of identifications at 1% false discovery rate unchanged. Modification-aware features thus allow mass shifts to be localized in a data-driven way, both for unexpected modifications and for expected ones where the search engine cannot decide between candidate sites.

**Pathmanaban Ramasamy**
Public repositories contain millions of experimentally identified post-translational modifications (PTMs), yet their mechanistic interpretation is limited by fragmented proteomics, structural and residue-level annotations. Scop3PTM is an open FAIR knowledgebase that integrates experimentally identified human PTMs with complete proteomics evidence, protein structures, conformational diversity, biophysical properties, genetic variation and disease annotations. It was generated through uniform reprocessing of 543 human PRIDE projects, yielding 6,785,349 PTM observations across 19,973 proteins. These observations map to 2,175,288 unique modified residues and ~300 PTM chemistries, with full traceability through peptidoforms, PSMs, runs, projects and Universal Spectrum Identifiers. PTM sites are linked to experimental PDB structures, AlphaFold models, PDBe-KB conformational clusters, CATH classifications and residue-level molecular context. Proteome-wide analyses revealed enrichment of biological PTMs at residues undergoing local conformational switching and modification-specific preferences across protein fold space. Scop3PTM therefore enables direct progression from raw spectra to structural and mechanistic interpretation of PTM-mediated protein regulation at proteome scale.

## Reference
[1] Loponte, H. F., Zheng, J., Ding, Y., et al. **GlycoGenius: a streamlined high-throughput glycan composition identification tool.** *Nature Communications* **16**, 10335 (2025). https://doi.org/10.1038/s41467-025-65265-2
