---
epistemic_grade: E3
---

# Spanish Territorial Organization, Geodetic Reference & Bioregional Architecture (`geo-es` — `E3`)

> **Epistemic Credibility Grade: `E3` (Official Cartographic, Statistical, Geodetic & Territorial Standard)**
>
> This architecture specification defines the 4-level statistical and administrative hierarchy of Spain (`NUTS-1 -> CCAA NUTS-2 -> Provincia/Isla NUTS-3 -> Municipio LAU`), official geodetic reference systems (`IGN` `RD 1071/2007`), and EU/Rivas-Martínez bioregional zoning used across `gov-es`, `dept-iso-finance`, and `dept-iso-bio` ([01_iso_3166_2_es_autonomous_communities_and_provinces.md](../reference/01_iso_3166_2_es_autonomous_communities_and_provinces.md)).

---

## 1. 4-Tier Territorial, Administrative & Eurostat `NUTS` Hierarchy (`Art. 137 CE`, `INE` & `Eurostat`) [E3]

> **Summary [E3]:** *Spain's territory maps deterministically onto `7` `NUTS-1` macro-regions, `17` Autonomous Communities + `2` Autonomous Cities (`ISO 3166-2:ES`, `NUTS-2`), `50` Provinces + `11` Island units (`INE CPRO 01..52`, `NUTS-3`), and `8,132` Municipalities (`LAU`, 5-digit `INE` code) ([01_iso_3166_2_es_autonomous_communities_and_provinces.md](../reference/01_iso_3166_2_es_autonomous_communities_and_provinces.md)).*

The table below defines the official statistical and constitutional hierarchy governing territorial identification in Spain:

| Territorial Tier | Total Units | Official Standard & Code Format | Constitutional, Statistical & Operational Role |
| :--- | :-: | :--- | :--- |
| **0. Macro-Regions (`NUTS-1`)** | `7` | Eurostat `ES1`..`ES7` (`Noroeste`, `Noreste`, `Com. Madrid`, `Centro`, `Este`, `Sur`, `Canarias`) | European regional cohesion funding (`FEDER`/`FSE+`), macro-climatic corridors, and national transport/grid planning. |
| **1. Autonomous Communities & Cities (`CCAA` — `NUTS-2`)** | `17 + 2` | `ISO 3166-2:ES` (`ES-AN`..`ES-VC`, `ES-CE`, `ES-ML`) & `INE CCAA` (`01`..`19`) | Legislative & executive autonomy (`Art. 143–158 CE`), environmental `AAI` permits, health, education, and fiscal regime (`Común`, `Foral`, `REF Canarias`, `IPSI`). |
| **2. Provinces & Islands (`Provincias / Islas` — `NUTS-3`)** | `50 + 11` | `INE CPRO` (`01`..`52`), `ISO 3166-2:ES` provincial codes, & `INE` Island codes | *Diputaciones Provinciales* (`Art. 141 CE`), *Cabildos Insulares* (`ES-CN` `7` islands), *Consells Insulars* (`ES-IB` `4` islands), and postal prefix (`CP 01xxx..52xxx`). |
| **3. Municipalities (`Municipios` — `LAU`)** | `8,132` | `5`-digit `INE` code (`CPRO` `2` digits + `CMUN` `3` digits) + `1` check digit (`DC`) | Local government (*Ayuntamientos*, `Art. 140 CE` & `Ley 7/1985 LRBRL`), urban planning (`PGOU`), activity licenses, municipal waste (`Ley 7/2022`), and local taxes (`IBI`, `IAE`, `ICIO`). |

### 1.1. Structure of the `INE` Municipal Code & Postal Prefix Invariant (`CPRO 01..52`)

Every Spanish municipality and postal address obeys two strict structural invariants:
1. **Postal Code Prefix (`Código Postal`, `5` digits `PPNNN`)**: The leading two digits `PP` (`01` through `52`) are **strictly identical** to the official `INE` Province Code (`CPRO`), ordered historically by alphabetical Spanish province name from `01` (*Araba/Álava*) to `50` (*Zaragoza*), followed by `51` (*Ceuta*) and `52` (*Melilla*).
2. **Official `INE` Municipal Identifier (`6` digits `PPMMM-D`)**: Concatenates the `2`-digit province code (`PP`), the `3`-digit sequential municipality code within that province (`MMM`), and a `1`-digit control check digit (`D`) published in the *Relación de Municipios y Códigos por Provincias* (`INE`).

---

## 2. Geodetic Reference Systems, `UTM` Meridian Cut-Points & Altimetric Datums (`RD 1071/2007`) [E3]

> **Summary [E3]:** *Under `Real Decreto 1071/2007` (`BOE-A-2007-15822`), all official cartography, GIS coordinates, and environmental/cadastral filings in Spain must use **`ETRS89`** (`EPSG:4258`) on the Iberian Peninsula, Balearic Islands, Ceuta, and Melilla, and **`REGCAN95`** (`EPSG:4081`) in the Canary Islands.*

Spatial coordinates, parcel boundaries (*Catastro*), and watershed models must respect the exact geodetic and `UTM` zone cut-points below:

| Geographic Scope | Official Geodetic System (`GRS80` Ellipsoid) | Geodetic `EPSG` | Projected `UTM` Zones & Exact Meridian Cut-Points (`N` vs. `N ± 1`) | Official Vertical / Altimetric Datum |
| :--- | :--- | :---: | :--- | :--- |
| **Western Iberia (`ES-GA`, western `ES-EX`/`ES-CL`/`ES-AN`)** | **`ETRS89`** | `EPSG:4258` | **`UTM Zone 29N`** (`EPSG:25829`): Longitude $\lambda \in [-12^\circ\text{W}, -6^\circ\text{W})$ (central meridian $9^\circ\text{W}$). | **NMMA** (*Nivel Medio del Mar en Alicante*, mainland) |
| **Central Iberia, Ceuta (`ES-CE`) & Melilla (`ES-ML`)** | **`ETRS89`** | `EPSG:4258` | **`UTM Zone 30N`** (`EPSG:25830`): Longitude $\lambda \in [-6^\circ\text{W}, 0^\circ)$ (central meridian $3^\circ\text{W}$; national mosaic default). | **NMMA** (mainland) / Local tide gauge (`Ceuta`, `Melilla`) |
| **Eastern Iberia (`ES-CT`, eastern `ES-AR`/`ES-VC`) & `ES-IB`** | **`ETRS89`** | `EPSG:4258` | **`UTM Zone 31N`** (`EPSG:25831`): Longitude $\lambda \in [0^\circ, +6^\circ\text{E}]$ (central meridian $3^\circ\text{E}$). | **NMMA** (mainland) / Local insular datum (`Mallorca`, `Menorca`, `Ibiza`) |
| **Canary Islands Archipelago (`ES-CN`)** | **`REGCAN95`** *(ITRF93 epoch 1994.8, compatible with WGS84/ETRS89)* | `EPSG:4081` | **`UTM Zone 28N`** (`EPSG:4083`): Longitude $\lambda \in [-18^\circ\text{W}, -12^\circ\text{W})$ *(El Hierro at $\sim 18^\circ 09'\text{W}$ extended into `28N` without zone split)*. | Individual island tide-gauge datums (`Tenerife`, `Gran Canaria`, `Lanzarote`, `Fuerteventura`, `La Palma`, `La Gomera`, `El Hierro`) |

---

## 3. Biogeographical Regions & Rivas-Martínez Bioclimatic Belts (`EU 92/43/EEC` & `MITECO`) [E3]

> **Summary [E3]:** *Spain is the only EU Member State spanning four Biogeographical Regions (`Mediterranean`, `Atlantic`, `Alpine`, `Macaronesian`), governing native species eligibility (`RD 630/2013`), agro-forestry biomass sourcing, and `Natura 2000` conservation gates.*

 Ecological, agricultural, and circular-economy operations classify every Spanish site across the four official EU Biogeographical Regions ([01_territorial_logistics_and_bioregional_sourcing_guide.md](../guides/01_territorial_logistics_and_bioregional_sourcing_guide.md)):

1. **Mediterranean Biogeographical Region (`~75%` of national area)**:
   - **Climate & Thermicity (`Rivas-Martínez`)**: Summer drought regime ($P_{s2} < 2 T_{s2}$, Köppen `Csa`, `Csb`, `BSk`, `BSh`) spanning Infra-, Thermo-, Meso-, Supra-, Oro-, and Cryoromediterranean belts.
   - **Indicator Native Taxa & Agro-Forestry Substrates**: *Quercus ilex* subsp. *ballota* (holm oak / *dehesa*), *Quercus suber* (cork oak), *Olea europaea* (olive), *Vitis vinifera* (vine), *Prunus dulcis* (almond), *Pinus halepensis*, and *Pinus pinea*.
2. **Atlantic (Eurosiberian) Biogeographical Region (`ES-GA`, `ES-AS`, `ES-CB`, `ES-PV`, northern `ES-NC` & northern `ES-CL`)**:
   - **Climate & Thermicity**: Oceanically tempered humid regime without summer drought (`Cfb`) across Thermocolline, Colline, and Montane belts.
   - **Indicator Native Taxa**: *Quercus robur*, *Quercus petraea*, *Fagus sylvatica* (beech), *Castanea sativa* (chestnut), and *Betula celtiberica*.
3. **Alpine Biogeographical Region (Pyrenees across northern `ES-HU`, `ES-L`, `ES-GI`, `ES-NA`)**:
   - **Climate & Thermicity**: High-altitude Subalpine (`1,600–2,300 m`) and Alpine (`> 2,300 m`) belts (`Dfb`, `Dfc`, `ET`).
   - **Indicator Native Taxa**: *Pinus uncinata*, *Abies alba*, *Rhododendron ferrugineum*, and alpine *Festuca* grasslands.
4. **Macaronesian Biogeographical Region (`ES-CN` Canary Islands)**:
   - **Climate & Thermicity**: Subtropical trade-wind (*alisios*) altitudinal zonation (`BWh` coastal xerophytic $\rightarrow$ `Csb` cloud-forest *mar de nubes* $\rightarrow$ high volcanic summit).
   - **Indicator Native Taxa**: *Euphorbia balsamifera/canariensis* (*cardonal-tabaibal*), Tertiary relic *Laurisilva* (*Laurus novocanariensis*, *Myrica faya*), *Pinus canariensis*, and subalpine *Spartocytisus supranubius*.
