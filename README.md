# Alzheimers-bioinformatics-resource
Contains computer code and data to investigate Alzheimer's disease genome-wide association regions for regulatory function

These files contain the computer code and data used to generate the Tables and Results for the paper “Bioinformatics strategy to advance the interpretation of Alzheimer’s disease GWAS discoveries: the roads from association to causation”.
A prototype bioinformatics pipeline was developed in visual basic for applications (VBA).  The decision to use visual basic for applications was based on the availability of tabular data from the UCSC Table Browser.  These data were imported into EXCEL and the overlap calculations performed using the VBA code.  For calculations for <100 regions, this code is a simple approach to implement.  For larger, genome-scale calculations, R-based code would be a possible choice using the VBA code as examples and using R table data structures instead of the worksheets.

The VBA code and all data is contained in the file “gene region map hotspots.xlsm” for CTCF hotspots and “gene region map peaks.xlsm” for CTCF peaks.  Documentation within the code indicates which worksheets/tables are input and which are output tables that result from operation of specific subroutines in the code.  For general use, these worksheets would be populated for analysis: genes, regions, adjusted_regions, CTCF_input, enhancers_input, totals.  These tables can be modified for the specific genes and regions of interest.  

The computer code is also contained in the file computer code.txt, which includes detailed comments on the code and input/output tables.

All data loaded from the UCSC Genome browser (GRCh37/hg19) was current as of 7/18/2018.

Several output datasets are included as .csv files for downstream analysis:

Enhancer ctcf overlap.csv contains overlap calculations for all the regions considered in the paper based on CTCF hotspots.

Mapped genes complete.csv contains a list of all genes mapped to the specific input genes and SNPs including genomic coordinates.  This file only contains valid entries where the gene is completely contained in the target adjusted region.

Mapped genes.csv is a full mapping of all genes mapped to the specific input genes and SNPs including genomic coordinates.  In this case, gene structure has to overlap with the target region, but the restriction of the gene being completely contained in the target adjusted region is relaxed.
