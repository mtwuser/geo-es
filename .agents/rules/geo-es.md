---
trigger: always_on
description: "Spanish Territorial ISO 3166-2:ES, INE Municipal Codes, Hydrographic Basins & Bioregional Grounding Rules (geo-es)"
---

# Spanish Territorial & Bioregional Corpus Rules (`geo-es`)

## Scope & Surface Target
- **Template Pack**: `templates/geo-es/` (`context-stack`).
- **Knowledge Domain**: `territorial-empirical` (`public:knowledge:territorial-empirical`, `E3..E1`).

## Normative Invariants (`GEO-ES-01..03`)

1. **`GEO-ES-01` (`ISO 3166-2:ES` & `INE` Territorial Code Precision)**:
   - Every Autonomous Community (`CCAA`), Province, or Municipality referenced in logistics, fiscal, or environmental ledgers must use its canonical `ISO 3166-2:ES` code (`ES-AN`..`ES-VC`) and 2-digit `INE` Provincial prefix (`01`..`52`).
2. **`GEO-ES-02` (`ETRS89` Geodetic Reference & Hydrographic/Bioclimatic Classification)**:
   - Geolocation coordinates in Spain must use `ETRS89` (`EPSG:4258` / `UTM` zones `28N–31N`, or `REGCAN95` in Canary Islands `ES-CN`) and classify sites by Hydrographic Confederation, Köppen-Geiger climate zone, and Rivas-Martínez bioclimatic belt.
3. **`GEO-ES-03` (Bioregional Sourcing & `gov-es` Fiscal-Territorial Alignment)**:
   - Cross-reference `geo-es` codes with `gov-es` when determining fiscal territory (*Territorio Común* vs. *Régimen Foral* `ES-PV`/`ES-NC` vs. *REF Canarias* `ES-CN`) and with `sci-biology` when verifying regional non-invasive flora (`Quercus`, `Olea`, `Vitis`, `Pinus`).

## Verification & Sign-Off Gates
- [ ] Verify zero drift via `zcg diff-project`.
- [ ] Confirm all territorial references use valid `ISO 3166-2:ES` and `INE` identifiers.
