Jupyter Notebooks to process Orbitrap isotope data:
  Orbitrap-data-sort-bracketing:
    Processes a 'Aditional-data' file output by Thermo R script for a sequence of injections, and calculates isotope deltas for each sample injection by bracketing, then conversion to international scale using known delta values of internal standard. 
    Allows filtering of bad injections
    Calculates deltas from no-M0 data when given the internal deltas from the corresponding M0 experiment
    No delta scale calibration
    Saves a '-sorted' csv for each injection
    Outputs 'internal_deltas' (relative to std) and 'external_deltas' (relative to international scale) files, summarising all injections
  Orbitrap-delta-calibration:
    Using the known delta values of any dried standards present in an 'extenal_deltas' file, calculates a 1-point, 2-point, or multiple-point linear regression for measured vs true delta values. Calibrates all samples.
    Outputs a 'calibrated_deltas' file, with delta values of all samples.
  Orbitrap-results-collate:
    Collates M0 and no-M0 results for the same experiment, calculates capital deltas for MIF and clumps
    Saves in a single file
  Orbitrap-vs-IRMS:
    Plots the comparison of IRMS isotope deltas with Orbitrap isotope deltas

Jupyter Notebooks for Orbitrap statistical tests:
  Allan-save:
    Calculates and saves the allan deviation, hadamard deviation and power spectrum for a single injection '-sorted' file as '-allan'
  Plot-drift-stats:
    Produces 4 tiled plots for each isotopologue, using '-sorted' and '-allan' files from a single (long) injection: 
    1. Autoreferenced delta for each scan
    2. 10 minute running mean delta
    3. Histogram showing delta distribution
    4. Allan deviation, Hadamard deviation and power spectrum

    
