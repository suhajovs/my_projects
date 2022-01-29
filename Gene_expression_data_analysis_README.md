# Semestral project
author: Simona Šuhajová
data:   18.6. 2021


## Assigment:
 - the main goal was to do an analysis on a selected experiment
 - this analysis is located in semestral_project.Rmd

### structure of files and directories
age_library.R - contains function for to create plots as a histogram, PCA, heatmap, heatmaply, boxplots and some computional functions

report.R - contain function for to create html reports for groups created by DEA model (Differential expression analysis)

semestral_project:
    data  
        - contain experimental data  
            E-MTAB-6909 
                - directory, which contained CEL files (data of experiment)
                - data can be downloaded from website: https://www.ebi.ac.uk/arrayexpress/experiments/E-MTAB-6909/
              
                E-MTAB-6909.sdrf.txt  
                    - sample sheet file
                    - file can be downloaded from the same website as the CEL files

    kegg_data_Acp: 
        - contain images of biological pathways gain by SPIA for group: control-mouse with knockout Acp gene
        - contained xml files downloaded from KEGG database for SPIA, this data can be downloaded by running code from semestral_project.Rmd
        
    kegg_data_Acp_Msx1: 
        - contain images of biological pathways gain by SPIA for group: control-mouse with knockout Acp and Msx1 gene
        - contained xml files downloaded from KEGG database for SPIA, this data can be downloaded by running code from semestral_project.Rmd
    
    images:
            ma_plot.png
                - contain MA plot for each sample with each
            gsea_cnetplot_Acp.png
                - netplot linking biological pathways and significantly expressed genes of group control vs mouse with knockout Acp gene
            gsea_cnetplot_Acp_Msx1.png
                - netplot linking biological pathways and significantly expressed genes of group control vs mouse with knockout Acp and Msx1 gene
            gsea_heatmap_Acp.png
                - heatmap shows where genes belong and their logFC of group control vs mouse with knockout Acp gene
            gsea_heatmap_Acp_Msx1.png
                - heatmap shows where genes belong and their logFC of group control vs mouse with knockout Acp and Msx1 gene
    
    reports:
        dea_signpost.html
            - signpost to HTML pages that contain links to HTML pages for tables of groups
        groupApc_knockout.html
            - contains table with data of group control-mouse with knockout Acp
        groupApc_and_Msx1_knockout.html
            - contains table with data of group control-mouse with knockout Acp and Msx1 gene
        dea_signpost.Rmd 
            - template of signpost html page in Rmd format 
        dea_table_template.Rmd 
            - template for HTML page for table of groups (control vs mouse with knockout Acp gene, control vs mouse with knockout Acp and Msx1 gene)
            
    semestral_project.Rmd
        - analysis of the selected experiment
    semestral_project.html
        - semestral_project.Rmd rendered to HTML page


### running programs
- data from selected experiment was downloaded from website 
- results as images, kegg_data and reports was obtained by running code in file semestral_project.Rmd
- in dea_signpost.html are links to other htmp pages but this links not run in RStudio (RStudio create another paths) so run in enviroment where path is the same as path for dea_signpost.html

### libraries for running code in R
- for running code in semestral_project.Rmd need install the libraries:   mogene20sttranscriptcluster.db
                                                                      affycoretools
- possibly other libraries that need to be installed (but can be installed in virtual machine):   dendextend
                                                                                                  here
                                                                                                  tidyverse
                                                                                                  patchwork
                                                                                                  ComplexHeatmap
                                                                                                  SPIA
- it needed to be install BiocManger version 3.13
                                                                      
                                                                      
                                                                      
                                                                      
                                                                      
                                                                      
                                                                      
                                                                      
                                                                      
                                                                      