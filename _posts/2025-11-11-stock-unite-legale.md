---
title: "StockUniteLegale file description (SIREN)"
layout: single
tags: [finance, siren]
categories: [finance]
author_profile: true
---

The following are the french and english translation for the fields in the StockUniteLegale file from the INSEE SIRENE database.

Description
StockUniteLegale is the INSEE SIRENE "stock" file listing legal units (companies/organizations) in France.
Format: CSV (UTF-8) packaged in a zip archive; one row per legal unit (SIREN as primary key).
Purpose: authoritative registry data for legal entities — identifiers, legal name, status, dates, activity codes, size and administrative metadata.

Key contents (examples)
* siren — SIREN company identifier.
* denominationUniteLegale - legal_name.
* dateCreationUniteLegale - creation_date.
* etatAdministratifUniteLegale - administrative_status.
* activitePrincipaleUniteLegale - main_activity_code (NAF).
* nicSiegeUniteLegale - head_office_nic.
* Personnel and size fields - trancheEffectifsUniteLegale, anneeEffectifsUniteLegale.
* Personal name fields for individual units - nomUniteLegale, prenom1UniteLegale, etc.
* Publication / processing metadata - statutDiffusionUniteLegale, dateDernierTraitementUniteLegale, nombrePeriodesUniteLegale

Usage notes
Use for company lookup, data enrichment and analytics; join on siren.
Large dataset — handle streaming/line-by-line parsing and consider incremental updates.
Public download (snapshot): https://object.infra.data.gouv.fr/browser/data-pipeline-open/siren/stock/2025-11-01-StockUniteLegale_utf8.zip.
Be aware some identifiers (tax IDs) may have restricted public use.


| French Header                                 | English Translation                                      | English Column Name         |
|-----------------------------------------------|----------------------------------------------------------|-----------------------------|
| `siren`                                       | Company ID (SIREN number)                                | `company_id`                |
| `statutDiffusionUniteLegale`                  | Data publication status                                  | `publication_status`        |
| `unitePurgeeUniteLegale`                      | Purged unit indicator                                    | `purged_unit`               |
| `dateCreationUniteLegale`                     | Company creation date                                    | `creation_date`             |
| `sigleUniteLegale`                            | Company acronym                                          | `acronym`                   |
| `sexeUniteLegale`                             | Gender (for individuals)                                 | `gender`                    |
| `prenom1UniteLegale`                          | First name                                               | `first_name`                |
| `prenom2UniteLegale`                          | Second name                                              | `second_name`               |
| `prenom3UniteLegale`                          | Third name                                               | `third_name`                |
| `prenom4UniteLegale`                          | Fourth name                                              | `fourth_name`               |
| `prenomUsuelUniteLegale`                      | Commonly used first name                                 | `usual_first_name`          |
| `pseudonymeUniteLegale`                       | Pseudonym                                                | `pseudonym`                 |
| `identifiantAssociationUniteLegale`           | Association identifier                                   | `association_id`            |
| `trancheEffectifsUniteLegale`                 | Employee size range                                      | `employee_range`            |
| `anneeEffectifsUniteLegale`                   | Year of employee count                                   | `employee_year`             |
| `dateDernierTraitementUniteLegale`            | Last processing date                                     | `last_processed_date`       |
| `nombrePeriodesUniteLegale`                   | Number of periods recorded                               | `number_of_periods`         |
| `categorieEntreprise`                         | Company size category (e.g., SME, large enterprise)      | `company_size_category`     |
| `anneeCategorieEntreprise`                    | Year of company size classification                      | `company_size_year`         |
| `dateDebut`                                   | Start date of the current period                         | `period_start_date`         |
| `etatAdministratifUniteLegale`                | Administrative status (e.g., active, closed)             | `administrative_status`     |
| `nomUniteLegale`                              | Last name (for individuals)                              | `last_name`                 |
| `nomUsageUniteLegale`                         | Used last name (if different)                            | `used_last_name`            |
| `denominationUniteLegale`                     | Legal name of the company                                | `legal_name`                |
| `denominationUsuelle1UniteLegale`             | Common name 1                                            | `common_name_1`             |
| `denominationUsuelle2UniteLegale`             | Common name 2                                            | `common_name_2`             |
| `denominationUsuelle3UniteLegale`             | Common name 3                                            | `common_name_3`             |
| `categorieJuridiqueUniteLegale`               | Legal category (e.g., SARL, SAS)                         | `legal_category`            |
| `activitePrincipaleUniteLegale`               | Main business activity (NAF code)                        | `main_activity_code`        |
| `nomenclatureActivitePrincipaleUniteLegale`   | Classification system used (usually NAF Rev. 2)          | `activity_classification`   |
| `nicSiegeUniteLegale`                         | NIC code of the head office                              | `head_office_nic`           |
| `economieSocialeSolidaireUniteLegale`         | Social and solidarity economy indicator                  | `social_economy_indicator`  |
| `societeMissionUniteLegale`                   | Mission-driven company indicator                         | `mission_driven_company`    |
| `caractereEmployeurUniteLegale`               | Employer status (yes/no)                                 | `employer_status`           |

Sample records:

`
000325175,O,,2000-09-26,,M,THIERRY,,,,THIERRY,,,NN,,2024-03-22T14:26:06,6,PME,2023,2018-02-07,A,JANOYER,,,,,,1000,32.12Z,NAFRev2,00065,,,
001807254,O,,1972-05-01,,M,JACQUES-LUCIEN,,,,JACQUES-LUCIEN,,,NN,,2024-03-22T14:26:06,5,,,2014-12-31,C,BRETON,,,,,,1000,85.59A,NAFRev2,00022,,,
005410220,O,true,1954-12-25,,M,GEORGES,,,,GEORGES,,,NN,,2024-03-22T14:26:06,1,,,1988-03-31,C,WATTEBLED,,,,,,1000,22.02,NAP,00015,,,
005410345,O,true,,,M,MICHEL,,,,MICHEL,,,NN,,2024-03-22T14:26:06,1,,,1984-12-25,C,DEBRAY,,,,,,1000,79.06,NAP,00010,,,
005410394,O,true,1954-12-25,,M,ROBERT,ALFRED,,,ROBERT,,,NN,,2024-03-22T14:26:06,1,,,1987-12-01,C,DAULT,,,,,,1000,64.42,NAP,00018,,,
005410428,O,true,1954-01-01,,M,RENE,PIERRE,,,RENE,,,NN,,2024-03-22T14:26:06,1,,,1989-06-11,C,DINGEON,,,,,,1000,70.2C,NAF1993,00014,,,
005410436,O,true,,,M,MARCEL,,,,MARCEL,,,NN,,2024-03-22T14:26:06,1,,,1984-12-25,C,CARBONNET,,,,,,1000,57.11,NAP,00017,,,
005410485,O,true,,,M,RENE,ALFRED,,,RENE,,,NN,,2024-03-22T14:26:06,1,,,1985-12-25,C,LECRIVAIN,,,,,,1000,64.42,NAP,00014,,,
005410493,O,true,1954-12-25,,M,PIERRE,,,,PIERRE,,,NN,,2024-03-22T14:26:06,1,,,1985-12-01,C,GODIN,,,,,,1000,86.06,NAP,00018,,,
`


The file can be downloaded from the INSEE SIRENE database at: [StockUniteLegale]




[StockUniteLegale]: https://object.infra.data.gouv.fr/browser/data-pipeline-open/siren/stock/2025-11-01-StockUniteLegale_utf8.zip