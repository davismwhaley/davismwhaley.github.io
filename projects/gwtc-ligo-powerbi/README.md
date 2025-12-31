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

- **Mass1 vs Mass2 Scatterplot (ligo1)**

  <figure>
  <img src="ligo1.1.webp" alt="Mass1 vs Mass2 scatterplot" width="650">
</figure>  
  This shows the main populations of binary black holes and the lower-mass neutron star systems. Bigger dots represent louder, clearer signals detected on Earth. Clusters of heavy pairs indicate typical black-hole mergers, while the small-mass events represent neutron-star collisions.
</figure>
<br><br>

- **Network SNR vs Distance_MPC (ligo2)**

  <figure>
  <img src="ligo2.1.webp" alt="Network SNR vs. Distance_MPC" width="650">
</figure>
  Each dot is a real cosmic collision showing how signal strength drops as the event gets farther away. Louder signals (bigger dots) come from either closer events or especially massive systems. This helps illustrate why LIGO can detect some huge mergers across billions of light-years but misses faint, distant ones.
</figure>
<br><br>

- **Chirp Mass Histogram (ligo3)**

  <figure>
  <img src="ligo3.1.webp" alt="Event Name vs ChirpMass" width="650">
</figure>
   Highlights the dominant population of stellar-mass black hole mergers around ~20–35 M☉, the neutron-star tail at low masses, and the rarer high-mass mergers, and whether the mergers were spinning in alignment with their orbit or not. Most events cluster near zero, meaning their spins didn’t strongly line up — an important clue about how these binary systems formed in space. Over time, you can see how the population stays mostly stable, suggesting consistent cosmic behavior across LIGO’s observing years.
</figure>
<br><br>

- **Effective Spin (χ_eff) vs Event Number (ligo5)**

  <figure>
  <img src="ligo5.1.webp" alt="Event Number vs Effective Spin" width="650">
</figure>
  This chart groups mergers by a special combination of masses called “chirp mass,” which controls how quickly the frequency rises during the inspiral (“the chirp”). Peaks in the histogram show the most common types of mergers LIGO sees. Bubble size encodes chirp mass. This reveals the natural population of stellar-mass black holes in the universe.

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
