# README — `final_FFP_table.csv`

Compiled catalogue of **free-floating planet (FFP) candidates** assembled for a TFM/thesis project.  
Each row corresponds to one candidate object. The table contains **296 entries** and **60 columns** covering astrometry, photometry, physical parameters, and detection metadata.

---

## Quick facts

| Property | Value |
|---|---|
| Total candidates | 296 |
| Robust | 131 |
| Probable | 92 |
| Tentative | 73 |
| Sky coverage | 18 star-forming regions + field |
| Dominant region | Upper Scorpius (165 objects, 56%) |
| Mass range at 3 Myr | 0.74 – 13.0 M_Jup |
| Mass range at 5 Myr | 0.17 – 16.7 M_Jup |
| Mass range at 10 Myr | 0.74 – 20.9 M_Jup |

---

## Column descriptions

### Identification

| Column | Description |
|---|---|
| `ID` | Object identifier (survey ID or common name) |
| `Other IDs` | Cross-matched names from other catalogues |
| `ref` | Bibliographic reference for this entry |
| `notes` | Free-text notes on membership, disk, peculiarities |

### Astrometry

| Column | Units | Description |
|---|---|---|
| `RAJ2000` | deg | Right ascension (J2000) |
| `DEJ2000` | deg | Declination (J2000) |
| `Distance (kpc)` | kpc | Individual distance (filled for ~11% of objects; others use region mean) |
| `parallax (mas)` | mas | Parallax (Gaia or literature; 3.7% fill) |
| `parallax_error (mas)` | mas | Parallax uncertainty |
| `pmRA (mas/yr)` | mas/yr | Proper motion in RA (cos δ corrected; 76% fill) |
| `pmDE (mas/yr)` | mas/yr | Proper motion in Dec (76% fill) |
| `pmra_error (mas/yr)` | mas/yr | pmRA uncertainty (9.8% fill) |
| `pmdec_error (mas/yr)` | mas/yr | pmDec uncertainty (9.8% fill) |

### Mass estimates

Masses are derived by comparing photometry to evolutionary model isochrones at three assumed ages. Objects with masses above 13 M_Jup at a given age are not classified as FFPs at that age.

| Column | Units | Description |
|---|---|---|
| `Mass3Myr (M_Jup)` | M_Jup | Inferred mass assuming age = 3 Myr (68% fill) |
| `AV3Myr` | mag | Extinction A_V used for the 3 Myr fit (57% fill) |
| `Mass5Myr (M_Jup)` | M_Jup | Inferred mass assuming age = 5 Myr (61% fill) |
| `AV5Myr` | mag | Extinction A_V used for the 5 Myr fit (60% fill) |
| `Mass10Myr (M_Jup)` | M_Jup | Inferred mass assuming age = 10 Myr (62% fill) |
| `AV10Myr` | mag | Extinction A_V used for the 10 Myr fit (57% fill) |
| `Model` | — | Evolutionary model used for mass derivation (`BHAC15`, `BT-Settl`, `COND`, or microlensing models `PSPL`/`ESPL`/`FSPL`) |

### Reliability classification

| Column | Values | Description |
|---|---|---|
| `FFP_class` | `robust`, `probable`, `tentative` | Confidence level of the FFP nature based on detection method, membership evidence, and available follow-up |

### Photometry

Magnitudes are in the AB or Vega system as defined by each survey. Empty cells mean no measurement is available for that band.

| Column | Instrument / Survey | Fill rate |
|---|---|---|
| `gmag`, `rmag`, `imag`, `zmag`, `ymag` | Pan-STARRS / SDSS optical | 3–64% |
| `umag` | SDSS u-band | 3% |
| `Mjmag` | MegaCam J | 3% |
| `Jmag`, `Hmag`, `Ksmag` | 2MASS / VISTA NIR | 84–87% |
| `F150Wmag`, `F200Wmag` | JWST/NIRCam | 2% |
| `W1mag`, `W2mag`, `W3mag` | WISE mid-IR | 2–7% |
| `[3.6]`, `[4.5]`, `[5.8]` | Spitzer/IRAC | <5% |

### Physical parameters

| Column | Units | Description |
|---|---|---|
| `Teff (K)` | K | Effective temperature from spectral fitting (20% fill) |
| `Radius (R_Jup)` | R_Jup | Object radius (10% fill) |
| `log g (cgs)` | dex | Surface gravity (9% fill) |
| `Spectral Type` | — | MK spectral type (33% fill; mostly M8–L8 and T/Y) |
| `v sin i (km s-1)` | km/s | Projected rotational velocity (1% fill) |

### Detection and membership

| Column | Description |
|---|---|
| `region` | Star-forming region or moving group (100% fill) |
| `detection_method` | How the candidate was identified (astrometry, direct imaging, spectroscopy, microlensing, photometry+pm+NIR spec) |
| `instrument` | Instrument(s) used for detection |
| `catalog` | Source survey catalogue (DANCe, VISTA/Spitzer/WISE, SONYC, OGLE-IV, CatWISE, etc.) |

### Microlensing parameters
Only filled for the 15 microlensing events (~5% of the catalogue).

| Column | Units | Description |
|---|---|---|
| `tE_days` | days | Einstein ring crossing time |
| `thetaE_muas` | µas | Angular Einstein radius |
| `mu_rel_masyr` | mas/yr | Relative lens–source proper motion |
| `u0` | — | Impact parameter |
| `rho` | — | Source radius normalised to Einstein radius |
| `Source_I0_mag` | mag | Unlensed source I-band magnitude |
| `Source_VI0` | mag | Unlensed source V−I colour |
| `Source_Teff_K` | K | Source effective temperature |
| `Surface_Gravity_GEarth` | g_Earth | Source surface gravity |

---

## Regions represented

| Region | N | Mean distance |
|---|---|---|
| Upper Scorpius | 165 | 145 pc |
| Orion | 36 | ~388 pc |
| Taurus | 19 | 140 pc |
| Chamaeleon I | 16 | 160 pc |
| Galactic bulge | 15 | ~8 kpc (microlensing) |
| NGC 1333 / Perseus | 14 | 300 pc |
| TW Hydrae | 8 | ~60 pc |
| AB Doradus | 4 | ~15 pc |
| Pleiades Cluster | 4 | 133 pc |
| Other / field | 15 | various |

---

## Key references

| Reference | Objects |
|---|---|
| Miret-Roig et al. (2022) | 165 — Upper Sco (DANCe astrometry) |
| Peña-Ramírez et al. (2012) | 17 — Orion (VISTA/Spitzer) |
| Bouy et al. (2025) | 15 — Galactic bulge (microlensing) |
| Esplin et al. (2017) | 14 — Chamaeleon I |
| Scholz et al. (2012) | 8 — NGC 1333 (SONYC) |
| Zapatero Osorio et al. (2000, 2017, 2018) | 12 — Orion / Pleiades |
| Bardalez Gagliuffi et al. (2020) | 5 — field (CatWISE / Backyard Worlds) |

---

## Notes on completeness

- **Photometry**: NIR bands (J, H, Ks) are the best-covered (~85%). Optical bands and mid-IR (Spitzer, WISE, JWST) are sparse.
- **Masses**: Only available for objects with a BHAC15/BT-Settl model fit (~62%). Microlensing events and some field objects lack mass estimates.
- **Distances**: Most objects use a single mean distance per region. Only ~11% have individual distance estimates.
- **Extinction**: The `AV` columns give the extinction used during mass fitting. For 3D line-of-sight extinction corrections use `mwdust Combined15` queried at (l, b, d_kpc).

---

## File format

- Encoding: UTF-8  
- Separator: comma  
- Missing values: empty cell (not `NaN` or `-99`)  
- Some mass columns contain string values for objects where the fit returned a non-numeric flag — use `pd.to_numeric(..., errors='coerce')` when loading.

```python
import pandas as pd
df = pd.read_csv('final_FFP_table.csv')
for col in ['Mass3Myr (M_Jup)', 'Mass5Myr (M_Jup)', 'Mass10Myr (M_Jup)']:
    df[col] = pd.to_numeric(df[col], errors='coerce')
```
