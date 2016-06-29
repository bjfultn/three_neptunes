## Machine-Readable data files for "Three Temperate Neptunes"
#### (insert url here)

### Description of files:

##### {star}\_detrendpars\_{instrument}.csv
  - These files contain the radial velocities (RVs) before and after the
    detrending process described in Section 2 of the manuscript.
  - There are separate files for APF, pre-upgrade (before 2004) Keck/HIRES,
    and post-upgrade Keck/HIRES
  - The detrending is applied to each insturment separately and the
    resulting detrended RVs are stitched back together
  - All environmental and PSF parameters that were searched for 
    correlations with RV are included in these files whether or
    not they were actually found to have significant correlations
  - Environmental parameters (e.g. pressure) are not available for Keck/HIRES

| **Column** | **Description** | **Units** |
| :---:  | :--- | :--- |
| **HJD_UTC**  | HJD_UTC-2440000 | JD |
| **VEL**  | Relative RV before detrending | m s<sup>-1<sup> |
| **1--18**  | PSF parameters 1--18 (amplitudes of the Gaussian's) |  |
| **err**  | Velocity uncertainty | m s<sup>-1<sup> |
| **cts**  | Counts near 5500 Angstroms | ADU |
| **el**  | Telescope elevation - mean(elevation) | degrees |
| **spectemp**  | Temperature inside spectrograph - mean(temperature) | C |
| **ccdtemp**  | Temperature of the CCD - mean(temperature) | C |
| **dewfoc**  | Position of the dewar focus stage - mean(position) | encoder counts |
| **pressure**  | Atmospheric pressure at weather station - mean(pressure) | hPa |
| **ha** | Hour angle of telescope - mean(hour angle) | hours |
| **exptime** | Exposure time - mean(exposure time)| s |



##### summary\_{star}_{instrument}.csv
  - These files contain a summary printout from the ordinary least squares fit to all environmental/PSF parameters that showed Spearman rank correlation coefficients greater than 0.1
  - Look here to determine which parameters were included in the fit for a given star+instrument combination


##### vst{star}_{instrument}.dat
  - IDL save files containing at least the cf3 and cf5 tags
  - These are the default output files from the California Planet Search RV extraction pipeline
  - The cf3 tag contains the non-detrended velocities and the cf5 tag contains the detrended velocities
  - Please contact me if you need further explaination of the data contained within these IDL structures
