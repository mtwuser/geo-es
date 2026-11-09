# Spanish Territorial Organization, Geodetic Reference & Bioregional Architecture (`geo-es` — `E3`)

> **Epistemic Credibility Grade: `E3` (Official Cartographic, Geodetic & Territorial Standard)**
>
> This architecture specification defines the 3-level territorial hierarchy of Spain (`CCAA -> Provincia -> Municipio`), official geodetic reference systems (`IGN` `RD 1071/2007`), and bioregional zoning used across `gov-es`, `dept-iso-finance`, and `dept-iso-bio`.

---

## 1. 3-Tier Territorial & Administrative Hierarchy (`Art. 137 CE` & `INE` — `E3`)

Spain's territorial organization maps deterministically onto three administrative and statistical levels (`NUTS-2`, `NUTS-3`, `LAU`):

| Territorial Tier | Total Units | Official Identifier Standard | Functional & Governance Role |
| :--- | :-: | :--- | :--- |
| **1. Autonomous Communities & Cities (`CCAA`)** | `17 + 2` | `ISO 3166-2:ES` (`ES-AN` .. `ES-VC`, `ES-CE`, `ES-ML`) & `NUTS-2` | Legislative & executive autonomy (`Estatutos de Autonomía`), environmental licensing, health, education, and fiscal regime differentiation (`Común`, `Foral`, `Canarias`). |
| **2. Provinces & Islands (`Provincias / Islas`)** | `50 + 11` | `INE CPRO` (`01` .. `52`) & `ISO 3166-2:ES` 1/2-letter provincial codes | Provincial Councils (*Diputaciones Provinciales*, *Cabildos Insulares*, *Consejos Insulares*), postal prefix (`CP 01xxx..52xxx`), and logistics hub routing. |
| **3. Municipalities (`Municipios`)** | `8,132` | 5-digit `INE CMUN` (`CPRO` `2` digits + `CMUN` `3` digits + `DC` `1` check digit) | Local government (*Ayuntamientos*), urban activity licensing, municipal waste collection (`Ley 7/2022`), and local property/economic taxes (`IBI`, `IAE`). |

---

## 2. Geodetic Reference Systems & Hydrographic / Bioregional Planes (`GEO-ES-02` — `E3`)

1. **Official Geodetic Reference (`RD 1071/2007`, `IGN`)**:
   - **Iberian Peninsula, Balearic Islands, Ceuta & Melilla**: **`ETRS89`** (*European Terrestrial Reference System 1989*, `EPSG:4258`), projected in `UTM` Zones `29N`, `30N`, and `31N`.
   - **Canary Islands (`ES-CN`)**: **`REGCAN95`** (`UTM` Zone `28N`).
   - **Altimetric Datum**: Mean sea level in **Alicante** (*Nivel Medio del Mar en Alicante — NMMA*) for peninsular Spain.
2. **4 Biogeographical Regions & Rivas-Martínez Bioclimatic Belts of Spain (`EU Habitats Directive 92/43/EEC` & `MITECO`)**:
   - **Mediterranean Region (`~75%` of territory)**: Characterized by summer drought (`Csa`/`Csb`/`BSk`) across Thermomediterranean, Mesomediterranean, Supramediterranean, and Oromediterranean bioclimatic belts; native agro-forestry biomass dominated by *Olea europaea* (olive), *Quercus ilex* (holm oak), *Quercus suber* (cork oak), *Vitis vinifera* (vine), and *Pinus halepensis/pinea*.
   - **Atlantic (Eurosiberian) Region (`ES-GA`, `ES-AS`, `ES-CB`, `ES-PV`, northern `ES-NC`/`ES-CL`)**: Humid temperate (`Cfb`) Colline and Montane bioclimatic belts; *Quercus robur*, *Fagus sylvatica*, *Castanea sativa*.
   - **Alpine Region (Pyrenees)**: High-mountain Subalpine and Alpine bioclimatic belts (`Dfb`/`ET`).
   - **Macaronesian Region (`ES-CN` Canary Islands)**: Subtropical volcanic archipelagos across Inframacaronesian to Supracanarian bioclimatic belts; *Laurisilva* and *Pinus canariensis*.
