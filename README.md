# Decentralization Reform in Ukraine (2014 -2022)

The project investigates the effects of restructurization of local councils (i.e. "rada", N = 11,250) into amalgamated territorial communities (i.e. "hromada", N = 1,469) and the effect of this tranformation on key macroeconomic and social indicators. Of specific interest is hromadas' resiliance to full-scale russian invasion launched on 2022-02-24.

The project is funded by GIZ within its project "Support to the Decentralisation Reform in Ukraine (UDU U-LEAD with Europe. Phase II) (#`81281025`)

![](https://www.nationsonline.org/maps/Ukraine-Administrative-Map.jpg)

| Name              | Role                                                            | \@         |
|--------------|-------------------------------------------|--------------|
| Tymofii Brik      | Lead Researcher                                                 |            |
| Andriy Darkovich  | Research Assistant                                              |            |
| Valentyn Hatsko   | Data Analyst                                                    | valgat29   |
| Andriy Koval      | Statistical modeling, data visualization, reproducible research | andkov     |
| Maryna Rabinovych | Senior Researcher                                               |            |
| Myroslava Savisko | Project Manager                                                 | splanetina |
| Serhii Tytiuk     | Data Analyst                                                    | tytser     |
| Igor Piddubniy    | Data Analyst                                                    | ipiddubnyi |

# Surveys

The Kyiv School of Economics (KSE) Institute conducted two surveys of hromadas in 2022 to study the impact of Russia's full-scale invasion on their economic performance and to identify factors of hromada resilience to various types of war-related shocks.

<table>
<colgroup>
<col style="width: 29%" />
<col style="width: 48%" />
<col style="width: 22%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>Survey #1</p></th>
<th><p>Survey #2</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Lead center</strong></p></td>
<td><p>KSE Agrocenter</p></td>
<td><p>KSE Center for Sociological Research Decentralization<br />
and Regional Development</p></td>
</tr>
<tr class="even">
<td><p><strong>Target audience</strong></p></td>
<td><p>Local authorities of hromadas </p></td>
<td><p>Local authorities of hromadas </p></td>
</tr>
<tr class="odd">
<td><p><strong>Survey mode</strong></p></td>
<td><p>Web survey</p></td>
<td><p>Web survey</p></td>
</tr>
<tr class="even">
<td><p><strong>Sample size</strong></p></td>
<td><p>477 hromadas</p></td>
<td><p>138 hromadas</p></td>
</tr>
<tr class="odd">
<td><p><strong>Fieldwork dates</strong></p></td>
<td><p>June-August 2022</p></td>
<td><p>October-November 2022</p></td>
</tr>
</tbody>
</table>

### **Map of hromadas participated in the surveys**

````{=html}
{r, echo=FALSE, results='asis'}
xfun::file_string('./map_surveys.html')
````

# Reports

-   [Resilience Survey overview](https://raw.githack.com/kse-ua/ua-de-center-serve/main/analysis/survey-overview/survey-overview.html) - Results and Key findings of the Resiliance Survey

-   [Hromada Dashboard](https://valentyn-hatsko.shinyapps.io/hromada-dash/) - Dashboard with Data on Territorial Communities

# Data Products

| Data Product Name                      | Description                                                                                                                                                                                                                                                                                                                                                                                            | Current State / Left To Do                                                                               | Script                                        |
|-----------|---------------------------------------|-----------|-----------|
| Admininstrative Units                  | Relationship among multiple administrative levels (settlement, rada, hromada, raion, oblast, region)                                                                                                                                                                                                                                                                                                   | ready for analysis at `./data-public/derived/ua-admin-map-2020.csv`                                      | `./manipulation/ellis-ua-admin.R`             |
| Admin History                          | Composition of hromadas (what radas comprise it) at every point in time when such composition changed, from 2014 to 2020                                                                                                                                                                                                                                                                               | push to ./data-public/derived/                                                                           | `./manipulation/ellis-rada-hromada.R`         |
| Population                             | Population counts at the level of hromada                                                                                                                                                                                                                                                                                                                                                              | Add more years (currently only 2021), push to ./data-public/derived/                                     | `./manipulation/ellis-demography.R`           |
| Open Budget                            | Tax revenues of admin units                                                                                                                                                                                                                                                                                                                                                                            | No clarity yet. Classify hromadas based on complexity of their admin history                             | `./manipulation/ellis-budget.R`               |
| Open Budget                            | Tax revenues of hromadas 2020-2022                                                                                                                                                                                                                                                                                                                                                                     | ready for analysis at `./data-public/derived/hromada_budget_2020_2022.xlsx`                              | `./manipulation/ellis-budget-2020-2022.R`     |
| Geographic                             | Main spatial features of hromadas: area, coordinates of hromada center, travel time to oblast center, mountain hromadas, distance from hromada centers to the nearest point of the border with Russia, Russia or Belarus, or the EU; hromadas within 30 km of the sea/30 km of the border/30 km of the border with Russia and Belarus; hromadas within 15 km of international roads and national roads | ready for analysis at `./data-public/derived/geography.csv`                                              | `./manipulation/ellis-geography.R`            |
| Geographic                             | Spatial poligons of hromadas                                                                                                                                                                                                                                                                                                                                                                           | Demonstate graphing maps (at hromada-raion-oblast level) using a replacable quantifier (e.g. population) |                                               |
| Community Competence                   | Number of youth centers, youth councils and centers for entrepreneurial support                                                                                                                                                                                                                                                                                                                        | ready for analysis at `./data-public/derived/community-competence-hromada.csv`                           | `./manipulation/ellis-community-competence.R` |
| Health Declarations                    | Number of declarations with health facilities as of February 2022                                                                                                                                                                                                                                                                                                                                      | ready for analysis at `./data-public/derived/declarations-hromada.csv`                                   | `./manipulation/ellis-health.R`               |
| OSBB (Homeowners Associations)         | Number of homeowners associations in 2015-2020                                                                                                                                                                                                                                                                                                                                                         | ready for analysis at `./data-public/derived/osbb-hromada.csv`                                           | `./manipulation/ellis-health.R`               |
| Passengers                             | Number of passengers arriving at hromada railway stations in 2021                                                                                                                                                                                                                                                                                                                                      | push to ./data-public/derived/                                                                           | `./manipulation/ellis-osbb.R`                 |
| ZNO (External Independent Examination) | Mean scores of ZNO (standardized test) for main subjects                                                                                                                                                                                                                                                                                                                                               | Add more years (currently only 2021), push to ./data-public/derived/                                     | `./manipulation/ellis-zno.R`                  |
| War zones                              | Statuses of the war zone/occupation according to the Ministry of Regional Development                                                                                                                                                                                                                                                                                                                  | push to ./data-public/derived                                                                            | `./manipulation/ellis-war-status.R`           |
| E-dem                                  | Form of electronic participation in hromadas                                                                                                                                                                                                                                                                                                                                                           | push to ./data-public/derived                                                                            | `./manipulation/ellis-edem.R`                 |
| DFRR                                   | Data on cost of the projects financed by the State Regional Development Fund                                                                                                                                                                                                                                                                                                                           | ready for analysis                                                                                       | `./manipulation/ellis-dfrr.R`                 |
| Hromada Mayors Bio                     | Information on mayor of hromadas that were elected in 2020 local elections                                                                                                                                                                                                                                                                                                                             | ready for analysis at `./data-public/raw/hromada_heads.xlsx`                                             | `./manipulation/ellis-mayors.R`               |
