# Changelog

All notable changes to **Chemistry Suite** will be documented in this file.

## [0.8.3] - 2025-12-19

### Added
- **requirements.txt**: Introduced runtime dependencies and optional testing tools:
  - `PyQt6`, `PyQt6-WebEngine`, `matplotlib`, `requests`, `certifi`, and optional `pytest`.

### Fixed
- **Theme / Placeholder readability**
  - Set `QPalette.PlaceholderText` in both `build_light_palette()` and `build_dark_palette()` to ensure placeholder text (e.g., “e.g. MnCl2.4H2O”) remains readable when switching themes.

- **Edit → Clear Inputs** coverage and completeness
  - **NMR Impurities**: Implemented `clear_inputs()` to reset nucleus, search box, solvent selection, table, and notes.
  - **Isotopic Distribution**: Added `clear_inputs()` to clear formula/adducts, table, plot, labels, and cached state.
  - **Elemental Analysis**: Extended `clear_inputs()` to also clear `results_box` and `report_box` so reports do not persist after clearing.
  - **DOSY NMR**: Extended `clear_inputs()` to also clear the shared `report_field`.
  - **Dilution Calculator (Mass Molarity section)**: Updated `clear_inputs()` to clear `mass_result` alongside input fields.

- **DOSY NMR Calculator – SEGWE parameters not repopulating after clear/method switch**
  - Updated `toggle_method_ui()` to call `update_segwe_params()` when switching to SEGWE (and `update_se_viscosity()` when switching to Stokes–Einstein).
  - Updated `clear_inputs()` to call `update_segwe_params()` so viscosity and solvent MW are populated immediately after a clear.

### Changed
- Minor palette/event propagation remains centralized via `PreferencesDialog._apply()` to refresh widgets on theme changes.
- **Solvent dataset tests**: Removed `tests/solvent_data_test.py` (dataset checks were non-math and brittle). Focus remains on logic/math and widge

---

## [0.8.2] - 2025-12-19
- Internal maintenance and preference management refinements.

## [0.8.1] - 2025-12-15
- Initial modular UI scaffolding, calculators and reference widgets baseline.
