# DNA from Fecal Immunochemical Test can replace stool for microbiota-based colorectal cancer screening

**Authors:** Nielson T. Baxter^1^, Mack T. Ruffin IV^2^, Mary A.M. Rogers^3^, and Patrick D. Schloss^1\*^


**Affiliations:**  
^1^Department of Microbiology and Immunology, University of Michigan, Ann Arbor, Michigan.  
^2^Department of Family Medicine, University of Michigan, Ann Arbor, Michigan.  
^3^Department of Internal Medicine, University of Michigan, Ann Arbor, Michigan.  
^\*^Corresponding author: pschloss@umich.edu




###Abstract  
(≤ 250 words, unstructured)


###Introduction  
Although colorectal cancer (CRC) mortality has declined in recent decades, it remains the second leading cause of death among cancers in the United States [@siegel2014colorectal]. Early detection of CRC is critical since patients whose tumors are detected at an early stage have a greater than 90% chance of survival. However more than a third of individuals for whom screening is recommended, do not adhere to screening guidelines [@centers2013vital]. The high cost and invasive nature of structural exams, like colonoscopy and sigmoidoscopy, are barriers for many people [@hsia2000importance;@jones2010barriers]. Unfortunately less expensive, non-invasive tests, such as the guaiac fecal occult blood test (gFOBT) and fecal immunochemical test (FIT), fail to reliably detect adenomas [@hundt2009comparative]. Thus, there is a need for novel non-invasive screening methods with improved sensitivity for early stage colonic lesions.

Several studies have demonstrated the potential for the gut microbiota to be used to detect CRC [@zeller2014potential;@yu2015metagenomic]. Moreover, we have shown that combining microbiota-analysis with conventional diagnostics, like gFOBT and FIT, can significantly improve the detection of colonic lesions over either method by itself [@zackular2014human;@baxter2016microbiota]. One limitation of microbiota-based CRC screening is the need to collect and process separate stool samples for microbiota characterization. Given the widespread use of FIT to collect specimens for screening, using the same sample for microbiota characterization could make processing more efficient and less expensive.  We hypothesized that the small amount of fecal material contained in FIT sampling cartridges was sufficient to perform both hemoglobin quantification and microbiota characterization.  To test this hypothesis, we isolated bacterial DNA from the residual buffer of FIT cartridges that had already been used for quantifying hemoglobin concentrations from stool. We then compared the bacterial composition of the FIT cartridge to that of DNA isolated directly from a patient's stool sample and assessed the ability of FIT cartidge-derived DNA to be used for microbiota-based CRC screening.


###Materials and Methods
**Study Design / Diagnoses / Stool Collection.** Stool samples were obtained through the Great Lakes-New England Early Detection Research Network. Patients were asymptomatic, at least 18 years old, willing to sign informed consent, able to tolerate removal of 58 mL of blood, and willing to collect a stool sample. Patient age at the time of enrollment ranged from 29 to 89 with a median of 60. Patients were were excluded if they had undergone surgery, radiation, or chemotherapy for current CRC prior to baseline samples or had inflammatory bowel disease, known hereditary non-polyposis CRC, or familial adenomatous polyposis. Patient diagnoses were determined by colonoscopic examination and histopathological review of any biopsies taken. Colonoscopies were performed and fecal samples were collected in four locations: Toronto (Ontario, Canada), Boston (Massachusetts, USA), Houston (Texas, USA), and Ann Arbor (Michigan, USA). Stool samples were packed in ice, shipped to a processing center via next day delivery and stored at -80˚C. Fecal material for FIT was collected from frozen stool aliquots using OC FIT-CHEK sampling bottles (Polymedco Inc.), processed using an OC-Auto Micro 80 automated system (Polymedco Inc.), and stored at -20C. The University of Michigan Institutional Review Board approved this study, and all subjects provided informed consent.

**16S rRNA gene sequencing.** Stool samples were obtained through the Great Lakes-New England Early Detection Research Network. Patients were asymptomatic, at least 18 years old, willing to sign informed consent, able to tolerate removal of 58 mL of blood, and willing to collect a stool sample. Patient age at the time of enrollment ranged from 29 to 89 with a median of 60. Patients were were excluded if they had undergone surgery, radiation, or chemotherapy for current CRC prior to baseline samples or had inflammatory bowel disease, known hereditary non-polyposis CRC, or familial adenomatous polyposis. Patient diagnoses were determined by colonoscopic examination and histopathological review of any biopsies taken. Colonoscopies were performed and fecal samples were collected in four locations: Toronto (Ontario, Canada), Boston (Massachusetts, USA), Houston (Texas, USA), and Ann Arbor (Michigan, USA). Stool samples were packed in ice, shipped to a processing center via next day delivery and stored at -80˚C. Fecal material for FIT was collected from frozen stool aliquots using OC FIT-CHEK sampling bottles (Polymedco Inc.), processed using an OC-Auto Micro 80 automated system (Polymedco Inc.), and stored at -20C. The University of Michigan Institutional Review Board approved this study, and all subjects provided informed consent.

**Statistical Methods.** All statistical analyses were performed using R (v.3.2.0). Random forest models were generated using the AUC-RF algorithm for feature reduction and maximizing model performance [@calle2011auc]. The most predictive OTUs were determined based on mean decrease in accuracy when removed from the model. The area under the curve (AUC) of receiver operator characteristic (ROC) curves were compared using the method described by DeLong et al. [@delong1988comparing]. The optimal cutoff for each model was determined using Youden's _J_ statistic as implemented in the pROC package in R [@youden1950index].


###Results
  


We tested whether the bacterial community profiles from FIT cartridges recapitulated their stool counterparts. First, we compared the number of OTUs shared between FIT/stool pairs from the same patient to the number of OTUs shared between patients. FIT cartridges and stool from the same patient had significantly more bacterial populations in common than those take from different patients (Fig. 1A, p<0.001), indicating that community membership was conserved between stool and FIT cartridges. Second, we calculated the similarity in community structure between samples using 1-thetaYC index [@reference]. This metric compares the presence or absence of bacterial populations along with their relative abundance. The bacterial community structure of stool and FIT samples from the same patient were significantly more similar to each other than to stool or FIT from other patients (Fig. 1B, p<0.001, two-sample Kolmogorov-Smirnov Test). Finally, we observed that the inter-personal variation in community structure between the stool samples of patients was conserved in samples from FIT cartridges (Mantel R=0.52, p<0.001). These findings suggest that that the overall composition of the microbiota in FIT cartridges matches that of stool.










Next, we compared the abundance of each genus in the FIT cartridges and stool (Fig. 2A). There was a strong correlation between the average abundance of each genus in stool and FIT cartridges (Spearman rho: 0.699, p<0.001), suggesting the abundance of bacterial genera was conserved. This correlation was especially strong for the 100 most abundant genera (Spearman rho: 0.886, p<0.001). Several bacterial species have been repeatedly associated with CRC, including _Fusobacterium nucleatum_, _Porphyromonas asaccharolytica_, _Peptostreptococcus stomatis_, and _Parvimonas micra_ [@warren2013co;@zeller2014potential;@yu2015metagenomic;@baxter2016microbiota].  As expected, the abundance of OTUs associated with these species in stool was significantly correlated with their abundance in matched FIT cartridges (all p<0.001)(Fig. 2B). We observed some biases in the abudance of certain taxa. In particular, the genus Pantoea was detected in 399 out of 404 FIT cartridges with an average abundance of 2.4%, but was only detected in 34 stool samples. The genus Helicobacter was detected in 172 FIT cartrdges, but only 10 stool samples. Likewise several genera of Actinobacteria were more abundant in stool samples compared to FIT. Notwithstanding these few exceptions, the abundance of the vast majority of genera were well conserved between stool and FIT cartridges.





We tested whether the bacterial relative abundances we observed in from FIT cartridges could be used to differentiate healthy patients from those with carcinomas using random forest models, as has been demonstrated with stool [@reference]. Using DNA from the FIT cartridge, the optimal model utilized 32 OTUs and had an AUC of 0.853. There was no significant difference in the AUC for this model and the model based on DNA isolated directly from stool, which used 28 OTUs and had an AUC of 0.831 (p=0.41). This demonstrated that models based on bacterial DNA from FIT cartridges could be as predictive as DNA isolated directly from stool.

When screening for CRC it is important to detect adenomas in addition to carcinomas. Unfortunately the gut microbiota, like FIT, cannot reliably detect adenomas on its own. However, we have shown that combining bacterial abundances and hemoglobin concentration into a single model significantly imporoves detection of lesions, especially adenomas, over either method by itself. Therefore we generated random forest models that combined hemoglobin concentration as determined by FIT with bacterial abundance from either stool or FIT catrdiges. As with the cancer versus normal comparison above, there was no difference in AUC the model based on bacteria from stool and the model based on bacteria from FIT cartridge. Again, this shows that bacterial DNA isolated from FIT cartridges can be used in place of stool for detecting colonic lesions based on the microbiota.


###Discussion
In this study we demonstrated that bacterial DNA isolated from FIT cartridges recapitulates the community structure and membership of patients' stool microbiota. FIT/stool pairs were significantly more similar within an individual than between individuals, and the interindividual differences in stool microbiota structure were conserved in FIT cartridge-derived microbiota.  Furthermore, FIT cartridge-derived and stool-derived bacterial DNA were equally predictive for differentiating healthy individuals from those with CRC. Finally, hemoglobin concentrations determined by FIT could be combined with microbiota from FIT cartridges to improve the sensitivity for detecting cancer.

The lower biomass of FIT cartridge buffer compared to stool does increase the risk of results being influenced by contaminants. For example, an OTU associated with Pantoea was found in all FIT cartridge samples and only ## stool samples. This may have been due to reagent contamination that was at a low enough concentration  to be undetectable in DNA from stool samples, but high enough to become apparent in the lower biomass FIT cartridges. Alternatively storage conditions could have played a role in biasing certain genera. FIT cartridges spent more time at or near room temperature so that they could be analyzed for hemoglobin concentration. Therefore its possible that certain species were able to grow, shifting their abundance relative to stool. Any biases were limitted to a small number of genera and had no apprent impact on the ability to detect CRC from FIT cartridged-derived DNA.

These findings demonstrate the potential for using DNA from FIT cartridges for microbiota-based screening. This could eliminate the need to collect and process separate stool samples, reducing the cost of screening. Furthermore, annual FIT cartridges could be used to moniter changes to a patients microbiota over time, making it possible to detect any shifts toward a disease-associated microbiome. It would also be possible to use FIT cartridges, rather than separate stool samples, for future studies on the role of the gut microbiota and CRC. Since FIT cartridges are already collected for CRC screening, it may be easier to recruit patients for large-scale validations of microbiota-based screening methods.

  
###Figures  

![](results/figure1.png)

**Figure 1. Bacterial community structure from FIT cartridge recapitulates stool.** Density plots showing distribution of the number of shared OTUs (A) and community similarity (B) between groups of samples (* p<0.001 two-sample Kolmogorov-Smirnov Test).

![](results/figure2A.png)
![](results/figure2B.png)
**Figure 2. Bacterial populations conserved between stool and FIT cartridge.**  (A) Scatterplot of the average relative abundance of each bacterial genus in stool and FIT cartridges. (B) Scatterplots of relative abundances of 4 OTUs frequently associated with CRC.

![](results/figure3.png)
**Figure 3. Microbiota-based models from FIT cartridge DNA are as predictive as models from stool.** (A) ROC curves for distinguishing healthy patients from those with cancer using using microbiota-based random forest models from FIT cartridge DNA or stool. (B) Probability of having cancer for each patient according to microbiota-based models from stool or FIT cartridges. (C) ROC curves for distinguishing patients with adenomas or carcinomas from healthy patients using both hemoglobin concentration and microbiota from either stool or FIT cartrdges. (D) Probability of having a lesion for each patient based on the models from C.


###References (≤25 references)
