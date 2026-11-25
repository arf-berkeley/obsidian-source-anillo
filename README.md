# Anillo Obsidian Geochemistry

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/arf-berkeley/obsidian-source-anillo/HEAD?urlpath=%2Fdoc%2Ftree%2Fnotebooks%2Fobsidian-geochem.ipynb)

This notebook compares the Anillo study samples with known obsidian source
chemistry using a biplot and a ternary diagram. It loads the two CSV files
included in `data/` automatically; no uploads, Google Sheets, or map selection
are required.

## Run the notebook

Open [the notebook](notebooks/obsidian-geochem.ipynb) in JupyterLab or VS Code
and run all cells. For a local Conda environment, run these commands from the
project directory:

```bash
conda env create -f environment.yml
conda activate obsidian-source-anillo
jupyter lab
```

The notebook loads [known source samples](data/KRA21_sources.csv) and
[study samples](data/study_samples.csv). See the [data README](data/README.md)
for the expected columns. Rows missing a sample name, group, Rb, Sr, or Zr
are excluded during loading.

## Explore the plots

- Choose the biplot's X and Y elements with the dropdowns; the default is
  Sr versus Zr.
- Choose the ternary plot's A, B, and C elements with its dropdowns; the
  default is Rb, Sr, and Zr. The plot uses each sample's selected element
  values as fractions of their sum. Rows with missing, negative, or zero-total
  compositions are omitted.
- The element choices are those with usable values in both data tables. Plots
  update when the selections change.
- **Show Labels** above either plot controls study sample labels on both.
  Ellipse labels identify the group and whether it is a source or study group;
  they remain visible when sample labels are hidden.
- Use the interactive legend to hide or show plotted groups.

Ellipses are estimated 95% bivariate normal data-spread contours based on each
group's sample covariance, not confidence intervals for the group mean. They
do not necessarily contain exactly 95% of observed samples; groups with too
little variation may produce degenerate ellipses.

## Export a PDF

Select **Export PDF** beneath either plot, then click the generated download
link. The vector PDF uses the selected elements and sample-label setting.
Exports include all groups, even those hidden using the interactive legend.
