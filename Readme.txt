# FastCHO CRISPR Screen Data Analysis Repository

This repository contains all scripts and data necessary for the analysis and visualization of CRISPR screen data performed in CHO cells.  
Both R and Python environments are supported and fully documented.

--------------------------------------------------------------------------------
## Repository Structure

├── Python/  
│   ├── input_data/                # Input files (e.g., MAGeCK outputs, annotation files)  
│   ├── output_data/               # All generated plots and analysis results  
│   ├── .venv/                     # Python virtual environment (optional)  
│   ├── Heatmap_of_top_genes.ipynb # Jupyter Notebook for visualization  
│   ├── README.md                  # Python-specific instructions   
│   ├── MAGeck-Code.ipynb          # MAGeCK-specific instructions parameters used for read count normalization, gene ranking, and statistical testing  
│   └── requirements.txt           # Python dependencies  
│  
├── R/  
│   ├── input_data/                # Input datasets for R scripts  
│   ├── output_data/               # R analysis results and plots  
│   ├── R-Analysis.Rmd             # Main R Markdown script for full analysis  
│   ├── R-Analysis.html            # Rendered HTML report (if available)  
│   ├── R-Analysis-Files/          # Associated R Markdown files  
│   ├── .RData / .Rhistory          # R workspace files  
│   └── README.md                  # R-specific instructions  

--------------------------------------------------------------------------------
## Main Functionalities

### Python  
- Heatmap and bar plot visualization of top genes across gene set categories.  
- Automated functional group assignment using KEGG, GO, and Reactome pathways.  
- Final outputs saved to `/output_data/` directory.  

### To Run Python Scripts:

1. Create and activate virtual environment:

    python -m venv .venv  
    .venv\Scripts\activate      (on Windows)  
    source .venv/bin/activate   (on Unix)  

2. Install dependencies:

    pip install -r requirements.txt  

3. Run Jupyter Notebook:

    jupyter notebook Heatmap_of_top_genes.ipynb  

--------------------------------------------------------------------------------
### R  
- Full CRISPR screen data processing using MAGeCK outputs.  
- Hit calling, scoring, pathway enrichment (GSEA), and gene set generation.  
- Automatic export of results and figures for publication.  

### To Run R Scripts:

1. Open `R-Analysis.Rmd` in RStudio.  
2. Execute all chunks or knit the file to generate a full HTML report.  
3. Outputs are saved in the `/output_data/` directory.  

--------------------------------------------------------------------------------
## Input Files (Located in `input_data/`)

- MAGeCK-output/  
- deg_annotation_e.xlsx  
- DEG_Sets_metadata_v2.xlsx  
- Essentiality_Virus_Free_CRISPR.csv  
- kegg_pathway_categories.csv  
- ReadCountsCHOWGLV4.xlsx  

--------------------------------------------------------------------------------
## Output Files (Generated in `output_data/`)

- FastCHO_GSEA_Plots/    → GSEA dot plots  
- FastCHO_Plots/         → Scatter plots for CRISPR hits  
- Gene_Sets/              → Gene set curation results  
- DEG_comparison/         → DEG overlap analysis and heatmaps  
- Hit_Calls/               → Final selected gene hits  
- Scoring_Plots/           → Custom scoring visualizations  

--------------------------------------------------------------------------------
## Notes

- All scripts are fully annotated for ease of understanding.  
- Modify the abbreviations dictionary in Python scripts to change functional group names.  
- For R, adjust filtering thresholds directly in the R Markdown file.  

--------------------------------------------------------------------------------
