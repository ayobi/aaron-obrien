# Aaron O'Brien

Bioinformatics and software engineering at the Centro de Biotecnología de Sistemas, Universidad Andrés Bello, in Santiago. I write Rust tooling for long-read rRNA metabarcoding and run the Nanopore amplicon work that goes with it — 16S and ITS, from library handoff to the report the biologist actually opens.

### Tools

**[ITSxRust](https://github.com/ayobi/ITSxRust)** — extracts ITS1, 5.8S and ITS2 from Nanopore and PacBio amplicons. Chains four profile-HMM anchors and falls back to two-anchor pairs when a read is missing a flank, so every region returned has a model boundary on both sides. Failures come back as structured codes and a per-sample QC summary. Packaged on Bioconda and included in `nf-core/ampliseq`.
[Methods in Ecology and Evolution, 2026](https://doi.org/10.1111/2041-210x.70393)

**[EMITS](https://github.com/ayobi/emits)** — species-level abundance estimation for fungal ITS communities. Runs expectation-maximization over minimap2 alignments against UNITE so reads that fit several references are split probabilistically rather than handed to the best hit, and abundance isn't fragmented across redundant accessions.
[Accepted at Methods in Ecology and Evolution; preprint](https://doi.org/10.64898/2026.03.31.715662)

**SSUplex** — both-strand small-subunit rRNA extraction and origin-sorting for environmental DNA metabarcoding.
[Preprint](https://doi.org/10.64898/2026.07.02.736232)

### Also

Amplicon pipelines in Snakemake and Nextflow with interactive D3 reporting, a LIMS for lab sample tracking, and a balance-and-recovery app for bioleaching campaigns — all running at the centre.

Mostly Rust and Python; FastAPI, PostgreSQL, React and D3 on the web side; Snakemake, Nextflow, QIIME2 and SLURM on the pipeline side.

### Elsewhere

- Site: [ayobi.github.io/aaron-obrien](https://ayobi.github.io/aaron-obrien/)
- ORCID: [0009-0008-4742-4683](https://orcid.org/0009-0008-4742-4683)
- Earlier work: [PEPhub](https://doi.org/10.1093/gigascience/giae033) (GigaScience, 2024) with the Sheffield lab at UVA
- obrien.aaron.g@gmail.com

Open to collaborations where solid engineering moves the science along — long-read metabarcoding, pipeline work, or a dataset that needs the analysis to hold up.
