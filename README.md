# Genome-Mining-CIIMAR-2025
Materials for the hands-on session 'Workflows for natural product genome mining with antiSMASH, BiG-SCAPE and MIBiG', of the CIIMAR short course Bioinformatics for Natural Product Discovery 2025

This hands-on session features three main tools/resources:
- antiSMASH (online)
- BiG-SCAPE (offline, on your laptop or server)

In this repo you'll find the materials for the antiSMASH part of this hands-on session. We recommend you start with this section.
Once you're done, or approximately 1hr into the session, we'll switch over to the BiG-SCAPE, find the materials for that part [here](https://github.com/CatarinaCarolina/BiG-SCAPE-workshop).

## antiSMASH Documentation

The official documentation for antiSMASH can be found [here](https://docs.antismash.secondarymetabolites.org).
See a supporting document with a demo of the antiSMASH online webserver [here](). Use this file to guide your exploration of antiSMASH.

## antiSMASH Exercises

To save time for today, we only will work with the pre-computed antiSMASH example record for Streptomyces coelicolor instead of uploading/running individual sequences.

### Exercise 1: secondary metabolite gene clusters of Streptomyces coelicolor

As an example, we will analyze the secondary metabolite gene clusters of the model organism Streptomyces coelicolor, which is provided as pre-computed demo data:

#### Load S. coelicolor demo data

1.	Open [antiSMASH](http://antismash.secondarymetabolites.org/) in your web browser
2.	Click “Open example output”

#### Cluster overview table

When the analysis is finished, a table of identified clusters is displayed
1.	Select individual clusters by clicking either on the colored boxes or on the colored “Cluster XXX” button
2.	Return to the overview table by clicking on “Overview”

#### Cluster details

1.	Browse through the different clusters; use the interactive page and get a feeling by clicking on the genes in the “Gene Cluster description”, Detailed annotation, and “Homologous (Sub)cluster” panels.
2.	Try links to blast or other services that appear on the dropdown windows when clicking on genes/domains.
3.	Analyze the CDA gene cluster (Cluster 10)
4.	Extract the predicted sequence of the peptide from the antiSMASH results.
5.	Compare the predicted amino acid sequence with the [experimentally determined structure](https://doi.org/10.1016/s1074-5521(02)00252-1).
6.	Find other organisms, which might produce similar compounds.
7.	Find the genes in the CDA gene cluster, which code for enzymes involved in the biosynthesis of the non-proteinogenic amino acid hydroxyphenylglycine (hpg).


### Exercise 2: Bacillus velezensis (amyloliquefaciens) FZB42 - (RefSeq accession: NC_009725.2)

1.	Find and download the Bacillus velezensis FZB42 genome from NCBI
2.	Run antiSMASH with the genome
3.	Analyze the data as discussed above.

#### Questions:
- How many BGCs does B. velezensis have?
- Which are PKS / NRPS / hybrid products
- Which compounds are known?
- Can you find these BGCs in [antiSMASH DB](https://antismash-db.secondarymetabolites.org/)? and in [MIBiG](https://mibig.secondarymetabolites.org/)?


Now, we'll switch over to the BiG-SCAPE, find the materials for that part [here](https://github.com/CatarinaCarolina/BiG-SCAPE-workshop).






