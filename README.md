# Phytoplankton Species Lookup

A single-page web application to look up phytoplankton species and retrieve Darwin Core taxonomic data from [WoRMS (World Register of Marine Species)](https://www.marinespecies.org/).

## Features
- Search by species or genus name with fuzzy/partial matching
- Displays full Darwin Core fields: scientificName, scientificNameAuthorship, taxonRank, kingdom, phylum, class, order, family, genus, species, scientificNameID (LSID), taxonID (AphiaID), taxonomicStatus, acceptedNameUsage, acceptedNameUsageID
- Handles multiple matches with a selectable results list
- Links directly to each species' WoRMS page
- Export all results to CSV with Darwin Core headers
- Error handling: no results, API timeout, network failure

## Usage
Open `index.html` in a web browser. No build step or server required.

## API
Uses the [WoRMS REST API](https://www.marinespecies.org/rest/): `GET /AphiaRecordsByName/{name}?like=true&marine_only=true`
