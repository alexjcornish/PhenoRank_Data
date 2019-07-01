PhenoRank data
=====================


Data sets
----------

##### `disease_classes.tsv`
Associations between diseases, represented by OMIM IDs (**OMIM**), and DO terms (**DO**) where available, and their disease class (**CLASS**). Included is both the DO term used to define the class (**CLASS**) and the name of the class (**CLASS_NAME**).

If an OMIM ID could not be mapped to a DO term, then it is not possible to assign a disease class, and this cell is therefore marked NA. 


##### `disease_phenotype.tsv`
Associations between diseases (represented by OMIM IDs, **Disease_ID**) and characteristic phenotypes (represented by HPO and MP terms. **Phenotype_ID**).

Mappings between disease terms and phenotype terms from HPO and Hoehndorf *et al*. are used in PhenoRank to measure the phenotypic similarity of the query disease and diseases in OMIM. Hoehndorf *et al*. mapped phenotype terms (from HPO and MP) to disease terms (from DO) through automated text mining. Hoehndorf *et al*. determined that the 21 phenotype terms most strongly associated with each disease were most informative when quantifying phenotypic similarity and we therefore include these phenotype term mappings in PhenoRank. The cross-referencing provided by the DO was used to transfer the mapped phenotype terms to the corresponding OMIM diseases. 


##### `gene_disease.tsv`
Associations between genes (**Ensembl_Gene_ID**) and diseases (represented by OMIM IDs, **Disease_ID**), and whether each association was included in the test data set used to benchmark PhenoRank. 

Data downloaded from ClinVar (on 22 October 2016), OMIM (on 1 November 2016) and UniProtKB (on 22 October 2016) were used to define the disease-gene associations used in PhenoRank. ClinVar variants not marked as pathogenic or likely pathogenic, or whose review status was less than two stars were excluded. Non-disease variants from UniProtKB were excluded. Disease-gene associations from OMIM were not considered if the molecular basis of the disease is unknown. Diseases reported using vocabularies other than OMIM were mapped to OMIM terms using the cross-referencing provided by the Disease Ontology (DO). A disease is defined as being associated with a gene if a gene variant is reported as being disease causing.


##### `gene_mousemutant.tsv`
Associations between human genes (**Ensembl_Gene_ID**) and mouse mutants (represented by MGD IDs, **MGI_ID**).

Genotypes and phenotype term annotations for 24,834 mouse mutants and human-mouse gene orthology data were downloaded from the Mouse Genomics Database (on 13 October 2016). Human orthologs of the mutated gene in 21,143 mouse mutants were identified using the orthology data.


##### `mousemutant_phenotype.tsv`
Associations between mouse mutants (represented by MGD IDs, **MGI_ID**) and phenotypes observed in these mutants (represented by MP terms. **Phenotype_ID**).


##### `omim_do.tsv`
Mappings between OMIM IDs (**OMIM_ID**) and DO terms (**DO_ID**).

Mappings were generated using the cross-referencing provided by the DO. 


##### `ppi.tsv`
PPIs used in PhenoRank. 

PPI data were downloaded from four databases: BioGRID (version 3.4.131), HI-II-14 (on 27 November 2015), HPRD (on 30 March 2015) and IntAct (on 4 January 2016). Only direct interactions, associations and physical associations were obtained from BioGRID and IntAct. Duplicate interactions, looping interactions and interactions that did not occur between two H. sapiens proteins were excluded. Some PPI resources do not record interactions between different protein isoforms and we therefore considered all interactions at the gene level. 



PhenoRank reference
----------
[Cornish, A.J., David, A. and Sternberg M.J.E. PhenoRank: reducing study bias in gene prioritisation through simulation. Bioinformatics (2018).][1] 



References for sources of data used in PhenoRank
----------
- Amberger, J. S. et al. (2015) OMIM.org: Online Mendelian Inheritance in Man (OMIM), an online catalog of human genes and genetic disorders. Nucleic Acids Res., 43, 789–798.
- Bult, C. J. et al. (2016) Mouse genome database 2016. Nucleic Acids Res., 44, D840–D847.
- Chatr-Aryamontri, A. et al. (2015) The BioGRID interaction database: 2015 update. Nucleic Acids Res., 43, D470–D478.
- Das, J. and Yu, H. (2012) HINT: High-quality protein interactomes and their applications in understanding human disease. BMC Syst. Biol., 6(1), 92.
- Hoehndorf, R. et al. (2015) Analysis of the human diseasome reveals phenotype modules across common, genetic, and infectious diseases. Sci. Rep., 5, 10888.
- Keshava Prasad, T. S. et al. (2009) Human Protein Reference Database-2009 update. Nucleic Acids Res., 37, D767–D772.
- Kibbe, W. A. et al. (2015) Disease Ontology 2015 update: an expanded and updated database of human diseases for linking biomedical knowledge through disease data. Nucleic Acids Res., 43, D1071–D1078.
- Köhler, S. et al. (2014) The Human Phenotype Ontology project: Linking molecular biology and disease through phenotype data. Nucleic Acids Res., 42, D966–D974.
- Landrum, M. J. et al. (2016) ClinVar: public archive of interpretations of clinically relevant variants. Nucleic Acids Res., 44, D862–D868.
- Orchard, S. et al. (2014) The MIntAct project--IntAct as a common curation platform for 11 molecular interaction databases. Nucleic Acids Res., 42, D358–D363.
- Rolland, T. et al. (2014) A Proteome-Scale Map of the Human Interactome Network. Cell, 159, 1212–1226.
- Smith, C. L., Goldsmith, C.-A. W. and Eppig, J. T. (2005) The Mammalian Phenotype Ontology as a tool for annotating, analyzing and comparing phenotypic information. Genome Biol., 6, R7.
- The UniProt Consortium (2014) Activities at the Universal Protein Resource (UniProt). Nucleic Acids Res., 42, D191–D198.

[1]: https://doi.org/10.1093/bioinformatics/bty028
