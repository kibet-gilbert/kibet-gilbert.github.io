---
layout: page
title: "Waste Water Based Epidemiological Surveillance (WBE)"
year: 2024
importance: 1
category: work
related_publications: true
tags: ["Waste Water", "metagenomics", "pathogen surveillance", "Epidemiology"]
description: This is the workflow we employ in the analysis of sequences with the goal of tracking pathogens of public health interest so as to inform on rapid response. Because a quick turn around is needed, the computational steps taken and fast to ensure feedback is provided in time.
img: /assets/img/ww_shotgun_metagenomics_workflow.png
links:
  github: https://github.com/ILRI-Genomics-Platform/wastewater-Meta-Genomic-Pathogen-Surveillance
  pdf: /assets/pdf/pipeline_poster.pdf
---

## Overview

This pipeline was developed based on **Nextflow + Singularity** to analysisd shotgun metagenomic NGS data for monitoring pathogens in wastewater across selected sites in Mombasa and Kisumu, Kenya. The work was done at [ILRI](https://www.ilri.org/) through its [Genomics Platform](https://www.ilri.org/research/facilities/genomics-platform).

## Sampling & Workflow

* Modular steps: Prefetch → QC → Assembly → Taxonomy → AMR
* Containerised with BioContainers
* Automated MultiQC reports & Slack alerts

- **Sequence data** from Illumina NextSeq is processed through a custom pipeline similar to [nf-core/MAG](https://nf-co.re/mag/): QC, human filtering, and taxonomic classification with Kraken2 and Centrifuge.
- **Taxonomic reports** are merged and filtered via [pavian](https://github.com/fbreitwieser/pavian) in R to generate relative and absolute abundance profiles.

## Pathogens of Interest

Lists of target organisms are curated and updated. See:
- Pathogenic Bacteria
- Pathogenic Viruses
- Pathogenic Parasites

Antimicrobial resistance gene detection using CARD/RGI is also under development.

## Resources

> This project is under active development. For details, see the Bioinformatics Workflow pdf.
