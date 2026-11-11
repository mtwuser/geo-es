# geo-es — Sovereign Epistemic Knowledge Corpus (`v1.0.0`)

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](VERSION)
[![ZeroCloudGravity](https://img.shields.io/badge/ZeroCloudGravity-v1.0.0-0F766E.svg)](https://github.com/mtwuser/zero-cloud-gravity)
[![Epistemic Grade](https://img.shields.io/badge/epistemic_grade-E3..E1-1D4ED8.svg)](docs/README.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

> **Spain Territorial Organization (`ISO 3166-2:ES`), Autonomous Communities & Bioregional Atlas** (`layer_role: knowledge`, `precedence: 20`, `stewardship_stage: public-community`).

## 1. Epistemic Corpus Index (`1:1:1` Progressive Disclosure)

All sections expose deterministic `rcap1` (`L0 -> L3`) capsules and cryptographic `citation_receipt` anchors (`<layer>::<file>#<slug>@<sha256_16>:<E3..E0>`):

| Tier | Credibility | Document |
| :--- | :--- | :--- |
| **Index** | `E2` | [`docs/README.md`](docs/README.md) |
| **Guide (`M1 -> M4`)** | `E1` | [Territorial Logistics, Fiscal Zoning & Bioregional Sourcing Guide (`M1 -> M4` — `E1`)](docs/guides/01_territorial_logistics_and_bioregional_sourcing_guide.md) |
| **Architecture & Taxonomy** | `E3` | [Spanish Territorial Organization, Geodetic Reference & Bioregional Architecture (`E3`)](docs/architecture/01_territorial_organization_and_bioregional_model.md) |
| **Primary Reference** | `E3/E2` | [ISO 3166-2:ES Autonomous Communities, INE Provinces & Hydrographic Basins (`E3`)](docs/reference/01_iso_3166_2_es_autonomous_communities_and_provinces.md) |

## 2. Mounting & Querying from Any `ZeroCloudGravity` Node

Link or mount this corpus into a personal (`<persona>-pc`, `<persona>-tutor`), research, or enterprise node without cloud dependencies:

```bash
zcg link <your-node-dir> --target https://github.com/mtwuser/geo-es.git --relation knowledge-feed
zcg consult-layer <your-node-dir> --layer geo-es --query "<topic>" --tier flash
```

## 3. Layer Setup Blueprint (`State U2: configured`)

- **Node ID & Role**: `geo-es` (`knowledge`, `precedence: 20`, `surface_veracity_mode: full-open-source`)
- **1-Hop Upstream Engine**: [`mtwuser/zero-cloud-gravity`](https://github.com/mtwuser/zero-cloud-gravity)
- **Active Template Packs**: `science-base`, `scientific-methodology`, `geo-es`, `knowledge-stewardship-portal`
- **Mission, Scope & Core Invariants**: Empirical territorial and geodetic reference corpus (`E3..E1`) covering `ISO 3166-2:ES` Autonomous Communities, INE provinces, fiscal regimes, hydrographic basins, and bioregional logistics.
- **Downstream Topology**: Consumed read-only via `knowledge-feed` links or `layers/*` subtrees across academic, scientific, public-sector, and enterprise nodes.
- **Authorized Layer Steward**: `geo-es Knowledge Steward <mtwuser@users.noreply.github.com>`
