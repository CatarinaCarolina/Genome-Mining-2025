# Genome Mining workshop 2025
Materials for the hands-on session 'Workflows for natural product genome mining with antiSMASH, BiG-SCAPE and MIBiG', of the CIIMAR short course Bioinformatics for Natural Product Discovery 2025

This hands-on session features three main tools/resources:
- antiSMASH & MIBiG (online)
- BiG-SCAPE (offline, on your laptop or server)

In this repo you'll find the materials for the antiSMASH part of this hands-on session. We recommend you start with this section.
Once you're done, or approximately 1hr into the session, we'll switch over to the BiG-SCAPE, find the materials for that part [here](https://github.com/CatarinaCarolina/BiG-SCAPE-workshop).

## antiSMASH Documentation

The official documentation for antiSMASH can be found [here](https://docs.antismash.secondarymetabolites.org).

See a supporting document with a demo of the antiSMASH online webserver [here](https://github.com/CatarinaCarolina/Genome-Mining-CIIMAR-2025/blob/main/antiSMASH_demo.pdf). Use this file to guide your exploration of antiSMASH.

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

#### Questions:

- Extract the predicted sequence of the peptide from the antiSMASH results.
- Compare the predicted amino acid sequence with the [experimentally determined structure](https://doi.org/10.1016/s1074-5521(02)00252-1).
- Find other organisms, which might produce similar compounds.
- Find the genes in the CDA gene cluster, which code for enzymes involved in the biosynthesis of the non-proteinogenic amino acid hydroxyphenylglycine (hpg).

------------

### Exercise 2: Bacillus velezensis (amyloliquefaciens) FZB42 - (RefSeq accession: NC_009725.2)

1.	Find and download the Bacillus velezensis FZB42 genome from NCBI
2.	Run antiSMASH with the genome
3.	Analyze the data as discussed above.

#### Questions:
- How many BGCs does B. velezensis have?
- Which are PKS / NRPS / hybrid products
- Which compounds are known?
- Can you find these BGCs in [antiSMASH DB](https://antismash-db.secondarymetabolites.org/)? and in [MIBiG](https://mibig.secondarymetabolites.org/)?

------------

### Exercise 3: secondary metabolite gene clusters of Streptomyces leeuwenhoekii

1. Open the antiSMASH results for a recently sequenced streptomycete genome using [default](http://bioinformatics.nl/~medem005/LN831790/index.html) settings and ['loose' mode](http://bioinformatics.nl/~medem005/LN831790_loose/index.html).

#### Questions:
- Explore the results produced by the default run settings.
 - How many biosynthetic gene clusters (BGCs) did antiSMASH identify? Based on the results, which known compounds do you expect this strain to be able to produce? _Hint: take a look at the detailed knownclusterblast results for each cluster that has at least > 50% similarity on the gene level to a known cluster to assess this._

- Now take a look at the results produced by the 'loose' mode.
  - Focus on some of the ‘newly added’ BGCs, and specifically look at the smCOG annotations and the knownclusterblast results.
  - Can you identify some clusters that are very probable to encode the biosynthesis of an actual secondary metabolite?
  - And can you find some clusters for which this is very unlikely? Which further methods could you use to identify those putative BGCs that are likely to encode the biosynthesis of a biologically active molecule?

#### 3.1 Chaxamycin

The following molecule is known to be made by the sequenced [strain](https://www.ebi.ac.uk/chebi/searchId.do?chebiId=CHEBI:69812)

The molecule (called chaxamycin) is an ansamycin-type polyketide. Ansamycins are characterized by the presence of a macrocycle composed of a benzenic or naphthalenic chromophore, bridged by an aliphatic ansa chain that terminates at the chromophore in an amide linkage. The key precursor of the chromophore is 3-amino-5-hydroxybenzoic acid (AHBA), which is known to be synthesized by proteins encoded by a specific sub-cluster that is found in all ansamycin PKS gene clusters, such as those for the production of rifamycin, macbecin and naphthmycin.

- Based on the antiSMASH results, which of the gene clusters in the sequenced genome is most likely to produce the chaxamycins?
  - Which antiSMASH feature(s) did you use to conclude this?
- Look at the ClusterBlast results for the region you identified. Does this region entry represent one single gene cluster, or does it in fact represent two separate but adjacently located gene clusters that are part of a single region? Why do you think so?

#### 3.2 Peptidic Fragments

Based on a mass spectrometry experiment, two apparently new natural products are identified from the strain. Based on fragmentation analysis, both appear to be peptides. For each of the two metabolites, a six amino acid-long fragment is retrieved that is reconstructed based on mass shifts from tandem mass spectra.

Fragment from peptide 1: Ala-Val-Ala-Phe-Orn-Thr
Fragment from peptide 2: Leu-Tyr-Gly-Val-Arg-Asn

The total mass of the entire second peptide is approximately twice as large as that of the first peptide. _Hint: one of the two peptides is not produced by an NRPS assembly line._

- Based on the antiSMASH results (default mode), which gene clusters do you think are responsible for the biosynthesis of the two peptides? What strategy did you use to find this out?

#### 3.3 Predicting the chemistry of the product of an unknown BGC

Now have a look at the gene cluster in region 10  ([default mode](http://bioinformatics.nl/~medem005/LN831790/index.html)).

- To which known gene clusters is this cluster similar?
  - What are the known biological activities of the product of these clusters?
  - Look into the literature references at the bottom of the MIBiG entries, which can be reached by clicking the link on the accession number of the knownclusterblast hit.

- What are the differences between the known gene cluster and this one?
  - Based on the chemistry generated by the enzymes that differ, what do you predict about the potential structural differences between this molecule and the region 10 product? Do you consider this a promising target for potential further investigation?


_For your reference, please find a paper describing the entire genome sequence used above [here](http://www.biomedcentral.com/1471-2164/16/485). For results on experiments on the chaxamycin cluster, see [here](https://aem.asm.org/content/81/17/5820.full)._


### Now, we'll switch over to the BiG-SCAPE, find the materials for that part [here](https://github.com/CatarinaCarolina/BiG-SCAPE-workshop).






