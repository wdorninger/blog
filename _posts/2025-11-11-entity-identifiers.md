---
title: "Entity Identifiers: Global and Local Data Sources"
layout: single
tags: [finance, lei, legal entity]
categories: [blog]
author_profile: true
---

Global open data sources:
1. GLEIF — [GLEIF] — Legal Entity Identifier (LEI)
2. OpenCorporates — https://opencorporates.com — OpenCorporates company records (jurisdictional company number + OC ID)

Global commercial providers:
3. Dun & Bradstreet — https://www.dnb.com — DUNS / D‑U‑N‑S Number (commercial)
4. Orbis / Bureau van Dijk (commercial) — https://www.bvdinfo.com — proprietary company IDs


Local data sources (to be verified)
Selected national/local registries (authority — website — identifier)
1. United States — Secretary of State registries (varies by state) — state company number; IRS — https://www.irs.gov — EIN (Employer Identification Number, not always public)
Corporations
2. Canada (federal filings) — https://www.ontario.ca/page/ontario-business-registry
   ... todo: list the various registers
3. United Kingdom — Companies House — https://www.gov.uk/government/organisations/companies-house — Company Number, 
   downloadable at https://download.companieshouse.gov.uk/en_output.html
4. France — INSEE / Sirene — https://www.insee.fr/en/information/2406152 — SIREN (9 digits), SIRET (SIREN+NIC 14 digits)
   * https://www.data.gouv.fr/dataservices/api-sirene-open-data/, 
   * https://www.data.gouv.fr/dataservices 
   * https://www.data.gouv.fr/datasets/base-sirene-des-entreprises-et-de-leurs-etablissements-siren-siret/
   * Filter and download: https://annuaire-entreprises.data.gouv.fr/export-sirene 

   * The historical SIRENE files - **stockUniteLegale** – Legal units (companies), **stockEtablissement** – Establishments (branches, locations) - https://object.infra.data.gouv.fr/browser/data-pipeline-open/siren/stock/

5. Germany — Handelsregister / Bundesanzeiger — https://www.handelsregister.de / https://www.bundeskartellamt.de (
   info) — Handelsregisternummer; USt‑IdNr (VAT ID) via BZSt
6. Spain — Registro Mercantil — https://www.registradores.org / https://www.registradores.org/ — CIF/NIF (tax ID for
   companies) and Registro Mercantil registration number
7. Italy — Registro delle Imprese (Infocamere) — https://www.registroimprese.it — REA / Company registration, Codice
   Fiscale / Partita IVA (VAT ID), Corporate Identity Number (CIN)
8. Netherlands — Kamer van Koophandel (KvK) — https://www.kvk.nl — KvK number
9. Belgium — Banque-Carrefour des Entreprises / Kruispuntbank van Ondernemingen (
   BCE/KBO) — https://kbopub.economie.fgov.be — Enterprise Number (Numéro d'entreprise / Ondernemingsnummer)
10. Luxembourg — Registre de Commerce et des Sociétés (RCS) — https://www.rcsl.lu — RCS number
11. Switzerland — UID Registry — https://www.uid.admin.ch — UID (CHE‑xxxxxx.xxxx)
12. Sweden — Bolagsverket — https://www.bolagsverket.se — Organisationsnummer
13. Norway — Brønnøysundregistrene — https://www.brreg.no — Organisasjonsnummer
14. Denmark — Danish Business Authority / CVR — https://datacvr.virk.dk — CVR number
15. Finland — Finnish Patent and Registration Office — https://www.prh.fi — Y‑tunnus (business ID)
16. Ireland — Companies Registration Office (CRO) — https://www.cro.ie — Company Number
17. Portugal — Conservatória do Registo Comercial / Empresa Na Hora — https://www.irn.mj.pt — NIPC / Número de
    Identificação de Pessoa Colectiva
18. Greece — General Commercial Registry (GEMI) / AADE — https://www.businessregistry.gr / https://www.aade.gr — GEMI
    reg. number; AFM (Tax Identification Number)
19. Poland — National Court Register (KRS) & GUS — https://ekrs.ms.gov.pl / https://stat.gov.pl — KRS number; REGON (
    statistical id)
20. Czech Republic — ARES / Justice.cz — https://www.justice.cz / https://wwwinfo.mfcr.cz — IČO (identification number)
21. Hungary — Company Court (Court of Registration) — https://cegtar.hu / https://www.e-cegjegyzek.hu — Cégjegyzékszám
22. Russia — Federal Tax Service / EGRUL — https://www.nalog.ru — OGRN, INN
23. India — Ministry of Corporate Affairs (MCA) — https://www.mca.gov.in — CIN (Corporate Identity Number); PAN; GSTIN (
    tax/GST ID)
24. China — National Enterprise Credit Information Publicity System — http://www.gsxt.gov.cn / enterprise info portals —
    Unified Social Credit Code (USCC)
25. Japan — National Tax Agency / Corporate Number Publication Site — https://www.houjin-bangou.nta.go.jp — Corporate
    Number (法人番号)
26. Australia — Australian Business Register / ABR — https://abr.business.gov.au — ABN (Australian Business Number);
    ASIC company number (ACN)
27. New Zealand — NZBN — https://www.nzbn.govt.nz — NZBN (New Zealand Business Number)
28. Canada — Corporations Canada / provincial registries — https://www.ic.gc.ca/eic/site/cd-dgc.nsf — Federal
    corporation number; Business Number (BN) via CRA
29. Brazil — Receita Federal / CNPJ Central — https://www.gov.br/receitafederal/ — CNPJ (Cadastro Nacional da Pessoa
    Jurídica)
30. Mexico — Registro Federal de Contribuyentes (SAT) / Public Registries — https://www.sat.gob.mx — RFC (tax ID)
31. South Africa — Companies and Intellectual Property Commission (CIPC) — https://www.cipc.co.za — Company registration
    number
32. Turkey — Central Registry (MERSIS) / Trade Registry Gazettes — https://mersis.gtb.gov.tr — MERSIS number; Tax ID
33. Israel — Registrar of Companies / VAT — https://www.gov.il/en/departments/registrar_of_companies — Company number;
    VAT number
34. Singapore — Accounting and Corporate Regulatory Authority (ACRA) — https://www.acra.gov.sg — UEN (Unique Entity
    Number)
35. Hong Kong — Companies Registry — https://www.cr.gov.hk — Company Number
36. UAE — Department of Economic Development / Federal registries /
    FTA — https://www.business.gov.ae / https://www.tax.gov.ae — Trade license number; TRN (Tax Registration Number) for
    VAT
37. Saudi Arabia — Ministry of Commerce / ZATCA — https://mci.gov.sa / https://zatca.gov.sa — Commercial Registration (
    CR) number; VAT TRN
38. South Korea — National Tax Service / Corporate registration — https://www.hometax.go.kr — Business Registration
    Number (사업자등록번호)
39. Argentina — AFIP — https://www.afip.gob.ar — CUIT
40. Chile — Servicio de Impuestos Internos (SII) / Registro de Empresas — https://www.sii.cl — RUT
41. Colombia — Cámara de Comercio / DIAN — https://www.rues.org.co / https://www.dian.gov.co — NIT; Cámara registration
    number
[GLEIF]: https://www.gleif.org

Notes
Identifier availability and public access vary by jurisdiction (some tax IDs are non‑public or restricted).
For authoritative LEI data use GLEIF; for broad cross‑jurisdictional scraping/use consider OpenCorporates (subject to terms).
Many countries also provide VAT ID validation (EU VIES: https://ec.europa.eu/taxation_customs/vies/) and commercial services (D&B, Bureau van Dijk) for enriched identifiers.