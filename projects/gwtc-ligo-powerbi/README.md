# LIGO Gravitational Wave Catalog Dashboard (Power BI)

This project is an interactive Power BI dashboard built from the **LIGO–Virgo–KAGRA Gravitational-Wave Transient Catalog (GWTC)**. It visualizes black hole and neutron star merger events from GWTC-1 through GWTC-4 using real open data from the Gravitational Wave Open Science Center (GWOSC).

## Data

- Source: Gravitational Wave Open Science Center (GWOSC) – GWTC event catalogs  
- Content: One row per event, including component masses, chirp mass, luminosity distance, network SNR, effective spin (χ_eff), and catalog release flags.

The raw event table was cleaned and lightly transformed in Power BI (e.g., derived mass ratio, chirp-mass bins, and simple log-distance fields).

## Key Terms in the LIGO Power BI Dashboard

**NetworkSNR:** The combined signal-to-noise ratio from all LIGO/Virgo detectors, measuring how “loud” or confidently detectable a gravitational-wave event was.

**Distance_Mpc:** The luminosity distance to the merger in megaparsecs (Mpc), representing how far away the signal originated in the universe.

**CatalogRelease:** The official dataset (GWTC-1, GWTC-2.1, GWTC-3, GWTC-4) in which the event was published, corresponding to different LIGO/Virgo observing runs.

**ChirpMass_MSun:** A specific combination of the two black hole masses (in solar masses) that largely determines the frequency evolution—or "chirp"—of the gravitational-wave signal.

**Mass1_Msun:** The estimated mass of the heavier object in the binary system, measured in solar masses.

**Mass2_Msun:** The estimated mass of the lighter object in the binary system, measured in solar masses.

**ChirpMass_Bins:** Grouped ranges (bins) of chirp mass used for histograms, revealing the distribution of event types (e.g., neutron-star vs black-hole systems).

**EventName:** The official LIGO/Virgo identifier of each gravitational-wave event, usually containing the date of detection (e.g., GW150914).

**Event Number (EventIndex):** The chronological index of events, allowing trends to be seen over time independent of catalog or naming.

**Effective Spin (χ_eff):** A quantity between –1 and +1 measuring how much the black holes’ spins are aligned with the orbital angular momentum; it influences the waveform shape and encodes astrophysical formation clues.

## Dashboard Features

The `.pbix` file contains several pages/visuals, including:

- **Mass1 vs Mass2 Scatterplot (ligo1)**  
  - Each point is a merger event; point size encodes network SNR, and color encodes catalog release.  
  - Shows the main populations of binary black holes and the lower-mass neutron star systems.

- **Network SNR vs Luminosity Distance (ligo2)**
  - Nearby events produce higher SNR and appear higher on the plot compared to more distant.
  - Shows LIGO’s selection bias: detectors preferentially “see” louder (often heavier) mergers farther away.
  
- **Chirp Mass Histogram (ligo3)**  
  - Binned distribution of chirp mass across GWTC-1–4.  
  - Highlights the dominant population of stellar-mass black hole mergers around ~20–35 M☉, the neutron-star tail at low masses, and the rarer high-mass mergers.

- **Effective Spin (χ_eff) vs Event Number (ligo5)**  
  - Events ordered chronologically on the x-axis with χ_eff on the y-axis (range –1 to +1).  
  - Bubble size encodes chirp mass; color encodes catalog (O1/O2/O3/O4).  
  - Shows that most observed mergers have χ_eff ≈ 0, with a few positively and negatively aligned outliers, consistent with current population studies.

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
