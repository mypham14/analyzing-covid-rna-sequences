# SARS-CoV-2 Genome Analysis Project

## Overview

This project involves the analysis of genomic data related to the Severe Acute Respiratory Syndrome Coronavirus 2 (SARS-CoV-2). The data is sourced from the National Center for Biotechnology Information (NCBI) and includes various metadata and nucleotide sequences of the virus. The project aims to explore and analyze the genomic data to gain insights into the virus's characteristics and its variants.

## Data Sources

- **NCBI GenBank Viral Genomes:** [Download URL](https://ftp.ncbi.nlm.nih.gov/genomes/genbank/viral/Severe_acute_respiratory_syndrome-related_coronavirus/latest_assembly_versions/)
- **Documentation:** [NCBI Datasets Documentation](https://www.ncbi.nlm.nih.gov/datasets/docs/v1/data-packages/sars-cov-2-genome/)
- **Many Records Download URL:** [NCBI Coronavirus Genomes](https://www.ncbi.nlm.nih.gov/datasets/coronavirus/genomes/)
- **Variant Information:** [CDC Variant Classifications](https://www.cdc.gov/coronavirus/2019-ncov/variants/variant-classifications.html)

## Dataset

The dataset used in this analysis is available for download at the following link: [Download ncbi_datasets.csv](https://drive.google.com/file/d/1S2ZDjdRkY78kZxBtc9YNUh0mByTHXQ23/view?usp=sharing).

### Columns

- `nucleotide_accession`: Accession number of the nucleotide sequence.
- `species_taxonomy_id`: Taxonomy ID of the species.
- `species_name`: Name of the species.
- `virus_genus`: Genus of the virus.
- `virus_family`: Family of the virus.
- `isolate_name`: Name of the isolate.
- `nucleotide_length`: Length of the nucleotide sequence.
- `sequence_type`: Type of sequence (e.g., RefSeq, GenBank).
- `nuc_completeness`: Completeness of the nucleotide sequence.
- `geo_location`: Geographical location of the isolate.
- `us_state`: US state where the isolate was collected (if applicable).
- `host_name`: Name of the host.
- `host_taxonomy_id`: Taxonomy ID of the host.
- `collection_date`: Date of collection.
- `bioproject`: BioProject ID.
- `biosample`: BioSample ID.
- `continent`: Continent of the geo location.

## Data Analysis

The dataset contains 847,791 records with 17 columns. The columns have been renamed to use lowercase and underscores instead of spaces for easier handling in code.

### Analysis Performed

1. **Earliest Collection Date by Continent:**
   - The earliest collection date for each continent was identified.

2. **Nucleotide Length Statistics:**
   - Count: 847,791
   - Mean: 29,825.75
   - Standard Deviation: 69.94
   - Minimum: 2,859
   - 25th Percentile: 29,786
   - Median (50%): 29,819
   - 75th Percentile: 29,884
   - Maximum: 30,018

3. **Sequence Analysis**
   - The sequence with the minimum nucleotide length is from Europe, with a length of 2,859.
   - The reference sequence (NC_045512.2) has a nucleotide length of 29,903.
   - The sequences identified as "Delta" and "Omicron" variants have nucleotide lengths of 29,858 and 29,788 respectively.

## Sequence Alignment

The sequences for the following accessions were downloaded and aligned:
- NC_045512.2 (Reference)
- OM061695.1 (Delta)
- OM095411.1 (Omicron)

The alignment was performed using the Needleman-Wunsch algorithm. The alignment results show the differences between the sequences, with mismatches highlighted in color.

### Sequence Alignment Differences
- **Red:** Deletions in the reference sequence
- **Green:** Insertions in the Delta sequence
- **Blue:** Substitutions

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- NCBI for providing the genomic data.
- CDC for variant classification information.
