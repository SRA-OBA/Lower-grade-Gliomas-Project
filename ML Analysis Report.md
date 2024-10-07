**MACHINE LEARNING ANALYSIS OF GLIOMA**

**INTRODUCTION**

<a id="_h44jo1ikpc3d"></a>Diffuse gliomas make up about 80% of malignant brain tumors. Mesfin and Al-Dhahir (2021) classify them into oligodendroglioma, oligoastrocytoma, astrocytoma, and glioblastoma, covering WHO grades II to IV. Mutations in the isocitrate dehydrogenase IDH1 and IDH2 genes are central to glioma biology, found mainly in lower-grade gliomas, and linked to the G-CIMP (glioma-CpG island methylator phenotype). IDH mutants are linked to better prognoses, while wild types are more aggressive (Garrett _et al._, 2021). DNA methylation profiling is crucial for understanding glioma subtypes, with IDH mutants typically showing higher methylation than wild types.

 

**METHODOLOGY**

**Preprocessing of Dataset for Machine Learning Analysis**

The gliomas dataset (n=516) from TCGA was cleaned and normalized to align gene expression data with metadata based on IDH status (mutant or wild type). The top 1000 most variable genes were selected based on standard deviation, and near-zero variance features were removed to reduce noise. Data was centered for standardization, and highly correlated features (correlation > 0.5) were removed to mitigate multicollinearity.   

**KNN Methodology**

 

The k-Nearest Neighbors (kNN) model was applied using an 80% training and 20% testing dataset split to classify gliomas based on molecular profiles. The 'k' value was optimized through cross-validation for maximum accuracy. Euclidean distance was used to measure similarity between data points. Performance was assessed using accuracy, precision, and confusion matrices to visualize results.

 

**RESULT AND MODEL PERFORMANCE**

 

The kNN model achieved approximately 95% accuracy, demonstrating strong classification performance for gliomas. Precision and recall scores varied by subtype but generally distinguished well between IDH mutant and wild-type gliomas. The box plot below shows feature importance, highlighting IDH status and TCGA-P5-A5F6-01A-11R-A28M-07, with the latter being slightly more influential.

<!--[if gte vml 1]><v:shapetype
 id="_x0000_t75" coordsize="21600,21600" o:spt="75" o:preferrelative="t"
 path="m@4@5l@4@11@9@11@9@5xe" filled="f" stroked="f">
 <v:stroke joinstyle="miter"/>
 <v:formulas>
  <v:f eqn="if lineDrawn pixelLineWidth 0"/>
  <v:f eqn="sum @0 1 0"/>
  <v:f eqn="sum 0 0 @1"/>
  <v:f eqn="prod @2 1 2"/>
  <v:f eqn="prod @3 21600 pixelWidth"/>
  <v:f eqn="prod @3 21600 pixelHeight"/>
  <v:f eqn="sum @0 0 1"/>
  <v:f eqn="prod @6 1 2"/>
  <v:f eqn="prod @7 21600 pixelWidth"/>
  <v:f eqn="sum @8 21600 0"/>
  <v:f eqn="prod @7 21600 pixelHeight"/>
  <v:f eqn="sum @10 21600 0"/>
 </v:formulas>
 <v:path o:extrusionok="f" gradientshapeok="t" o:connecttype="rect"/>
 <o:lock v:ext="edit" aspectratio="t"/>
</v:shapetype><v:shape id="Picture_x0020_2" o:spid="_x0000_i1025" type="#_x0000_t75"
 style='width:240pt;height:220.8pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="file:///C:/Users/SALAAM~1/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png"
  o:title="KNN_Rplot"/>
</v:shape><![endif]--><!--[if !vml]-->![](file:///C:/Users/SALAAM~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)<!--[endif]-->

 

**Figure 1: Box plot illustrating the feature importance for a k-nearest neighbors (KNN) model.**

** **

**Comparison of Findings Reported in the Target Paper**

** **

Ceccarelli et al. (2016) identified distinct diffuse glioma subtypes through genetic alterations, with DNA methylation profiling revealing clinically significant subsets, including an IDH mutant subtype linked to poor outcomes due to DNA demethylation. These findings support exploring additional clusters in the glioma dataset with updated methods and data, potentially uncovering new subtypes or refining existing classifications.

 

**CONCLUSION AND FUTURE DIRECTIONS**

 

In conclusion, while Ceccarelli et al.'s findings greatly enhance our understanding of diffuse glioma biology and classification, the evolving field of genomic research suggests that additional clustering using newer datasets could provide further insights.

 

 

 

 

 

**REFERENCES**

HACKBIO. Machine Learning in Genomics Course. 2024. <https://thehackbio.com/courses/60>

Ceccarelli, M., Barthel, Floris P., Malta, Tathiane M., Sabedot, Thais S., Salama, Sofie R., Murray, Bradley A., Morozova, O., Newton, Y., Radenbaugh, A., Pagnotta, Stefano M., Anjum, S., Wang, J., Manyam, G., Zoppoli, P., Ling, S., Rao, Arjun A., Grifford, M., Cherniack, Andrew D., Zhang, H., & Poisson, L. (2016). Molecular Profiling Reveals Biologically Discrete Subsets and Pathways of Progression in Diffuse Glioma. _Cell_, _164_(3), 550–563. https\://doi.org/10.1016/j.cell.2015.12.028

Garrett, M., Fujii, Y., Osaka, N., Ito, D., Hirota, Y., & Sasaki, A. (2021). Emerging Roles of Wild-type and Mutant IDH1 in Growth, Metabolism and Therapeutics of Glioma. _Exon Publications_, 61–78. https\://doi.org/10.36255/exonpublications.gliomas.2021.chapter4

Mesfin, F. B., & Al-Dhahir, M. A. (2021, February 14). _Cancer, Brain Gliomas_. Nih.gov; StatPearls Publishing. https\://www\.ncbi.nlm.nih.gov/books/NBK441874/

 

 
