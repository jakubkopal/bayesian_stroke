# Code supplement to the manuscript: Bayesian modeling disentangles language versus executive control disruption in stroke
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)
[![DOI](https://img.shields.io/badge/DOI-10.1101%2F862615-informational
)]([https://doi.org/10.1101/2023.04.17.537199](https://doi.org/10.1101/2023.04.17.537199))

This repository contains the code used to process and analyse the data presented in the "Bayesian modeling disentangles language versus executive control disruption in stroke" manuscript. In addition, the repository contains published figures.

## Abstract
<div style="margin-left: 40px;" align="justify">
Stroke is the leading cause of long-term disability worldwide. Incurred brain damage disrupts cognition, often with persisting deficits in language and executive capacities. Despite their clinical relevance, the commonalities, and differences of language versus executive control impairments remain under-specified. We tailored a Bayesian hierarchical modeling solution in a largest-of-its-kind cohort (1080 stroke patients) to deconvolve language and executive control in the brain substrates of stroke insults. Four cognitive factors distinguished left- and right-hemispheric contributions to ischemic tissue lesion. One factor delineated language and general cognitive performance and was mainly associated with damage to left-hemispheric brain regions in the frontal and temporal cortex. A factor for executive control summarized control and visual-constructional abilities. This factor was strongly related to right-hemispheric brain damage of posterior regions in the occipital cortex. The interplay of language and executive control was reflected in two factors: executive speech functions and verbal memory. Impairments on both were mainly linked to left-hemispheric lesions. These findings shed light onto the causal implications of hemispheric specialization for cognition; and make steps towards subgroup-specific treatment protocols after stroke.
</div>


<c>![Figure 5](https://github.com/jakubkopal/bayesian_stroke/blob/main/figures/Fig5.png)</c>


Figure 1

**Distinct associations of lesion atoms and cognitive factors disentangle language and executive deficits.**

<div align="justify">
Results for the four-factor solution. (a) Lesion-deficit associations for the different factors and lesion atoms. Factors 1, 2 and 4 show the most prominent brain lesion effects for atom 6 in the left hemisphere (including temporal regions), while factor 3 shows strong implications for atom 4 (summarizing occipital regions) in the right hemisphere. (b) Correlations between model-specific beta values dedicated to each factor. Left-dominant factors show more significant correlations with each other. (c) Distinct relationships between significant lesion atoms and cognitive impairments. The significance of lesion-related beta estimates was assessed based on the difference of 90% highest density intervals from zero. Left: lesion atom 1 is characterized by left-hemispheric contributions from factors 3 and 4 and right-hemispheric contributions from factor 4, with the overall strongest load of the left insular cortex. Middle: Overlap and distinct contributions of the four factors. Right: lesion atom 6 is characterized by left-hemispheric contributions from factor 2, with the strongest load of the middle temporal gyrus. (d) Correlations of factors with maps of the language network and multiple-demand network44,45 show a relatively stronger overlap of executive speech functions and language with the language network. Executive functions and verbal memory show relatively stronger associations with the multiple-demand network. (e) Hemispheric relevance depends on key covariates. The plot depicts the interrelation between the relevance of lesion load in each hemisphere (y-axis, left hemisphere: light colors, right hemisphere: dark colors) and marginal posterior parameters of two key covariates (x-axis) in predicting cognitive performance. Years of education had positive effects on all four factors. The strongest effect was on factor 2. Conversely, an increase on the IQCODE scale37, i.e. a higher pre-stroke cognitive decline, predicted a decrease in scores of factors 1, 2, and 4. Lesion atom-outcome associations uncovered factor-specific language and executive control deficits: a prominent contribution of the lesion atom covering left-hemispheric superior and middle temporal regions to language, executive speech functions and verbal memory and strong implications of right occipital brain regions for executive functions.
</div>



## Resources and Scripts
CNV-specific asymmetry patterns are saved in the `data` folder. All figures used in the articles are in the `figures` folder. Findings from the article are based on the analysis scripts in the `scripts` folder.

1.   `scripts/extract_asymmetry_pattern.py` is an example of using Linear discriminant to isolate CNV-specific asymmetry patterns from raw anatomical data. Bootstraping is implemented to increase robustness.
2.   `scripts/analyze_single_CNV.py` is an analysis script to examine the asymmetry patterns of each CNV separately.
3.   `scripts/analyze_multiple_CNV.m` uses multi-class LDA to highlight similarities and differences among asymmetry patterns of 8 selected CNVs.
4.   `scripts/planum_temporale_analysis.py` is an analysis script to investigate CNV effects on planum temporale.
5.   `scripts/neurosynth_analysis.py` interrogates the NeuroSynth database to functionally annotate derived asymmetry patterns.
6.   `scripts/genetics_asymmtry.py` plots the annotation of SNPs and genes associated with planum temporale asymmetry in GWAS Catalogue.
