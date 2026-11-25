## Required columns

### `KRA21_sources.csv`
- `Name` (sample label)
- `Group` (source name)
- `Rb`, `Sr`, and `Zr` (numeric concentrations)

### `study_samples.csv`
- `Sample` (sample label)
- `Group` (study group)
- Rb, Sr, and Zr concentrations (numeric). Bruker names such as `RbKa1`,
  `SrKa1`, and `ZrKa1` are normalized automatically.

Both tables must include `Group` and the three plotted elements. Rows without
usable Rb, Sr, or Zr values are excluded from the visualizations.