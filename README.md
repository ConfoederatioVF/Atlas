# Atlas

<div align = "center">
<img src = "https://i.postimg.cc/3ND2B1zL/crd-coat-of-arms-logo.png" height = "64">
<br><br>
<img src = "https://i.postimg.cc/tyxHQzXB/84-atlas.png" width = "100%">
<br><br>
<div align = "center">Figure 1. Atlas de facto as presented in Confoederatio Dataview for the Holy Roman Empire (10 January 1356AD).</div>
<br>
 
[![Join our community (Element Matrix)!](https://img.shields.io/badge/chat-on%20matrix-51bb9c?style=for-the-badge)](https://matrix.to/#/#confoederatio:matrix.confoederatio.org) [![Join our community!](https://img.shields.io/discord/548994743925997570?label=Discord&style=for-the-badge)](https://discord.gg/89kQY2KFQz) ![](https://img.shields.io/github/languages/code-size/ConfoederatioVF/Eoscala?style=for-the-badge)

</div>

## Abstract.

> [!NOTE]
> **Atlas de facto** is currently a naive geospatialisation of all Wikipedia corpus text and maps with limited manual edits. Therefore, it inherits the same errors that Wikipedia does. We are actively working to address these problems.

- E-mail: [vf@confoederatio.org](mailto:vf@confoederatio.org)
- Dataview: https://dataview.confoederatio.org/
- <ins>Download:</ins>
- - Stadestér (Cities, part of Velkscala) | [Github](https://github.com/ConfoederatioVF/Stadester) | [Projects (1.1)](https://projects.confoederatio.org/c/Stadester)
- - Velkscala (Demographics) | [Github](https://github.com/ConfoederatioVF/Velkscala) | [Datavault (1.0)](https://datavault.confoederatio.org/s/44Pfgt7ya8wE77b)
- - Eoscala (Economics) | [Github](https://github.com/ConfoederatioVF/Eoscala) | [Datavault (1.5)](https://datavault.confoederatio.org/s/2Kytdej7ABpw4rr)
- - **Atlas (Polities)** | [Github](https://github.com/ConfoederatioVF/Atlas) | [Datavault (0.7)](https://datavault.confoederatio.org/s/rPntqXwCxzXg4Bk)
- View legacy Atlas data (<0.7b): https://confoederatio.org/pages/atlas

Atlas is a geospatial dataset comprised of both *de jure* and *de facto* border changes, from 3500BC-2025AD. *De facto* changes are tracked at daily resolution, and *de jure* changes are tracked at yearly resolution.

*De jure* borders can be confusing prior to the emergence of the international system, and so we define it as a composite of three academic databases: [Seshat](https://seshat-db.com/) (<1815AD), [Correlates of War](https://correlatesofwar.org/) (1815AD-1886AD) and [C-Shapes 2.0](https://icr.ethz.ch/data/cshapes/) (1886AD-Present). For consistency purposes, we provide cumulative IDs for each dataset over their entire domain, such that countries after 1815AD have both COW IDs as well as Seshat IDs, and countries after 1886AD have additional Gleditsch and War IDs. 

See **Atlas (de jure)** for more information.

### What is a `.naissance` file?

Because `.geojson` does not natively allow for moving geometries, **Atlas 0.7** utilises `.naissance` files, which are an extended form of GeoJSON that allow for diffs per geometry, also known as *keyframes*. Each geometry has a set of keyframes, in which timestamps are measured in minutes from 00:00GMT, 1 January 1AD as a JavaScript `number`.

We recommend using either [Naissance GIS](https://projects.confoederatio.org/c/Naissance) or [Confoederatio Dataview](https://dataview.confoederatio.org) for editing and viewing `.naissance` files respectively.

## Atlas (de facto)

The main `.naissance` file for de facto boundaries can be found in `/defacto/atlas_defacto.naissance`.

## Data Structure.

`.control_type`:

'Administration', 'Ally', 'Associate', 'Autonomous Region', 'Bantustan', 'Client', 'Colony', 'Company Rule', 'Concession', 'Condominium', 'Constituent County', 'Crown Dependency', 'De Facto Control', 'Dependency', 'Dependent Territory', 'Directorate', 'Dominion', 'External Territory', 'Fief', 'Foederatus', 'Governorate', 'Influence', 'Lease', 'Mandate', 'Military Base', 'Military Occupation', 'Nominal Colony', 'Nominal Possession', 'Nominal Vassal', 'Overseas Collectivity', 'Overseas Department', 'Overseas Province', 'Overseas Territory', 'Personal Union', 'Possession', 'Princely State', 'Protectorate', 'Puppet State', 'Satellite', 'Self-Governing Colony', 'Semi-Autonomous Region', 'Semi-Independent Circuit', 'Special Administrative Region', 'Special Municipality', 'Territory', 'Trading Post', 'Tributary', 'Unincorporated Territory', 'Vassal', 'Viceroyalty'

`.description`: string

`.id`: string - Isomorphic to `.state_id`, assigned Naissance ID.

`.label`: string

<details>
<summary>Expand `.label` values (157)</summary>
  
- akan states
- albanian principalities
- albanian principalities;serbian principalities
- american confederate secessionist states
- anatolian beyliks
- ancient estonian counties
- anglian polities in britain
- antique greek leagues
- arab polities of east congo
- aramean polities
- argentinian juntas;juntas
- baltic states
- baltic states;separatists (russian civil war)
- bantustans
- barangay states
- barbarian kingdoms
- barbarian kingdoms;frankish polities
- berber kingdoms
- boer states
- bolsheviks (russian civil war)
- british colonies in australia
- bronze age levant city-states
- byzantine fragmentation
- byzantine successors in southern italy
- byzantine successors in southern italy;maritime republics
- catalan counties
- caucasian khanates
- caucasian khanates;kurdish principalities
- celtic polities
- celtic polities in britain;celtic polities
- celtic polities in britain;welsh polities;celtic polities
- celtic polities of brittany;celtic polities
- christian kingdoms of nubia
- civil war of the constantinian dynasty
- civil wars of the tetrarchy
- comoros sultanates;polities of the swahili coast
- concessions in china
- confederation of the rhine;german confederation
- crisis of the third century
- crusader states
- crusader states;holy roman empire
- cyprus petty kingdoms
- cyprus petty kingdoms;greek poleis
- cyprus petty kingdoms;phoenician polities (outside phoenicia)
- dalmatian city-states
- deccan sultanates
- diadochi
- easter island polities
- eighteen kingdoms
- english chieftancies in sierra leone
- etruscan polities;pre-roman confederations in italy
- european enclaves in north africa before 1830
- five dynasties and ten kingdoms - five dynasties (chinese history)
- five dynasties and ten kingdoms - other countries  (chinese history)
- five dynasties and ten kingdoms - ten kingdoms  (chinese history)
- four great native chiefdoms in guizhou
- fragmentation of bali
- fragmentation of the odrysian kingdom
- frankokratia
- fula jihads polities
- fula jihads polities;hausa states
- german confederation
- greco-bactrian polities
- greek poleis
- griqua states
- guanche states
- hausa states
- hausa states;fula jihads polities
- hausa states;tuareg polities;berber kingdoms
- herodian tetrarchy
- holy roman empire
- holy roman empire;confederation of the rhine
- holy roman empire;confederation of the rhine;german confederation
- holy roman empire;german confederation
- indian princely states
- indus valley civilization city-states
- iranian intermezzo
- irish medieval kingdoms;celtic polities
- irish medieval kingdoms;norse/viking polities
- juntas
- kingdoms in the gibe region
- kongsi republic
- kurdish principalities
- kurdish principalities;iranian intermezzo
- latgalian elderships
- lombard polities
- lombard polities;barbarian kingdoms
- lower egypt nomi
- luwian-aramean polities;aramean polities
- mahajanapadas
- maritime republics
- maritime republics;byzantine successors in southern italy
- maritime republics;holy roman empire
- mesoamerican polities
- mesopotamian city-states
- modern kurdish polities
- mon kingdoms
- mycenean greece
- napoleonic polities;french revolutionary states
- napoleonic polities;french revolutionary states;confederation of the rhine
- napoleonic polities;french revolutionary states;confederation of the rhine;german confederation
- napoleonic polities;french revolutionary states;holy roman empire
- napoleonic polities;french revolutionary states;holy roman empire;confederation of the rhine
- nepal petty kingdoms
- norse/viking polities
- norse/viking polities;celtic polities
- norse/viking polities;norman polities in southern italy
- northern and southern dynasties (chinese history)
- norwegian petty kingdoms
- ottoman interregnum
- ovimbundu kingdoms
- persia after the disintegration of the ilkhanate
- phoenician polities;phoenician polities (outside phoenicia)
- phoenician polities;phoenician polities (phoenicia)
- polish polities after the congress of vienna
- polities of the swahili coast
- pre-roman confederations in italy
- pyu city-states
- roman-maurian kingdoms;berber kingdoms
- russian principalities
- ryuku polities
- sardinian judicates
- saxon polities in britain
- second intermediate period of egypt
- seleucid secessionist states
- seleucid secessionist states;greco-bactrian polities
- separatists (russian civil war)
- serbian principalities
- shan states
- sicilian taifas
- sister republic;french revolutionary states
- sister republic;french revolutionary states;holy roman empire
- sixteen kingdoms (chinese history)
- small arab emirates in europe
- southern arabia petty kingdoms
- soviet republics in germany after world war i
- spanish taifas
- spring and autumn and warring states periods
- states emerged from the northern crusades
- states emerged from the northern crusades;holy roman empire
- successors of the mongol empire
- tarim basin
- third intermediate period of egypt
- thirteen colonies
- three kingdoms (chinese history)
- tibetan era of fragmentation
- tuareg polities
- unfederated malay states
- upper egypt nomi
- us colonies in liberia
- warsaw pact
- whites (russian civil war)
- year of the five emperors
- yoruba kingdoms
- yugra principalities
- yugra principalities;russian principalities

</details>
  
`.link`: string - The Wikipedia link for the given polity.

`.name`: string - The name of the polity.

`.parent`: string | Optional

`.state_id`: string

Capital city information for `atlas_detailed.naissance` is available via [Stadestér](https://datavault.confoederatio.org/s/emwGKmWNCtmcgmp)’s `city_metadata.json`, which contains both the historical names of individual cities, as well as capital city histories.

If you would prefer viewing capital cities tied directly to polity `.state_id` as opposed to individual cities, see the `/capital_cities/` folder within Stadestér. Details on usage are included with [Stadestér’s README](https://datavault.confoederatio.org/s/QcXSrmcA7qYSmR6).

## Atlas (de jure)

Consistent socioeconomic areal masks, which are not time-dependent, are contained in [Eoscala 1.5](https://datavault.confoederatio.org/s/2Kytdej7ABpw4rr)’s `/admin_modern/` folder, with the following file structure:

- `geocodes.csv` - ISO3 map.
- `geocodes.png` - ISO3 raster.
- `hmd.png` - Human Mortality Database areas.
- `hmd_geocodes.csv` - Human Mortality Database map.
- `iso2.png` - ISO2 map, based off the area codes used by the World Inequality Database.
- `iso2_geocodes.csv` - ISO2 flat-map, matching direct colourcodes to their ISO2.
- `iso2_regions.csv` - ISO2 map for individual regions as defined by the World Inequality Database/World Bank.
- `iso3_ilo_geocodes.csv` - ISO3 map as used by the International Labour Organisation.

### File Structure.

`dejure/`: 

- `atlas_dejure.naissance` - Composite .naissance file containing Seshat, Correlates of War, and CShapes-2.0 geometries.
- `atlas_seshat.naissance` - .naissance file containing only Seshat geometries. These geometries are reduced from `atlas_simplified.naissance`.
- `atlas_simplified.naissance` - Simplified de facto map isomorphic to Seshat, allowing for the splitting of Seshat IDs/polities into multiple sub-polities.
- `atlas_seshat_map.txt` - Mapping between Atlas polity IDs and Seshat polity IDs. Recommended for use only if you intend on using `atlas_simplified.naissance` instead of the pre-reduced dejure/seshat versions.

### Data Structure.

`atlas_seshat_map.txt`: 

- Atlas_ID | Split_From | Split_To | Atlas_Name | Seshat_ID - Note that Split_From, Split_To refers to the temporal domain of the polity.
- number | number | number | string | string

`.naissance`:

- `.id`: string
- `.description`: string
- `.name`: string
- `.cow_code`: number - Correlates of War code for the given polity (1815AD-2025AD).
- `.gwcode`: number - CShapes-2.0/Gleditsch and Ward code for the given polity (1886AD-2025AD).
- `.seshat_id`: string - The Seshat ID for the given polity (3500BC-2025AD).
