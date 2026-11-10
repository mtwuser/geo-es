---
epistemic_grade: E1
---

# Territorial Logistics, Fiscal Zoning & Bioregional Sourcing Guide (`M1 -> M4` — `geo-es` `E1`)

> **Epistemic Credibility Grade: `E1` (Adaptive `M1..M4` Territorial, GIS & Supply-Chain Guide)**
>
> This practical guide demonstrates how students, GIS analysts, and operational enterprise layers (`dept-iso-finance`, `dept-iso-bio`, `dept-iso-legal`) combine `geo-es` ([01_territorial_organization_and_bioregional_model.md](../architecture/01_territorial_organization_and_bioregional_model.md) and [01_iso_3166_2_es_autonomous_communities_and_provinces.md](../reference/01_iso_3166_2_es_autonomous_communities_and_provinces.md)) with `gov-es` and `sci-biology`.

---

## 1. Deterministic 3-Scenario Cross-Layer Workflows (`geo-es <-> gov-es <-> sci-biology`) [E1]

> **Summary [E1]:** *From a single 5-digit Spanish postal code (`PPNNN`) or `ISO 3166-2:ES` region, derive deterministically: (1) fiscal tax & e-invoicing regime, (2) `EPSG` geodetic coordinate system & river basin authority, and (3) EU biogeographical flora/biomass eligibility ([01_iso_3166_2_es_autonomous_communities_and_provinces.md](../reference/01_iso_3166_2_es_autonomous_communities_and_provinces.md)).*

Apply the three canonical resolution flows below across software, logistics, and environmental compliance workflows:

### 1.1. Scenario A — Automated Fiscal & Customs Routing from Postal Prefix (`CPRO 01..52`)

Given any Spanish counterparty postal code `PPNNN`, extract `CPRO = PP` and match against Section 1 of [01_iso_3166_2_es_autonomous_communities_and_provinces.md](../reference/01_iso_3166_2_es_autonomous_communities_and_provinces.md):
- **`CPRO` in `{01, 20, 48}` (`ES-PV`)**: Apply Basque *Concierto Económico* rules and **TicketBAI / Batuz** XML signature chaining when the issuer has Basque fiscal domicile.
- **`CPRO == 31` (`ES-NC`)**: Apply Navarrese *Convenio Económico* (`Hacienda Foral de Navarra`).
- **`CPRO` in `{35, 38}` (`ES-CN`)**: Treat physical shipments between mainland/Balears and Canarias as **extra-VAT customs exports/imports (`DUA`)** subject to **`IGIC`** (`7%` general) and `AIEM` (never mainland `IVA`).
- **`CPRO` in `{51, 52}` (`ES-CE`, `ES-ML`)**: Apply **`IPSI`** and customs `DUA` clearance.
- **All remaining `43` provinces (`15` Common-Territory `CCAA`)**: Apply standard `AEAT` `IVA` (`21% / 10% / 4%`) and `Veri*factu` / `SII` rules (`gov-es::AREA-01`).

### 1.2. Scenario B — GIS Coordinate Validation & Watershed Licensing (`ETRS89` vs. `REGCAN95`)

Before accepting parcel coordinates or industrial water permits in an engineering or cadastral pipeline:
1. Check `ISO 3166-2:ES` in [01_territorial_organization_and_bioregional_model.md](../architecture/01_territorial_organization_and_bioregional_model.md):
   - Reject legacy `ED50` (`EPSG:4230`) coordinates (`RD 1071/2007` cutover).
   - Enforce **`REGCAN95` / `UTM 28N` (`EPSG:4081` / `EPSG:4083`)** for `ES-CN` (`CPRO 35, 38`) and **`ETRS89` (`EPSG:4258` / `EPSG:25829..25831`)** for all peninsular, Balearic, Ceuta, and Melilla sites.
2. Intersect parcel coordinates with the Hydrographic Basin District (`ES010..ES127` in Section 3 of [01_iso_3166_2_es_autonomous_communities_and_provinces.md](../reference/01_iso_3166_2_es_autonomous_communities_and_provinces.md)) to route discharge permits to the competent *Confederación Hidrográfica* (`MITECO`) or Intra-Community Water Agency (`ACA`, `URA`, `Augas de Galicia`).

### 1.3. Scenario C — Bioregional Non-Invasive Biomass & Biodiversity Screening (`geo-es + sci-biology`)

When sourcing agro-forestry by-products (`Ley 7/2022 Art. 4`) or validating ecological restoration projects:
- Resolve the province's **Biogeographical Region** (`Mediterranean`, `Atlantic`, `Alpine`, or `Macaronesian`) and verify that candidate botanical species belong to the native indicator taxa for that belt and are absent from the *Catálogo Español de Especies Exóticas Invasoras* (`RD 630/2013`).

```bash
# Compact L1 lookup of Basque / Canary fiscal & territorial metadata
make consult LAYER=geo-es QUERY="ES-CN REGCAN95 IGIC"
```

---

## 2. Progressive `M1 -> M4` Consumer Adaptation Matrix [E1]

> **Summary [E1]:** *`geo-es` scales from school/university geography (`M1..M2`) to automated ERP/GIS software validation (`M3`) and multi-basin environmental/fiscal auditing (`M4`).*

The table below summarizes how different personas consume `geo-es` via `rcap1` capsules:

| Mastery Level | Target Persona | Recommended `geo-es` Surface & Resolution | Key Deliverable Enabled |
| :--- | :--- | :--- | :--- |
| **`M1`** | Primary / Secondary Geography & Social Science Student | `docs/guides/` + `CCAA` / Capital / Relief summary (`L1` / `L2`) | Masters Spain's `17 CCAA + 2 Autonomous Cities`, `50` provinces, insular archipelagos, and Atlantic vs. Mediterranean rivers. |
| **`M2`** | University Student (Geography, Environmental Science, Economics) | `NUTS-1..3` hierarchy + `4` Biogeographical Regions (`L2`) | Performs Eurostat `NUTS-2/3` statistical joins and Rivas-Martínez bioclimatic classification. |
| **`M3`** | Software / FinOps / Supply-Chain Engineer (`dept-iso-finance`, `dept-iso-eng`) | `CPRO 01..52` fiscal table + `EPSG` `UTM` meridian cut-points (`L2 -> L3`) | Implements deterministic `CPRO -> Tax Regime` (`IVA`/`TicketBAI`/`IGIC`/`IPSI`) and `EPSG` boundary validators (`100%` `AAA` unit tested). |
| **`M4`** | Environmental Director / Territorial Auditor (`dept-iso-bio`, `dept-iso-legal`) | Full `ES010..ES127` Hydrographic Districts + Insular `NUTS-3` + `citation_receipt` (`L3`) | Certifies multi-region `AAI` permits, watershed compliance, and bioregional origin traceability (`Record #NNN`). |
