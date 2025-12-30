# LIGO Gravitational Wave Catalog Dashboard (Power BI)

This project is an interactive Power BI dashboard built from the **LIGO–Virgo–KAGRA Gravitational-Wave Transient Catalog (GWTC)**. It visualizes black hole and neutron star merger events from GWTC-1 through GWTC-4 using real open data from the Gravitational Wave Open Science Center (GWOSC).

## Data

- Source: Gravitational Wave Open Science Center (GWOSC) – GWTC event catalogs  
- Content: One row per event, including component masses, chirp mass, luminosity distance, network SNR, effective spin (χ_eff), and catalog release flags.

The raw event table was cleaned and lightly transformed in Power BI (e.g., derived mass ratio, chirp-mass bins, and simple log-distance fields).

## Dashboard Features

The `.pbix` file contains several pages/visuals, including:

- **Mass1 vs Mass2 Scatterplot (ligo1)**  
  - Each point is a merger event; point size encodes network SNR, and color encodes catalog release.  
  - Shows the main populations of binary black holes and the lower-mass neutron star systems.

- **Chirp Mass Histogram (ligo3)**  
  - Binned distribution of chirp mass across GWTC-1–4.  
  - Highlights the dominant population of stellar-mass black hole mergers around ~20–35 M☉, the neutron-star tail at low masses, and the rarer high-mass mergers.

- **Effective Spin (χ_eff) vs Event Number (ligo5)**  
  - Events ordered chronologically on the x-axis with χ_eff on the y-axis (range –1 to +1).  
  - Bubble size encodes chirp mass; color encodes catalog (O1/O2/O3/O4).  
  - Shows that most observed mergers have χ_eff ≈ 0, with a few positively and negatively aligned outliers, consistent with current population studies.

Additional pages experiment with SNR vs distance, catalog-based filtering, and basic slicers for exploring subsets of events.

## How to Use

1. Download `GWTC_Events.pbix` from this folder.
2. Open it in **Microsoft Power BI Desktop** (free download from Microsoft).
3. Use the slicers and filters to:
   - focus on specific catalogs (e.g., GWTC-3 only),
   - explore different mass ranges,
   - examine how SNR and distance interact with mass and spin.

If you want to reproduce or extend the model, you can start from the provided Excel/CSV event table (`gwtc_events.xlsx`) or swap in newer GWTC releases.

## Skills Demonstrated

- Working with **real astrophysics data** from GWOSC  
- Data cleaning and feature engineering in Power BI (mass ratio, chirp-mass bins, etc.)  
- Designing publication-style scientific visuals (scatterplots, histograms, spin vs event number)  
- Communicating physical insights about black hole masses, spins, and selection effects in a dashboard format

## Credits

- Data from the **LIGO–Virgo–KAGRA Collaboration** via the Gravitational Wave Open Science Center (GWOSC).  
- Interpretation and visual design by Davis Whaley.
