# Aaron O'Brien

Bioinformatician at the Centro de Biotecnología de Sistemas, Universidad Andrés Bello, in Santiago, Chile. I help biologists turn DNA sequencing into answers about fungi and other microbes: which ones are in a sample, how much of each, and which ones nobody has named yet. Along the way I write Rust tools for long-read rRNA metabarcoding and run the centre's Nanopore amplicon work, 16S and ITS, from library handoff to the report the biologist actually opens.

### Tools

**[ITSxRust](https://github.com/ayobi/ITSxRust)** finds the fungal barcode in each long read, and tells you why when it can't. It extracts ITS1, 5.8S and ITS2 from Nanopore and PacBio amplicons by chaining four profile-HMM anchors, and falls back to two-anchor pairs when a read is missing a flank, so every region returned has a model boundary on both sides. Failures come back as structured codes and a per-sample QC summary. Included in `nf-core/ampliseq`.
Published in *Methods in Ecology and Evolution* 17: 2843–2853 (2026) · [paper](https://doi.org/10.1111/2041-210x.70393) · [Bioconda](https://anaconda.org/bioconda/itsxrust)

**[EMITS](https://github.com/ayobi/emits)** estimates how much of each fungal species is in a sample. It runs expectation-maximization over minimap2 alignments against UNITE, so reads that fit several references are shared between them by the evidence instead of handed to the best hit, and abundance isn't fragmented across redundant accessions.
Published in *Methods in Ecology and Evolution* (2026) · [paper](https://doi.org/10.1111/2041-210x.70418) · [preprint](https://doi.org/10.64898/2026.03.31.715662) · [Bioconda](https://anaconda.org/bioconda/emits)

**[SSUplex](https://github.com/ayobi/ssuplex)** sorts ribosomal reads by where they came from: bacteria, archaea, eukaryotes, mitochondria or chloroplasts. It extracts small-subunit rRNA from environmental reads on either strand, so host and organelle DNA is counted apart from the community you meant to study.
In revision at *Bioinformatics Advances* · [preprint](https://doi.org/10.64898/2026.07.02.736232) · [Bioconda](https://anaconda.org/channels/bioconda/packages/ssuplex/overview) · [v0.2.0 archive](https://doi.org/10.5281/zenodo.23246210)

### Research

Much of the fungal DNA in a soil sample belongs to genera no reference database has a name for, yet classifiers still hand back a name. Three companion studies ask how often those names are wrong and how to flag sequences that are genuinely new. All three are under review:

- **A learned fungal ITS embedding does not outperform correctly configured alignment in open-world evaluation**, with Auguste Gardette. *Methods in Ecology and Evolution*.
- **Classical baselines outperform released deep-learning ITS classifiers, which collapse on ITS2 where predictions follow the flanking regions**, with Auguste Gardette, César Marín and Pilar Parada. *Briefings in Bioinformatics* · [preprint, earlier version](https://doi.org/10.64898/2026.07.29.741510) · [code](https://github.com/ayobi/its-classifier-audit)
- **A calibrated novelty flag for fungal ITS metabarcoding: choosing the error rate at which sequences are declared new**, with César Marín and Pilar Parada. *IMA Fungus* · [preprint](https://doi.org/10.64898/2026.07.29.741524) · [code](https://github.com/ayobi/its-novelty)

### In the lab

Amplicon pipelines in Snakemake and Nextflow with PICRUSt2 profiling and interactive D3 reports, like this [vineyard soil microbiome dashboard](https://ayobi.github.io/aaron-obrien/vineyard-soils.html) built for Bárbara Ojeda's thesis. Also a LIMS for sample tracking and BioBalance, a metal-balance and recovery app for bioleaching campaigns, both running at the centre.

Mostly Rust and Python; FastAPI, PostgreSQL, React and D3 on the web side; Snakemake, Nextflow, QIIME2 and SLURM on the pipeline side.

### Elsewhere

- Site, in English and Spanish: [ayobi.github.io/aaron-obrien](https://ayobi.github.io/aaron-obrien/)
- ORCID: [0009-0008-4742-4683](https://orcid.org/0009-0008-4742-4683)
- LinkedIn: [in/aarongobrien](https://linkedin.com/in/aarongobrien)
- Earlier work: [PEPhub](https://doi.org/10.1093/gigascience/giae033) (*GigaScience*, 2024) with the Sheffield lab at UVA
- Email: [obrien.aaron.g@gmail.com](mailto:obrien.aaron.g@gmail.com)

Open to collaborations where solid engineering moves the science along: long-read metabarcoding, pipeline work, or a dataset that needs the analysis to hold up. Write to me in English or Spanish.
