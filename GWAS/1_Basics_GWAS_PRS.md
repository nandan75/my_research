**Genetics basics when understanding -GWAS**
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6001694/ 

The aim of genome‐wide association studies (GWAS) is to identify single nucleotide polymorphisms of which the allele frequencies vary systematically as a function of phenotypic trait values .
- **Single nucleotide polymorphism (SNP)**: This is a variation in a single nucleotide (i.e., A, C, G, or T) that occurs at a specific position in the genome. A SNP usually exists as two different forms (e.g., A vs. T). These different forms are called alleles. A SNP with two alleles has three different genotypes (e.g., AA, AT, and TT).	
- **Linkage disequilibrium (LD)**: This is a measure of non‐random association between alleles at different loci at the same chromosome in a given population. SNPs are in LD when the frequency of association of their alleles is higher than expected under random assortment. LD concerns patterns of correlations between SNPs.
- **Clumping**: This is a procedure in which only the most significant SNP (i.e., lowest p value) in each LD block is identified and selected for further analyses. This reduces the correlation between the remaining SNPs, while retaining SNPs with the strongest statistical evidence.
- **Heterozygosity**: This is the carrying of two different alleles of a specific SNP. The heterozygosity rate of an individual is the proportion of heterozygous genotypes. High levels of heterozygosity within an individual might be an indication of low sample quality whereas low levels of heterozygosity may be due to inbreeding.	
- **Minor allele frequency (MAF)**: This is the frequency of the least often occurring allele at a specific location. Most studies are underpowered to detect associations with SNPs with a low MAF and therefore exclude these SNPs.
- **The Hardy–Weinberg (dis)equilibrium (HWE) law**: This concerns the relation between the allele and genotype frequencies. 
  - It assumes an indefinitely large population, with no selection, mutation, or migration. 
  - The law states that the genotype and the allele frequencies are constant over generations. 
  - Violation of the HWE law indicates that genotype frequencies are significantly different from expectations (e.g., if the frequency of allele A = 0.20 and the frequency of allele T = 0.80; the expected frequency of genotype AT is 2*0.2*0.8 = 0.32) and the observed frequency should not be significantly different. In GWAS, it is generally assumed that deviations from HWE are the result of genotyping errors. The HWE thresholds in cases are often less stringent than those in controls, as the violation of the HWE law in cases can be indicative of true genetic association with disease risk.	
- **Population stratification**: This is the presence of multiple subpopulations (e.g., individuals with different ethnic background) in a study. Because allele frequencies can differ between subpopulations, population stratification can lead to false positive associations and/or mask true associations. 
  - An excellent example of this is the chopstick gene, where a SNP, due to population stratification, accounted for nearly half of the variance in the capacity to eat with chopsticks (Hamer & Sirota, 2000).
- **Pruning**: This is a method to select a subset of markers that are in approximate linkage equilibrium. In PLINK, this method uses the strength of LD between SNPs within a specific window (region) of the chromosome and selects only SNPs that are approximately uncorrelated, based on a user‐specified threshold of LD. In contrast to clumping, pruning does not take the p value of a SNP into account.

For rest of the important definitions see - https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6001694/#mpr1608-blk-0001 


**GWAS (Genome-Wide Association Study)** 
- It is a method used in genetics and genomics research to identify associations between genetic variations and traits or diseases. 
  - So the aim of genome‐wide association studies (GWAS) is to identify single nucleotide polymorphisms of which the allele frequencies vary systematically as a function of phenotypic trait values.   
- In a GWAS, researchers examine a large number of genetic markers, such as single nucleotide polymorphisms (SNPs), across the entire genome of individuals from a population. 
- By comparing the presence or absence of specific genetic variations in individuals with a particular trait or disease to those without the trait or disease, researchers can identify potential genetic associations.
- GWAS studies have been instrumental in discovering genetic variants that are associated with various complex traits and diseases, including common conditions like diabetes, heart disease, and certain types of cancer. The findings from GWAS can provide insights into the underlying genetic basis of these traits and diseases, as well as potential targets for further research and therapeutic interventions.
  - Can involve **targeted genotyping of specific and pre-selected variants** using microarrays, whereas 
  - Whole-exome sequencing (WES) and whole-genome sequencing (WGS) studies aim to **capture all genetic variation**. 


Genome‐wide association studies (GWAS) have become increasingly popular to identify associations between single nucleotide polymorphisms (SNPs) and phenotypic traits. 


**PRS (Polygenic Risk Score)**

- It is a numerical score calculated using data from GWAS studies to estimate an individual's genetic predisposition to a particular trait or disease. 
- The PRS is based on the cumulative effects of multiple genetic variants identified in GWAS, each of which may have a small effect on the trait or disease.
- To calculate a PRS, researchers assign a weight to each genetic variant based on its strength of association with the trait or disease in the GWAS. These weights are then multiplied by the number of risk alleles (i.e., the specific genetic variant associated with the trait or disease) an individual carries at each relevant locus. The weighted scores are summed to generate an overall PRS for an individual, indicating their genetic risk profile for the trait or disease of interest.
PRS can be used in various applications, including 
  - Predicting an individual's susceptibility to developing certain diseases, such as diabetes or coronary heart disease. 
  - It can also be used to stratify individuals in research studies, assess disease risk in population-level studies, or identify high-risk individuals who may benefit from early interventions or targeted screening.   
  - However, it's important to note that PRS is a probabilistic estimation and does not provide definitive predictions or diagnoses on an individual level.
