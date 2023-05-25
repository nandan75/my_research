_Performing genome-wide association analyses (GWAS)_ to identify etiological differences underlying subtypes of a disease involves several steps.   
Here are the possible steps involved in conducting such analyses:

**Define disease subtypes:** Clearly define the subtypes of the disease based on relevant clinical or molecular characteristics.   
- This could involve considering factors such as disease progression, response to treatment, or molecular signatures.
- Clinical expertise and domain knowledge are essential for defining disease subtypes based on relevant clinical or molecular characteristics.

**Sample collection:** Gather a well-characterized cohort of individuals representing each disease subtype.   
- Collect relevant clinical and molecular data for each individual, including phenotypic information, medical history, and genetic data.

**Genotyping or sequencing:** Obtain genetic data for each individual in the cohort. 
- This can be done through genotyping arrays or whole-genome sequencing, depending on the available resources and study objectives.
  - **Genotyping arrays**: PLINK, Illumina GenomeStudio, Affymetrix Power Tools (APT).
  - **Whole-genome sequencing**: GATK (Genome Analysis Toolkit), BWA (Burrows-Wheeler Aligner), SAMtools.

**Quality control and data cleaning**: Perform quality control checks on the genetic data to ensure accuracy and reliability. Remove low-quality samples and variants that do not meet the predefined quality criteria.
- PLINK, GATK, Hail, SNPTEST, KING.

**Imputation and variant annotation**: Impute missing genotypes using reference panels to maximize the coverage of genetic variants.   
- Annotate the genetic variants with functional information to identify potentially relevant variants.
- **Imputation**: IMPUTE2, Minimac3, Michigan Imputation Server.
- **Variant annotation**: ANNOVAR, VEP (Variant Effect Predictor), SnpEff.

**Association analysis**: Conduct association tests between genetic variants and disease subtypes.   
- This involves comparing the genotypes or allele frequencies of each variant between different subtypes using appropriate statistical methods. 
- [Adjust for potential confounders](./more_details_about_terms.md#Potential-confounders) such as population structure, age, and sex.
- PLINK, SNPTEST, EPACTS, GEMMA, BOLT-LMM.

**Multiple testing correction**: Account for the multiple comparisons conducted in the GWAS by applying statistical corrections (e.g., Bonferroni correction, false discovery rate) to control for false-positive findings.
- PLINK, QVALUE, FDRtools, Benjamini-Hochberg procedure.

**Functional interpretation**: Analyze the identified associated variants in terms of their functional implications.   
- This may involve investigating their biological roles, potential mechanisms of action, and relevance to the disease subtypes.
- Ingenuity Pathway Analysis (IPA), Gene Ontology (GO) enrichment analysis, Reactome, DAVID, Enrichr.

**Replication and validation**: Replicate the findings in independent cohorts or populations to validate the associations.   
- Replication helps to establish the robustness and generalizability of the identified genetic variants.
- PLINK, SNPTEST, EPACTS, BOLT-LMM (applied to independent cohorts or populations).

**Integration with other data types**: Integrate the GWAS results with 
- other omics data (e.g., transcriptomics, epigenomics, proteomics) and clinical data to gain a more comprehensive understanding of the molecular and biological processes underlying the disease subtypes.

**Biological interpretation**: Interpret the results in the context of existing knowledge about the disease and its subtypes.   
- Investigate the biological pathways, networks, or molecular processes that are enriched or disrupted in the identified genetic variants.
- Ingenuity Pathway Analysis (IPA), Gene Set Enrichment Analysis (GSEA), WebGestalt, Enrichr, STRING.

**Follow-up functional studies**: Perform functional studies, such as in vitro or in vivo experiments, to experimentally validate the functional consequences of the identified genetic variants and gain insights into their impact on disease subtypes.

- It's worth noting that the steps outlined above provide a general framework for performing GWAS analyses. 
- The specific details and tools used may vary depending on the resources available, the nature of the disease, and the research objectives.
  
    
    
<img alt="Screen Shot 2023-05-23 at 2 33 22 pm" src="https://github.com/nandan75/my_research/assets/12062345/6234873e-5018-4e42-8672-041fa7549723" style="width:80%; height:80%;">
  
a | **Selecting study populations**: Data can be collected from study cohorts etc.  
b | **Genotyping**: Genotypic data can be collected using microarrays to capture common variants, or NGS methods for WGS or whole-exome sequencing WES.   
**Data processing**. 
c | **Quality control** includes steps at the wet-laboratory stage, such as genotype calling and DNA switches, and dry-laboratory stages on called genotypes, such as deletion of bad SNPs and individuals, detection of population strata in the sample and calculation of principal components. Figure depicts clustering of individuals according to genetic substrata.   
d | **Genotypic data can be phased, and untyped genotypes imputed **  
       using information from matched reference populations from repositories such as 1000 Genomes Project or TopMed.   

e | **Testing for associations**: Genetic association tests are run for each genetic variant, using an appropriate model (for example, additive, non-additive, linear or logistic regression). Output is inspected for unusual patterns and summary statistics are generated.   

Accounting for false discovery. 
**Genome-wide association meta-analysis. **

f | Results from multiple smaller cohorts are combined using standardized statistical pipelines.   
g | Results can be replicated using internal replication or external replication in an independent cohort.  
h | In silico analysis of genome-wide association studies (GWAS), using information from external resources. This can include in silico fine-mapping, SNP to gene mapping, gene to function mapping, pathway analysis, genetic correlation analysis, Mendelian randomization and polygenic risk prediction. After GWAS, functional hypotheses can be tested using experimental techniques such as CRISPR or massively parallel reporter assays, or results can be validated in a human trait/disease model (not shown).  



