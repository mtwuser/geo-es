# Territorial Logistics, Fiscal Zoning & Bioregional Sourcing Guide (`M1 -> M4` — `geo-es` `E1`)

> **Epistemic Credibility Grade: `E1` (Adaptive `M1..M4` Territorial & Supply-Chain Guide)**
>
> Practical guide showing how operational layers (`dept-iso-finance`, `dept-iso-bio`, `dept-iso-legal`) combine `geo-es` with `gov-es` and `sci-biology`.

---

## 1. Cross-Layer Application Scenarios (`geo-es <-> gov-es <-> sci-biology`)

1. **Supply-Chain & Invoicing Validation (`dept-iso-finance`)**:
   - Look up the supplier or customer `CPRO` (`01..52`) in `01_iso_3166_2_es_autonomous_communities_and_provinces.md`.
   - Automatically route invoicing rules to mainland `IVA` (`ES-MD`, `ES-CT`, `ES-AN`, etc.), Foral *TicketBAI* (`ES-PV` `01/20/48`, `ES-NC` `31`), or Canary Islands `IGIC`/DUA (`ES-CN` `35/38`).
2. **Bioregional Non-Invasive Biomass Sourcing (`dept-iso-bio` + `sci-biology`)**:
   - Match the harvesting province's Biogeographical Region (`Mediterranean` vs. `Atlantic` in `01_territorial_organization_and_bioregional_model.md`) against authorized native agro-forestry species (`Olea europaea`, `Quercus ilex`, `Vitis vinifera`, `Pinus`) to guarantee compliance with `BIO-04` and `MITECO` `RD 630/2013`.
3. **Querying & Citing `geo-es`**:
   - Run `make consult LAYER=geo-es QUERY="ES-PV"` or `QUERY="Mediterranean"` and attach the returned `citation_receipt` to your BOM or batch record (`Record #NNN`).
