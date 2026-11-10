---
epistemic_grade: E3
---

# ISO 3166-2:ES Autonomous Communities, INE Provinces, Islands & Hydrographic Basins (`geo-es` — `E3`)

> **Epistemic Credibility Grade: `E3` (Canonical ISO 3166-2:ES, Eurostat NUTS, INE & Hydrographic Reference Table)**
>
> Primary lookup substrate for Spain's `17` Autonomous Communities, `2` Autonomous Cities, `50` Provinces (`INE 01..52`), `11` Insular Councils/Cabildos, fiscal regimes (`gov-es`), and official Water Framework Directive Hydrographic Basin Districts (`ES010..ES190`), implementing [01_territorial_organization_and_bioregional_model.md](../architecture/01_territorial_organization_and_bioregional_model.md).

---

## 1. Master Table of Autonomous Communities & Cities (`ISO 3166-2:ES`, `NUTS-2`, `INE` & Fiscal Regime) [E3]

> **Exon [E3]:** *Use the exact `ISO 3166-2:ES` code (`ES-AN`..`ES-VC`, `ES-CE`, `ES-ML`) and 2-digit `INE CPRO` (`01..52`) to determine fiscal jurisdiction (`IVA` vs. `Foral` vs. `IGIC` vs. `IPSI`), `UTM` projection zone, and bioregional classification ([01_territorial_organization_and_bioregional_model.md](../architecture/01_territorial_organization_and_bioregional_model.md)).*

Each Autonomous Community and Autonomous City is indexed below with its Eurostat `NUTS-2` code, `INE` provinces (`CPRO`), fiscal regime, `UTM` zone, and bioregion:

| `ISO 3166-2` | `NUTS-2` | Autonomous Community / City | Capital | `INE` Provinces (`CPRO` = Postal Prefix) | Fiscal Regime (`gov-es`) | Primary `UTM` & Bioregion |
| :--- | :---: | :--- | :--- | :--- | :--- | :--- |
| **`ES-AN`** | `ES61` | Andalucía | Sevilla | `04` Almería, `11` Cádiz, `14` Córdoba, `18` Granada, `21` Huelva, `23` Jaén, `29` Málaga, `41` Sevilla | Territorio Común (`IVA`) | `29N`/`30N` · Mediterranean (`Csa`, `BSk`) |
| **`ES-AR`** | `ES24` | Aragón | Zaragoza | `22` Huesca, `44` Teruel, `50` Zaragoza | Territorio Común (`IVA`) | `30N`/`31N` · Med. / Alpine (`BSk`, `Dfb`) |
| **`ES-AS`** | `ES12` | Principado de Asturias | Oviedo | `33` Asturias | Territorio Común (`IVA`) | `29N`/`30N` · Atlantic (`Cfb`) |
| **`ES-CB`** | `ES13` | Cantabria | Santander | `39` Cantabria | Territorio Común (`IVA`) | `30N` · Atlantic (`Cfb`) |
| **`ES-CL`** | `ES41` | Castilla y León | Valladolid *(sede inst.)* | `05` Ávila, `09` Burgos, `24` León, `34` Palencia, `37` Salamanca, `40` Segovia, `42` Soria, `47` Valladolid, `49` Zamora | Territorio Común (`IVA`) | `29N`/`30N` · Cont. Med. / Atl. (`Csb`, `BSk`) |
| **`ES-CM`** | `ES42` | Castilla-La Mancha | Toledo | `02` Albacete, `13` Ciudad Real, `16` Cuenca, `19` Guadalajara, `45` Toledo | Territorio Común (`IVA`) | `30N` · Cont. Mediterranean (`Csa`, `BSk`) |
| **`ES-CN`** | `ES70` | Canarias | Las Palmas / S.C. Tenerife | `35` Las Palmas, `38` Santa Cruz de Tenerife | **REF Canarias (`IGIC` / `AIEM` + `DUA`)** | `28N` (`REGCAN95`) · Macaronesian |
| **`ES-CT`** | `ES51` | Cataluña / Catalunya | Barcelona | `08` Barcelona, `17` Girona, `25` Lleida, `43` Tarragona | Territorio Común (`IVA`) | `31N` · Med. / Alpine (`Csa`, `Cfb`, `Dfb`) |
| **`ES-EX`** | `ES43` | Extremadura | Mérida | `06` Badajoz, `10` Cáceres | Territorio Común (`IVA`) | `29N`/`30N` · Mediterranean (`Csa`) |
| **`ES-GA`** | `ES11` | Galicia | Santiago de Compostela | `15` A Coruña, `27` Lugo, `32` Ourense, `36` Pontevedra | Territorio Común (`IVA`) | `29N` · Atlantic (`Cfb`, `Csb`) |
| **`ES-IB`** | `ES53` | Illes Balears | Palma | `07` Illes Balears | Territorio Común (`IVA`) | `31N` · Insular Mediterranean (`Csa`, `BSk`) |
| **`ES-MC`** | `ES62` | Región de Murcia | Murcia | `30` Murcia | Territorio Común (`IVA`) | `30N` · Semiarid Mediterranean (`BSh`, `BSk`) |
| **`ES-MD`** | `ES30` | Comunidad de Madrid | Madrid | `28` Madrid | Territorio Común (`IVA`) | `30N` · Cont. Mediterranean (`Csa`, `BSk`) |
| **`ES-NC`** | `ES22` | Comunidad Foral de Navarra | Pamplona / Iruña | `31` Navarra | **Régimen Foral (`Convenio` / `IVA Foral`)** | `30N` · Atl. / Med. / Alpine (`Cfb`, `Csa`) |
| **`ES-PV`** | `ES21` | País Vasco / Euskadi | Vitoria-Gasteiz *(sede)* | `01` Araba/Álava, `20` Gipuzkoa, `48` Bizkaia | **Régimen Foral (`Concierto` / `TicketBAI`)** | `30N` · Atlantic (`Cfb`) |
| **`ES-RI`** | `ES23` | La Rioja | Logroño | `26` La Rioja | Territorio Común (`IVA`) | `30N` · Mediterranean (`Csa`, `Cfb`) |
| **`ES-VC`** | `ES52` | Comunitat Valenciana | València | `03` Alicante/Alacant, `12` Castellón/Castelló, `46` Valencia/València | Territorio Común (`IVA`) | `30N`/`31N` · Mediterranean (`Csa`, `BSk`) |
| **`ES-CE`** | `ES63` | Ceuta *(Ciudad Autónoma)* | Ceuta | `51` Ceuta | **Régimen Especial (`IPSI` + `DUA`)** | `30N` · Mediterranean (`Csa`) |
| **`ES-ML`** | `ES64` | Melilla *(Ciudad Autónoma)* | Melilla | `52` Melilla | **Régimen Especial (`IPSI` + `DUA`)** | `30N` · Mediterranean (`BSk`) |

---

## 2. Insular `NUTS-3` Units: *Consells Insulars* (`ES-IB`) & *Cabildos Insulares* (`ES-CN`) [E3]

> **Exon [E3]:** *In `ES-IB` (`07`) and `ES-CN` (`35`, `38`), island-level statistical and administrative governance operates per island (`NUTS-3`) rather than solely at provincial level (`Art. 141.4 CE`).*

The `11` official island administrations and their Eurostat `NUTS-3` / `INE` insular codes are listed below:

| Archipelago (`CCAA`) | Parent Province (`CPRO`) | Island Administration (*Consell* / *Cabildo*) | `NUTS-3` Code | `INE` Island Code | Capital / Seat |
| :--- | :--- | :--- | :---: | :---: | :--- |
| **`ES-IB` (Illes Balears)** | `07` Illes Balears | Mallorca (`Consell Insular de Mallorca`) | `ES532` | `071` | Palma |
| **`ES-IB` (Illes Balears)** | `07` Illes Balears | Menorca (`Consell Insular de Menorca`) | `ES533` | `072` | Maó |
| **`ES-IB` (Illes Balears)** | `07` Illes Balears | Eivissa & Formentera (`Consells d'Eivissa i Formentera`) | `ES531` | `073` / `074` | Eivissa / Sant Francesc Xavier |
| **`ES-CN` (Canarias)** | `35` Las Palmas | Gran Canaria (`Cabildo de Gran Canaria`) | `ES705` | `351` | Las Palmas de Gran Canaria |
| **`ES-CN` (Canarias)** | `35` Las Palmas | Fuerteventura (`Cabildo de Fuerteventura`) | `ES704` | `352` | Puerto del Rosario |
| **`ES-CN` (Canarias)** | `35` Las Palmas | Lanzarote & La Graciosa (`Cabildo de Lanzarote`) | `ES708` | `353` | Arrecife |
| **`ES-CN` (Canarias)** | `38` S.C. de Tenerife | Tenerife (`Cabildo de Tenerife`) | `ES709` | `381` | Santa Cruz de Tenerife |
| **`ES-CN` (Canarias)** | `38` S.C. de Tenerife | La Palma (`Cabildo de La Palma`) | `ES707` | `382` | Santa Cruz de La Palma |
| **`ES-CN` (Canarias)** | `38` S.C. de Tenerife | La Gomera (`Cabildo de La Gomera`) | `ES706` | `383` | San Sebastián de La Gomera |
| **`ES-CN` (Canarias)** | `38` S.C. de Tenerife | El Hierro (`Cabildo de El Hierro`) | `ES703` | `384` | Valverde |

---

## 3. Official Hydrographic Basin Districts (`Demarcaciones Hidrográficas`, `RD 125/2007` & `DMA 2000/60/EC`) [E3]

> **Exon [E3]:** *Water concessions, industrial discharge permits (`Autorización de Vertido`, `RDLeg 1/2001 TRLA`), and flood-zone constraints follow hydrographic watershed boundaries (`Confederaciones Hidrográficas` for inter-community rivers vs. Autonomous Water Agencies for intra-community basins).*

The table below indexes Spain's major inter-community and intra-community River Basin Districts (`Demarcaciones Hidrográficas`):

| EU Basin District ID | Hydrographic Basin District (`Demarcación`) | Drainage Slope | Competent Authority (`Art. 149.1.22ª CE`) | Principal `CCAA` Traversed |
| :---: | :--- | :--- | :--- | :--- |
| **`ES010`** | **Miño-Sil** | Atlantic | *Confederación Hidrográfica del Miño-Sil (`MITECO`)* | `ES-GA`, `ES-CL`, `ES-AS` |
| **`ES014`** | **Galicia-Costa** | Atlantic | *Augas de Galicia (`ES-GA` — Intra-community)* | `ES-GA` |
| **`ES018` / `ES017`** | **Cantábrico Occidental & Oriental** | Cantabrian / Atl. | *CH del Cantábrico (`MITECO`)* & *URA (`ES-PV`)* | `ES-AS`, `ES-CB`, `ES-PV`, `ES-NC`, `ES-CL` |
| **`ES020`** | **Duero** *(Transboundary ES-PT)* | Atlantic | *Confederación Hidrográfica del Duero (`MITECO`)* | `ES-CL`, `ES-GA`, `ES-EX`, `ES-MD`, `ES-CM` |
| **`ES030`** | **Tajo** *(Transboundary ES-PT)* | Atlantic | *Confederación Hidrográfica del Tajo (`MITECO`)* | `ES-MD`, `ES-CM`, `ES-EX`, `ES-AR`, `ES-CL` |
| **`ES040`** | **Guadiana** *(Transboundary ES-PT)* | Atlantic | *Confederación Hidrográfica del Guadiana (`MITECO`)* | `ES-EX`, `ES-CM`, `ES-AN` |
| **`ES050`** | **Guadalquivir** | Atlantic | *Confederación Hidrográfica del Guadalquivir (`MITECO`)* | `ES-AN`, `ES-CM`, `ES-EX`, `ES-MC` |
| **`ES060` / `ES063` / `ES064`** | **Cuencas Mediterráneas Andaluzas, Guadalete-Barbate & Tinto-Odiel-Piedras** | Med. / Atlantic | *Administración Hidráulica de Andalucía (`ES-AN`)* | `ES-AN` |
| **`ES070`** | **Segura** | Mediterranean | *Confederación Hidrográfica del Segura (`MITECO`)* | `ES-MC`, `ES-VC`, `ES-CM`, `ES-AN` |
| **`ES080`** | **Júcar** | Mediterranean | *Confederación Hidrográfica del Júcar (`MITECO`)* | `ES-VC`, `ES-CM`, `ES-AR`, `ES-CT` |
| **`ES091`** | **Ebro** | Mediterranean | *Confederación Hidrográfica del Ebro (`MITECO`)* | `ES-AR`, `ES-CT`, `ES-NC`, `ES-RI`, `ES-PV`, `ES-CL`, `ES-CB`, `ES-CM`, `ES-VC` |
| **`ES100`** | **Cuencas Internas de Cataluña** | Mediterranean | *Agència Catalana de l'Aigua (`ACA`, `ES-CT`)* | `ES-CT` |
| **`ES110` & `ES120..127`** | **Illes Balears (`ES110`) & Insular Basins of Canarias (`ES120..127`)** | Insular | *Govern Illes Balears* & *Consejos Insulares de Aguas (`ES-CN`)* | `ES-IB`, `ES-CN` |
