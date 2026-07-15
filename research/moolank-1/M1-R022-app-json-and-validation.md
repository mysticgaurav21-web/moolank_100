# M1-R022 — App JSON and Validation

## Metadata
- Record ID: M1-R022
- Status: Validation specification complete

## Deliverable
Canonical app record: `data/moolank/moolank-1.json` validated against `schemas/moolank-profile.schema.json`.

## Required checks
1. `schemaVersion` equals `1.0`.
2. `profileId` equals `M-1-FOUNDATION`.
3. `number` equals `1`.
4. Status is one of the schema enums.
5. All 14 required content domains are present.
6. Every string list contains unique, meaningful items.
7. Every conditional shadow contains triggers and protective factors.
8. `scientificBirthNumberLink` equals `not-established`.
9. Reference objects contain source type, publisher, title, URI and usage.
10. Safety disclaimer, prohibited claims and questionnaire boundary are present.
11. No additional properties outside the shared schema.
12. JSON parses successfully and validates with Draft 2020-12.

## Content QA
- conditional rather than deterministic language;
- no diagnosis, medical claims or event prediction;
- balanced and under-pressure coverage;
- no fixed profession, relationship or wealth outcome;
- psychology constructs do not validate numerology;
- compound dates remain calculation metadata, not separate personalities;
- practical supports are low-risk and revisable.

## Suggested automated validation
Use a Draft 2020-12 JSON Schema validator in CI. Validation failure must block canonical status.

## Release criteria
Moolank 1 is complete when:
- the JSON file validates;
- the master index marks profile 1 canonical;
- research units M1-R001 through M1-R022 exist;
- the repository status identifies Moolank 2 as the next foundation profile.

## Result
The consolidated record is approved for canonical creation and repository tracking updates.