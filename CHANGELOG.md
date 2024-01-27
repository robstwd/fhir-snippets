# Change Log

All notable changes to the "fhir-snippets" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [0.1.1] - 2024-01-28

### Added

- added the [core spec extension patient-birthTime](https://hl7.org/fhir/extensions/StructureDefinition-patient-birthTime.html) on HL7AU Patient profiles (on element `Patient.birthDate`)
- added element `Patient.communication.preferred` to AU Patient profile snippets
- add hyperlinks for resources to readme

### Changed

- reformatted readme to remove markdown formatting violations (using [markdownlint](https://github.com/DavidAnson/markdownlint))
- reverted the superscript tag in the readme, back to using `<sup>`

### Removed

- nil

### Fixed

- corrected the bad ordering of numbered placeholder elements in the Patient resource snippets

[0.1.1]: https://github.com/robstwd/fhir-snippets/compare/v0.1.0...v0.1.1

## [0.1.0] - 2023-12-23

### Added

- added snippet for FHIR Organization aligned to AU PD Organisation profile
- added snippet for FHIR Organization aligned to PCA Organisation profile
- added snippet for FHIR HealthcareService aligned to PCA Healthcare Service profile
- added snippet for FHIR Identifier aligned to PCA Healthcare Service Identifier (PCA-HSI) profile
- added hyperlinks to Changelog for GitHub tag comparison
- added sections in README for feature and usage
- added missing description for AU Core Organisation snippet
- added missing description for AU Core HealthcareService snippet 
- added internal snippet to facilitate Changelog updates

### Changed

- nil

### Removed

- removed redundant text from a changelog entry

### Fixed

- readme typo

[0.1.0]: https://github.com/robstwd/fhir-snippets/compare/v0.0.7...v0.1.0

## [0.0.7] - 2023-10-26

### Fixed

- corrected display value TODO string (added hyphen)
- corrected change log heading
- fixed typos
- fixed snippet JSON formatting
- fixed ordering of snippet inserted text entries

### Added

- Location snippet aligned to PCA Location of kind physical

### Removed

#### AU Core Patient profile snippet

- removed the `active=true` constraint (following decision taken recently at AU Core Technical Working Group meetings)
- removed date of arrival extension (following decision taken recently at AU Core Technical Working Group meetings)

#### AU Core PractitionerRole profile snippet

- removed PractitionerRole.healthcareService (following decision taken recently at AU Core Technical Working Group meetings)
- removed PractitionerRole.identifier related to HPI-I (following decision taken recently at AU Core Technical Working Group meetings)
- removed the `active=true` constraint (following decision taken recently at AU Core Technical Working Group meetings)

#### AU Core Practitioner profile snippet

- removed the `active=true` constraint (following decision taken recently at AU Core Technical Working Group meetings)

#### AU Core Organisation profile snippet

- removed the `active=true` constraint (following decision taken recently at AU Core Technical Working Group meetings)

#### AU Core HealthcareService profile snippet

- removed the `active=true` constraint (following decision taken recently at AU Core Technical Working Group meetings)

#### AU Core RelatedPerson profile snippet

- removed the `active=true` constraint (following decision taken recently at AU Core Technical Working Group meetings)

[0.0.7]: https://github.com/robstwd/fhir-snippets/compare/v0.0.6...v0.0.7

## [0.0.6] - 2023-09-24

### Added

- snippet files for FHIR RelatedPerson instance examples

[0.0.6]: https://github.com/robstwd/fhir-snippets/compare/v0.0.5...v0.0.6

## [0.0.5] - 2023-09-24

### Added

- README updated with full details of supported FHIR structures

[0.0.5]: https://github.com/robstwd/fhir-snippets/compare/v0.0.4...v0.0.5

## [0.0.4] - 2023-09-23

### Added

- changelog details

## [0.0.3] - 2023-09-23

### Added

- snippet files for other FHIR resources, ie HealthcareService, Organization, Patient & PractitionerRole
- various infrastructure files for the extension
- first upload to the extension Marketplace

## [0.0.2] - 2023-09-23

### Added

- snippet files for FHIR Practitioner instance examples and various pertinent identifiers

## [0.0.1] - 2023-09-23

- Initial poking around
