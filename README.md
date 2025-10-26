# Redefining separate or integrated food waste and wastewater streams for 29 large cities
# Urban Biowaste Flux (UBF) Model — README

## Overview
The Urban Biowaste Flux (UBF) model takes a small set of inputs—waste composition and treatment parameters—and simultaneously quantifies:
- Mass flows
- Energy demand
- Operational costs
- Greenhouse gas (GHG) emissions

All results update automatically when you run scenarios from the uncertainty sheet.

## 1) Plant Overview
- Purpose: Visualizes mass fluxes from food waste and wastewater generation through each treatment unit to final disposal.
- Dynamic updates: All flux values refresh when scenarios are run in the uncertainty sheet.
- COD balance check: See cells AL43–AT52 to verify COD balances for all bioreactions.

## 2) Uncertainty
This sheet contains buttons to run simulations, sensitivity/uncertainty analyses, and generate Sankey diagrams.

Button name — Function — Output
- Treatment Method — Simulate the four treatment strategies described in the manuscript — Sheets: CEPT&Inc; CEPT&Landfill; AO&Inc; AO&Landfill
- Sensitivity Analysis 0% — Run sensitivity analysis with FWDR = 0% — Sheets: sensitivity plot 0%, Paper results
- Sensitivity Analysis 50% — Run sensitivity analysis with FWDR = 50% — Sheets: sensitivity plot 50%, Paper results
- Uncertainty Analysis — Full uncertainty analysis for Hong Kong across all parameters — Sheet: uncertainty, cells Z49:EG11049
- Sankey Diagram 0% — Generate Sankey at FWDR = 0%; mass flux in Plant Overview; breakdown in EI–SR — Sheet: uncertainty, columns EI–SR
- Sankey Diagram 10%, 20%, … 100% — Same as above for FWDR = 10%, 20%, … 100% — Sheet: uncertainty, columns EI–SR
- Megacities — Batch run for 29 cities at FWDR = 0% and 50%; results in EI–SR — Sheet: uncertainty, columns EI–SR
- Megacity 1–29 — Run individually for each of the 29 cities (buttons in column W) — Sheet: uncertainty, columns EI–SR

Note: FWDR = Food Waste Diversion Rate.

## 3) LCI
- Definition: The Life Cycle Index (LCI) converts mass fluxes into GHG emissions, energy use, and operational costs.
- Location: Computed automatically in columns EI–SR.

## 4) How to Use the Model
Before you begin, ensure Excel macros are enabled:
File → Options → Trust Center → Trust Center Settings → Macro Settings → Enable all macros

Steps:
1) Open the uncertainty sheet.
2) Click the desired button: Treatment Method, Sensitivity Analysis, Uncertainty Analysis, Sankey Diagram, or Megacities.
3) View results in:
   - Plant Overview (mass flux)
   - sensitivity plot 0% / sensitivity plot 50% (sensitivity results)
   - uncertainty, columns EI–SR (GHG, energy, cost)
   - uncertainty, cells Z49:EG11049 (Hong Kong uncertainty analysis)

## Notes
- File: UBF model.xlsm (enable macros for full functionality).
- Some outputs are large; calculations may take time depending on your machine.
- If you modify parameters or add cities, re-run the relevant buttons to refresh results.
