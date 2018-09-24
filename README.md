# Comparative LD Score Regression

## Motivation

LD score regression is used in the human literature to identify genetic signatures from human GWAS studies that show marked similarities to one another [@zheng2017ld]. To my knowledge, nobody has used LD score regression in a cross-species way (though Elissa has commented that GeneWeaver does this). The advantage of this methodology would be that one could take a human phenotype such as cocaine use disorder and correlate it with a mouse phenotype such as cocaine IVSA. Neither phenotype would require significant genes to be found; instead, such an LD regression methodology would work on the whole genome structure of the statistical score.

The advantage of this technique is that it would allow for complex and multigenic strain mouse models for addiction to be validated. Such a technique would also allow for gene finding and regulatory variant finding to be performed in mouse, where resources are much better than they are in humans. If this works, it would be an innately translational method that could be readily applied to translational research.

## High-level description of proposed method

At a high level, this method would require the identification of syntenic portions of the human and mouse genomes. These syntenic portions would be used to map markers whose LD scores could then be imputed at virtual locations that translate between the two genomes. The human LD score would be derived from a GWAS while the mouse LD score would be derived from a QTL mapping study on, e.g., a human cocaine use disorder GWAS compared to cocaine IVSA in the Diversity Outbred animals. The LD score regression described earlier [@zheng2017ld] would be used on the datasets. A high LD score regression would indicate that the genetic structure of complex human and mouse genotypes are similar even across species. This would provide for construct validity in complex mouse experiments.

## Pipeline proposal (preliminary)

This preliminary pipeline proposal attempts to lay out the first steps of the pipeline to map virtual markers.

1) Identify human markers with LD summary scores
2) Map markers to mice using two-way reciprocol best BLAST hit (two-way RBH)
3) Impute mouse LD scores for virtual human markers
4) Run LDSR on the human-to-mouse data
5) Interpret results

The preliminary pipeline would need proofing out using simulated data. The initial work would be to build a suitable map of virtual markers to impute.

## Anticipated roadblocks

Finding and mapping of the cross-species markers is anticipated to be a significant problem. Various translocations have occured throughout evolutionary history, making it difficult to know *a priori* how these genomes will be powered for analysis.

## Test Case

Blood pressure QTL study: the human study was published in *Nature* in 2011 and was entitled "Genetic variants in novel pathways influence blood pressure and cardiovascular disease risk." The mouse version was published in *Hypertension* in 2009 and entitled "Genetic analysis of blood pressure in 8 mouse intercross populations."
