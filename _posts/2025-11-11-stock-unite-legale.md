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

{% highlight csv %}
company_id,publication_status,purged_unit,creation_date,acronym,gender,first_name,second_name,third_name,fourth_name,usual_first_name,pseudonym,association_id,employee_range,employee_year,last_processed_date,number_of_periods,company_size_category,company_size_year,period_start_date,administrative_status,last_name,used_last_name,legal_name,common_name_1,common_name_2,common_name_3,legal_category,main_activity_code,activity_classification,head_office_nic,social_economy_indicator,mission_driven_company,employer_status
000325175,O,,2000-09-26,,M,THIERRY,,,,THIERRY,,,NN,,2024-03-22T14:26:06,6,PME,2023,2018-02-07,A,JANOYER,,,,,,1000,32.12Z,NAFRev2,00065,,,
001807254,O,,1972-05-01,,M,JACQUES-LUCIEN,,,,JACQUES-LUCIEN,,,NN,,2024-03-22T14:26:06,5,,,2014-12-31,C,BRETON,,,,,,1000,85.59A,NAFRev2,00022,,,
005411582,O,,1954-01-01,,M,RENE,PIERRE,ANDRE,,RENE,,,NN,,2024-03-22T14:26:06,4,,,2008-01-01,A,GERVOISE,,,,,,1000,68.20B,NAFRev2,00017,,,
005420021,O,,1954-01-01,,,,,,,,,,NN,,2024-03-22T14:26:06,7,PME,2023,2011-06-10,A,,,ETABLISSEMENTS LUCIEN BIQUEZ,,,,5710,46.69B,NAFRev2,00056,,,
005420047,O,,1954-01-01,,,,,,,,,,NN,,2024-03-22T14:26:06,4,,,2008-09-26,C,,,SOCIETE ANONYME MARCEL CARON ET FILS,,,,5599,45.3F,NAFRev1,00010,,,
005420104,O,,1954-01-01,,,,,,,,,,NN,,2024-03-22T14:26:06,4,,,2013-12-16,C,,,VETEMENTS JARDI,,,,5499,47.71Z,NAFRev2,00019,,,
005420120,O,,1954-01-01,,,,,,,,,,03,2023,2025-10-09T12:01:24,5,PME,2023,2020-10-23,A,,,SOCIETE DES SUCRERIES DU MARQUENTERRE,,,,5599,70.10Z,NAFRev2,00031,N,,
{% endhighlight %}


The file can be downloaded from the INSEE SIRENE database at: [StockUniteLegale]




[StockUniteLegale]: https://object.infra.data.gouv.fr/browser/data-pipeline-open/siren/stock/2025-11-01-StockUniteLegale_utf8.zip