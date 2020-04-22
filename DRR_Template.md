---
params:
  projectDir: "N:/IMD_HTML_DRR_Template"
  reportNumber: "REPORT NUMBER"                           # Optional. Only include this if publishing in the semi-official Data Release Report Series. Contact Joe if you are.
  reportRefID: 123456                                     # This should match the Data Store Reference ID for this report.
  packageAbstract: >-
    Abstract Should go here.
    Multiple Lines are okay; it'll format correctly.
    Do not put the abstract in the text section below; this will allow
    For reuse of the abtract in all associated products.
    </br> </br> 
    The Abstract should succinctly describe the study, the assay(s) performed, 
    the resulting data, and their reuse potential, but should not make any 
    claims regarding new scientific findings. No references are allowed in this section. 
  dataPackage1RefID: 2272463                              # Data Store reference ID for data set associated with this report. You must have at least one.
  dataPackage1Title: "Dataset 1 FULL TITLE"               # Should match title in data store.
  dataPackage1Description: "SHORT TITLE FOR DATASET 1"  
  dataPackage2RefID: 2272464                              # Data Store reference ID for data set associated with this report. You must have at least one.
  dataPackage2Title: "Dataset 2 FULL TITLE"               # Should match title in data store.
  dataPackage2Description: "SHORT TITLE FOR DATASET 1"  
      
title: "REPORT TITLE"
subtitle: |
  | Data Release Report REPORT NUMBER 
author:
  - name: "Author 1"                                      # Add or remove authors as appropriate.
    affiliation: |
      | NPS Inventory & Monitoring Division 
      | 1201 Oakridge, Suite 150
      | Fort Collins, Colorado
  - name: "Author 2"
    affiliation: |
      | Managed Business Solutions (MBS), a Sealaska Company  
      | Contractor to National Park Service  
      | Natural Resource Stewardship and Science
date: "10 April, 2020"
abstract: "Abstract Should go here. Multiple Lines are okay; it'll format correctly. Do not put the abstract in the text section below; this will allow For reuse of the abtract in all associated products. </br> </br>  The Abstract should succinctly describe the study, the assay(s) performed,  the resulting data, and their reuse potential, but should not make any  claims regarding new scientific findings. No references are allowed in this section. "
editor_options:
  chunk_output_type: inline
csl: https://raw.githubusercontent.com/citation-style-language/styles/master/apa.csl
link-citations: yes
output:
  html_document:
    df_print: kable
    fig_caption: yes
    dev: svg
    highlight: haddock
    keep_md: yes
    smart: no
    theme: journal
    css: "common/journalnps.min.css"
    toc: yes
    toc_float: true
    number_sections: true
    includes:
        before_body:
          - "common/header.html"
        after_body: 
          - "common/footer.html"
  word_document:
    df_print: kable
    fig_caption: yes
    fig_height: 5
    fig_width: 5
    highlight: haddock
    reference_docx: "common/NRDS_Author_Template_V3.2.docx"
---





<hr>
# Background & Introduction
The Background & Summary should provide an overview of the study design, the assay(s) performed, and the data generated, including any background information needed to put this study in the context of previous work and the literature, and should reference literature as needed. The section should also briefly outline the broader goals that motivated collection of the data, as well as their potential reuse value. We also encourage authors to include a figure that provides a schematic overview of the study and assay(s) design. 

# Methods
The Methods should include detailed text describing any steps or procedures used in producing the data, including full descriptions of the experimental design, data acquisition assays, and any computational processing (e.g. normalization, image feature extraction). See the detailed section in our submission guidelines for advice on writing a transparent and reproducible methods section. Related methods should be grouped under corresponding subheadings where possible, and methods should be described in enough detail to allow other researchers to interpret and repeat, if required, the full study. Specific data outputs should be explicitly referenced via data citation (see Data Records and Citing Data, below).

Authors should cite previous descriptions of the methods under use, but ideally the method descriptions should be complete enough for others to understand and reproduce the methods and processing steps without referring to associated publications. There is no limit to the length of the Methods section.

Authors are encouraged to consider creating a figure that outlines the experimental workflow(s) used to generate and analyse the data output(s) (Figure 1).

<center>
![**Figure 1.** Example general workflow to include in the methods section.](figures/ProcessingWorkflow.png)
</center>

## Data Collection and Sample Processing Methods (optional)
Include a description of field methods and sample processing 

## Additional Data Sources (optional)
Provide descriptions (with citations) of other data sources used.

## Data Processing (required if done)
Summarize process and results of any QC processes done that manipulate, change, or qualify data.

## Code Availability (required)
For all studies using custom code in the generation or processing of datasets, a statement must be included in the Methods section, under the subheading "Code availability", indicating whether and how the code can be accessed, including any restrictions to access. This section should also include information on the versions of any software used, if relevant, and any specific variables or parameters used to generate, test, or process the current dataset. Actual analytical code should be provided in Appendices.

# Data Records (required)
The Data Records section should be used to explain each data record associated
with this work, including the repository where this information is stored, and
to provide an overview of the data files and their formats. Each external data
record should be cited as described below. A data citation should also be placed
in the subsection of the Methods containing the data-collection or analytical
procedure(s) used to derive the corresponding record.

Tables should be used to support the data records, and should clearly indicate
the samples and subjects (study inputs), their provenance, and the experimental
manipulations performed on each (please see example Tables below). They should
also specify the data output resulting from each data-collection or analytical
step, should these form part of the archived record.

## Required Elements for this Section

### Summary of datasets created. Example of stock text to include. ###

Two datasets were generated as a part of this effort (Table 2):

* **Dataset 1 FULL TITLE.** Comma-separated text file enumerating the specific taxa considered to have federal conservation status in NPS park units. These data were compiled by the National Park Service Biological Resources Division and were last updated on XX. Available at https://irma.nps.gov/DataStore/Reference/Profile/2272463. 

* **Dataset 2 FULL TITLE.** Comma-seperated text file enumerating the park-specific specific taxa about which data must be protected from release to the public based on federal conservation status. This dataset includes all taxa identified by the USFWS as well as their child taxa and taxonomic synonyms. Available at https://irma.nps.gov/DataStore/Reference/Profile/2272464. 


*Also include a table explaining provenance of datasets*

See Appendix for additional notes and examples.

# Data Quality Evaluation (required)
The Data Quality Evaluation section should present any analyses that are needed
to support the technical quality of the dataset. This section may be supported
by figures and tables, as needed. *This is a required section*; authors must
provide information to justify the reliability of their data. Wherever possible
& appropriate, data quality evaluation should be presented in the context of
data standards and quality control procedures as prescribed in the project’s
quality assurance planning documentation.

**Required elements for this section**

*Stock Text to include:*

The data within the data records listed above have been reviewed by staff in the NPS Inventory and Monitoring Division to ensure accuracy, completeness, and consistency with documented data quality standards, as well as for usability and reproducibility. The *Dataset 2 FULL TITLE* is suitable for its intendend use as of the date of processing (2020-04-10).

*Required Table*

Summary of any data qualification codes used, their definitions, and the fields to which they apply.


Possible content **strongly Suggested to Include**

-   Occurrence rates or patterns in data that do not meet established standards
    or data quality objectives.

Possible content **may include:**

-   experiments that support or validate the data-collection procedure(s) (e.g.
    negative controls, or an analysis of standards to confirm measurement
    linearity)

-   statistical analyses of experimental error and variation

-   general discussions of any procedures used to ensure reliable and unbiased
    data production, such as chain of custody procedures, blinding and
    randomization, sample tracking systems, etc.

-   any other information needed for assessment of technical rigor by
    reviewers/users

Generally, this **should not include:**

-   follow-up experiments aimed at testing or supporting an interpretation of
    the data

-   statistical hypothesis testing (e.g. tests of statistical significance,
    identifying differentially expressed genes, trend analysis, etc.)

-   exploratory computational analyses like clustering and annotation enrichment
    (e.g. GO analysis).

# Usage Notes (required)
The Usage Notes should contain brief instructions to assist other researchers
with reuse of the data. This may include discussion of software packages that
are suitable for analysing the assay data files, suggested downstream processing
steps (e.g. normalization, etc.), or tips for integrating or comparing the data
records with other datasets. Authors are encouraged to provide code, programs or
data-processing workflows if they may help others understand or use the data.

For studies involving privacy or safety controls on public access to the data,
this section should describe in detail these controls, including how authors can
apply to access the data, what criteria will be used to determine who may access
the data, and any limitations on data use.

# Acknowledgements (optional)
The Acknowledgements should contain text acknowledging non-author contributors.
Acknowledgements should be brief, and should not include thanks to anonymous
referees and editors or effusive comments. Grant or contribution numbers may be
acknowledged.

# References (required)
Bibliographic information for any works cited in the above sections, using the
standard *NPS NR Publication Series* referencing style.

In line with emerging [industry-wide standards for data
citation](https://www.nature.com/articles/sdata2018259), references to all
datasets described or used in the manuscript should be cited in the text and
listed in the ‘References’ section in the same manner as a conventional
literature reference.

ITIS. 2020. Integrated Taxonomic Information System. Available at: https://www.itis.gov/ (accessed 29 January 2020).

National Park Service (NPS). 2010. Draft Reference Manual RM 66B: Handling Protected Information. National Park Service, Washington, DC. (Available at https://irma.nps.gov/DataStore/Reference/Profile/2224216)

National Park Service (NPS). 2019. NPSpecies - the National Park Service biodiversity database. Available at: https://irma.nps.gov/NPSpecies/ (accessed xx).

Office of Management and Budget (OMB). 2013. Open Data Policy-Managing Information as an Asset. Office of Management and Budget. (Available at https://digital.gov/open-data-policy-m-13-13/)

U.S. Fish & Wildlife Service (USFWS). 2019. ECOS Environmental Conservation Online System. Available at: https://ecos.fws.gov/ecp/ (accessed xx).

U.S. Government Printing Office (GPO). 2013. Making Open and Machine Readable the New Default for Government Information. Executive Order 13642.(Available at https://www.govinfo.gov/content/pkg/CFR-2014-title3-vol1/pdf/CFR-2014-title3-vol1-eo13642.pdf)


\pagebreak

# Appendix C. R Code Listing

```r
# This setup code loads both reproducible reporting packages
# (delete those not needed) and packages for the actual project.
# Note that it also generates the start of a BibTex literature cited
# including the citations for R and all used packages

# reproducible reporting packages
RRpackages <- c('markdown',     # links to Sundown rendering library
                'rmarkdown',    # newer rendering via pandoc
                'pander',       # alternative renderer for markdown,
                                # plus better tables than just knitr
                'knitr',
                "dataMaid",     # for makeCodebooks
                "R.rsp",        # dynamic generation of scientific reports
                "kimisc",       #
                "papeR",        # stat tables
                "texreg",       # formatting regression results for LaTeX
                                # or html
                "rmdHelpers",   # misc from Mark Peterson
                                #  thisFileName() thisFile_knit()
                'yaml',         # format data into markdown
                'rmdformats',   # templates including automatic ToC,
                                # also use_bookdown()
                'htmltools',    #
                "bibtex",
                "RefManageR",   # BibTeX reference manager
                "knitcitations" #
                )

inst <- RRpackages %in% installed.packages()
if (length(RRpackages[!inst]) > 0) {
   install.packages(RRpackages[!inst], dep = TRUE)
}
lapply(RRpackages, library, character.only = TRUE)

# __________________________________
# Now repeat for packages used in the analyses
pkgList <- c("devtools",
             "RODBC", 
             "EML",
             "EMLassemblyline",
             "flextable",
             "english",
             "dplyr")
inst <- pkgList %in% installed.packages()
if (length(pkgList[!inst]) > 0) {
   install.packages(pkgList[!inst], dep = TRUE, 
                    repos = "https://cloud.r-project.org")
}

lapply(pkgList, library, character.only = TRUE, quietly = TRUE)

# create stub of citations for packages
pkgBibTex <- lapply(c("base", pkgList, RRpackages), citation)

# pkgBibTex <- do.call()

knitr::opts_chunk$set(
   root.dir = params$projectDir,  # from YAML parameter, knitr instead of setwd()
   echo = TRUE,
   comment = " ",
#   dev = "svg",
   fig.path = "figures/",
   tidy.opts = list(width.cutoff = 60),
   tidy = TRUE
   )
# if ggplot, update theme to default to centered titles
if ("ggplot2" %in% .packages()) {
   theme_update(plot.title = element_text(hjust = 0.5))
}

setwd(params$projectDir)

# Write YAML parameters to file for consistent reuse across report and data packages
save(params,file="./data/temp/reportParameters.RData")
# Load datasets for use
sessionInfo()
Sys.time()
```

\pagebreak

# Appendix D. R Session and Version Information

```
  R version 3.6.2 (2019-12-12)
  Platform: x86_64-w64-mingw32/x64 (64-bit)
  Running under: Windows 10 x64 (build 17134)
  
  Matrix products: default
  
  locale:
  [1] LC_COLLATE=English_United States.1252 
  [2] LC_CTYPE=English_United States.1252   
  [3] LC_MONETARY=English_United States.1252
  [4] LC_NUMERIC=C                          
  [5] LC_TIME=English_United States.1252    
  
  attached base packages:
  [1] stats     graphics  grDevices utils     datasets  methods   base     
  
  other attached packages:
   [1] english_1.2-5         flextable_0.5.9       EMLassemblyline_2.6.1
   [4] EML_2.0.2             RODBC_1.3-16          devtools_2.2.2       
   [7] usethis_1.5.1         knitcitations_1.0.10  RefManageR_1.2.12    
  [10] bibtex_0.4.2.2        htmltools_0.4.0       rmdformats_0.3.7     
  [13] yaml_2.2.1            rmdHelpers_1.2        dplyr_0.8.5          
  [16] texreg_1.36.23        papeR_1.0-4           xtable_1.8-4         
  [19] car_3.0-7             carData_3.0-3         kimisc_0.4           
  [22] R.rsp_0.43.2          dataMaid_1.4.0        knitr_1.28           
  [25] pander_0.6.3          rmarkdown_2.1         markdown_1.1         
  
  loaded via a namespace (and not attached):
   [1] colorspace_1.4-1  ellipsis_0.3.0    rio_0.5.16        rprojroot_1.3-2  
   [5] base64enc_0.1-3   fs_1.4.1          remotes_2.1.1     fansi_0.4.1      
   [9] lubridate_1.7.4   xml2_1.3.0        R.methodsS3_1.8.0 robustbase_0.93-6
  [13] pkgload_1.0.2     jsonlite_1.6.1    R.oo_1.23.0       compiler_3.6.2   
  [17] httr_1.4.1        backports_1.1.5   assertthat_0.2.1  lazyeval_0.2.2   
  [21] cli_2.0.2         formatR_1.7       prettyunits_1.1.1 tools_3.6.2      
  [25] gtable_0.3.0      glue_1.4.0        gmodels_2.18.1    V8_3.0.2         
  [29] Rcpp_1.0.4        cellranger_1.1.0  vctrs_0.2.4       gdata_2.18.0     
  [33] xfun_0.12         stringr_1.4.0     ps_1.3.2          openxlsx_4.1.4   
  [37] testthat_2.3.2    lifecycle_0.2.0   gtools_3.8.2      jqr_1.1.0        
  [41] DEoptimR_1.0-8    MASS_7.3-51.4     scales_1.1.0      jsonld_2.1       
  [45] hms_0.5.3         curl_4.3          memoise_1.1.0     gridExtra_2.3    
  [49] ggplot2_3.3.0     gdtools_0.2.2     stringi_1.4.6     desc_1.2.0       
  [53] emld_0.4.0        pkgbuild_1.0.6    zip_2.0.4         rlang_0.4.5      
  [57] pkgconfig_2.0.3   systemfonts_0.1.1 evaluate_0.14     purrr_0.3.3      
  [61] processx_3.4.2    tidyselect_1.0.0  plyr_1.8.6        magrittr_1.5     
  [65] bookdown_0.18     R6_2.4.1          pillar_1.4.3      haven_2.2.0      
  [69] foreign_0.8-72    withr_2.1.2       abind_1.4-5       tibble_3.0.0     
  [73] crayon_1.3.4      uuid_0.1-4        officer_0.3.8     grid_3.6.2       
  [77] readxl_1.3.1      data.table_1.12.8 callr_3.4.3       forcats_0.5.0    
  [81] digest_0.6.25     R.cache_0.14.0    R.utils_2.9.2     munsell_0.5.0    
  [85] sessioninfo_1.1.1
```

```
  [1] "2020-04-10 17:06:53 MDT"
```

# Additional Notes (this should not be included in reports...)

## Figures

Figure images should be included in-text near the initial point of reference.

Figure captions begin with a brief title sentence summarizing the purpose of the figure as a whole, and continue with a short description of what is shown in each panel and an explanation of any symbols used. Legends must total no more than 350 words, and may contain literature references. The first sentence of the legend will be used as the title for the figure. It (the first sentence) should contain no references of any kind, including to specific figure panels, bibliographic citations or references to other figures or panels.

## Tables
Authors are encouraged to provide one or more tables that provide basic
information on the main ‘inputs’ to the study (e.g. samples, participants, or
information sources) and the main data outputs of the study; also see the
additional information on providing metadata on page 6. Tables in the manuscript
should generally not be used to present primary data (i.e. measurements). Tables
containing primary data should be submitted to an appropriate data repository.

Authors may provide tables within text near the initial citation or as an
appendix. Legends, where needed, should be included in the Word document.
Generally, a Data Publication Report should have fewer than ten tables, but more
may be allowed when needed.

### Example Data Record Summary Tables
Here, we provide four generic ‘Table 1’ examples, including two experimental
study examples, one observational study example, and an example for an
aggregated dataset of the type that may result from a meta-analysis. 

**Table 1.** Experimental study example Data Records table. 

| **Subjects** | **Protocol 1** | **Protocol 2**   | **Protocol 3** | **Protocol 4** | **Data** |
|--------------|----------------|------------------|----------------|----------------|----------|
| Mouse1       | Drug treatment | Liver dissection | RNA extraction | RNA-Seq        | GEOXXXXX |
| Mouse2       | Drug treatment | Liver dissection | RNA extraction | RNA-Seq        | GEOXXXXX |
| Mousen       | Drug treatment | Liver dissection | RNA extraction | RNA-Seq        | GEOXXXXX |

**Table 2.** Experimental study with replicates Data Records table.

| **Source**   | **Protocol 1** | **Protocol 2** | **Samples**    | **Protocol 3**           | **Data** |
|--------------|----------------|----------------|----------------|--------------------------|----------|
| CellCulture1 | Drug treatment | RNA extraction | TechnicalRep1a | Microarray hybridization | GEOXXXXX |
| CellCulture1 | Drug treatment | RNA extraction | TechnicalRep2a | Microarray hybridization | GEOXXXXX |
| CellCulture1 | Drug treatment | RNA extraction | TechnicalRep3a | Microarray hybridization | GEOXXXXX |
| CellCulture2 | Drug treatment | RNA extraction | TechnicalRep1b | Microarray hybridization | GEOXXXXX |
| CellCulture2 | Drug treatment | RNA extraction | TechnicalRep2b | Microarray hybridization | GEOXXXXX |
| CellCulture2 | Drug treatment | RNA extraction | TechnicalRep3b | Microarray hybridization | GEOXXXXX |

**Table 3.** Observational study example Data Records table.

| **Sample**      | **Geographical location** | **Geoposition**               | **Protocol**                       | **Data**  |
|-----------------|---------------------------|-------------------------------|------------------------------------|-----------|
| Body of water 1 | location name             | latitude, longitude, altitude | Measurement of surface temperature | dataFile1 |
| Body of water 2 | location name             | latitude, longitude, altitude | Measurement of surface temperature | dataFile2 |
| Body of water n | location name             | latitude, longitude, altitude | Measurement of surface temperature | dataFile3 |

**Table 4.** Data aggregation study example Data Records table.

| **Source**     | **Sample** | **Sample number**                | **Temporal range**                            | **Protocol 1**              | **Protocol 2**                 | **Data**  |
|----------------|------------|----------------------------------|-----------------------------------------------|-----------------------------|--------------------------------|-----------|
| Database URL 1 | Dataset 1  | Number of samples in the dataset | Range of measurements reported in the dataset | Data assimilation procedure | Method to generate output data | dataFile1 |
| Database URL 1 | Dataset 2  | Number of samples in the dataset | Range of measurements reported in the dataset | Data assimilation procedure | Method to generate output data | dataFile1 |
| Database URL 2 | Dataset n  | Number of samples in the dataset | Range of measurements reported in the dataset | Data assimilation procedure | Method to generate output data | dataFile2 |