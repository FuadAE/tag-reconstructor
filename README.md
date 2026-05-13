# tag-reconstructor

Bottom-up optimization framework to reconstruct triacylglycerol (TAG) mixtures that reproduce experimental fatty acid methyl ester (FAME) profiles.

## What this repository contains
- An RMarkdown notebook implementing:
  - TAG combinatorial generation
  - Greedy selection of candidate TAGs
  - Optimization of TAG mixture proportions
  - Optional comparison to experimental GC-FID replicates

## Expected input data
The pipeline expects tidy datasets with these columns:

### Required dataset (summary FAME profile)
- Treatment_ID
- Type
- FAME
- Mean_abundance
- rank (optional)

### Optional dataset (replicate-level FAME profile, used only for validation plots)
- Treatment_ID
- Type
- Peak#
- %FAME
- Lab_Tag

## Example data
Example input files are provided in the `data/` folder:
- data/example_top12_by_group.csv
- data/example_FAMEprofile.csv

## How to run
Open `analysis/tag-reconstructor.Rmd` in RStudio and click **Knit**.
