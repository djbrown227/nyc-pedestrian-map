# NYC Pedestrian Network Explorer

An interactive geospatial visualization of estimated pedestrian flows across New York City’s street and sidewalk network, based on the NYC Pedestrian Network Estimates (2018–2019) dataset.

The project visualizes modeled pedestrian movement across time of day, day type, and trip purpose using a high-resolution representation of NYC’s walkable network.

---

## Dataset

**File:**  
NYC_pednetwork_estimates_counts_2018-2019.geojson

This dataset represents a citywide pedestrian network of sidewalk and crosswalk segments in New York City, enriched with estimated and observed pedestrian volumes.

### Citation

Sevtsuk, A., Basu, R., Liu, L., Kollar, J. (2025).  
Spatial Distribution of Foot-traffic in New York City and Applications for Urban Planning.  
Nature Cities (2025)

---

## Data Provenance

Prepared by the MIT City Form Lab, based on the NYC LION planimetric sidewalk layer [57].

The original dataset included sidewalks and crosswalks across NYC but:

- lacked park pathways  
- contained geometric and topological errors  
- was not suitable for routing or network analysis in its raw form  

### Processing

The dataset was processed through:

- Automated network cleaning  
- Manual correction and validation  
- Verification against 2019 aerial imagery in ArcGIS  
- Citywide quality control of connectivity and geometry  

---

## Coordinate Reference System

- EPSG: 6538  
- NAD 1983 (2011) StatePlane New York Long Island FIPS 3104 (Meters)

All spatial computations are performed in a projected coordinate system using meters.

---

## Data Structure

Each network segment includes the following attributes:

### Predicted pedestrian volumes (time-based)

- predwkdyAM – Weekday 8–9 AM  
- predwkdyMD – Weekday 12:30–1:30 PM  
- predwkdyPM – Weekday 5–6 PM  
- predwkndAM – Weekend 8–9 AM  
- predwkndMD – Weekend 12:30–1:30 PM  
- predwkndPM – Weekend 5–6 PM  

### Trip-purpose flows (uncalibrated estimates)

- HME_* – Home-based trips (school, work, parks, amenities, subway)  
- JOB_* – Work-based trips  
- AMN_* – Amenity-based trips  

These represent modeled flow patterns rather than fully calibrated absolute counts.

### Observed calibration counts

- Wkdy_*_CT – observed weekday counts  
- Wknd_*_CT – observed weekend counts  
- CountLoc – weekday calibration availability flag  
- CntLocWKND – weekend calibration availability flag  

---

## Notes

- Trip-purpose variables are uncalibrated estimates  
- Absolute values may not match real pedestrian counts  
- Spatial variation is the primary analytical signal  
- The dataset is not intended for routing or navigation  

---

## Contact

Andres Sevtsuk  
MIT City Form Lab  
asevtsuk@mit.edu  

---

## Dataset Version

Latest modification date: September 14, 2025  

---

## Project Context

This visualization supports exploratory analysis of:

- Fine-grained pedestrian movement in NYC  
- Temporal variation in foot traffic  
- Trip-purpose based flows across the network  
- Spatial distribution of pedestrian intensity  

It is designed as an interactive analytical tool rather than a static map.
