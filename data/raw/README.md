# Original source data

The two original CSVs were supplied by Noah Nentwig on 2 November 2026 and are included unchanged:

- `renewable_energy_readings.csv`: 17,947 raw rows, 34 reporting country IDs, years 2015–2025.
- `countries.csv`: 38 country metadata rows. Four countries have no readings in the supplied dataset.

The notebook removes exact duplicates excluding `record_id` before analysis. Provider names, policy targets and population values are supplied metadata. The original download location, external provenance and license have not been independently verified; no open-data license is asserted.
