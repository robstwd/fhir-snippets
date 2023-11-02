# FHIR Snippets in XML

This extension is a collection of VS Code snippets to create instances of various  HL7<sup>&reg;</sup> FHIR<sup>&reg;&copy;</sup> resources, aligned to an Australian context.

The primary motivations to develop this extension:
1. learning 
2. always seeking efficiencies
3. share with colleagues 

## FHIR
Refer to the main FHIR specification page [https://hl7.org/fhir/R4/index.html](https://hl7.org/fhir/R4/index.html)

## Scope
- support for xml instances only at this time 
- FHIR R4 (4.0.1 and probably R4B)
- support for Australian context

## Features
This extension supports snippets for
- entire FHIR resource types, such as Patient, Practitioner, HealthcareService, Location, Organization, PractitionerRole and RelatedPerson
  - each resource type is represented in a number of '_flavours_', that comply with the core spec as well as various profiles in the Australian context; such as HL7AU AU Base profiles, or HL7AU AU Core profiles. See below for the complete list of supported _flavours_.
  - each of the file snippets represents a complete FHIR resource, with all mandatory elements and the majority of available optional elements. The optional elements can then just be deleted as desired to support the scenario of interest
  - snippets complying with AU Core profiles include all mandatory elements and only optional elements that have must support as true
  - the sample values supplied use the string "TODO" to be a prompt for the user to update with desired values
  - where terminology based elements have a discrete list of codes, they are supported by a drop down pick list in the snippet
- Identifier datatype nodes, such as IHI or HPI-I identifiers
  - Identifier snippets can be inserted into any of the above complete FHIR resources in the standard element ordering
  - Identifier snippets are organised by applicable resource type and closely follow the definitions in the AU Base Identifier datatype profiles
  - see below for a complete list of available Identifier types

## Usage
1. Within an empty file of type `.xml`
2. Invoke the list of available snippets as a pop up by 
   1. pressing `Ctrl + Space`
   2. opening the command palette (`Ctrl + Shift + p`), type 'snippet' and choose 'insert snippet'
   3. pressing `Shift + Alt + s`
3. Scroll the list or start typing characters from the prefixes listed in the tables below
4. Eg to filter the snippets to those related to AU Base profiles, type `aubase` or to find all Identifiers, type `identifier` or part thereof
5. Scroll down to one of the choices and hit enter, upon which the specific XML nodes are added
6. Choose from the available pick lists and update data to support the example scenario 

## Supported resources
### HealthcareService
#### Resource flavours
The following flavours of the HealthcareService resource are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Example FHIR HealthcareService core spec | `HealthcareService-corespec` | [Core R4 HealthcareService](https://hl7.org/fhir/R4/healthcareservice.html) |
| Example FHIR HealthcareService AU Base | `HealthcareService-aubase` | [AU Base HealthcareService](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-healthcareservice.html) |
| Example FHIR HealthcareService AU Core | `HealthcareService-aucore` | [AU Core HealthcareService](https://build.fhir.org/ig/hl7au/au-fhir-core/StructureDefinition-au-core-healthcareservice.html) |

#### Identifier types
The following Identifier types pertinent for the HealthcareService resource in an Australian context are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| HealthcareService-Identifier-Residential Aged Care Service Identifier | `HealthcareService-Identifier-ResidentialAgedCareServiceIdentifier` | [AU Residential Aged Care Service Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-residentialagedcareserviceidentifier.html) |
| HealthcareService-Identifier-HPI-O | `HealthcareService-Identifier-HPI-O` and `hpio` | [AU HPI-O Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-hpio.html) |

### Location
#### Resource flavours
The following flavours of the Location resource are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Example FHIR Location core spec | `Location-corespec` | [Core R4 Location](https://hl7.org/fhir/R4/location.html) |
| Example FHIR Location AU Base | `Location-aubase` | [AU Base Location](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-location.html) |
| Example FHIR Location AU Core | `Location-aucore` | [AU Core Location](https://build.fhir.org/ig/hl7au/au-fhir-core/StructureDefinition-au-core-location.html) |
| Example FHIR Location PCA mobile | `Location-pca-mobile` | [PCA Location](https://pca.digitalhealth.gov.au/fhir/4.0/2.4.0/StructureDefinition-pca-location.html) of type 'mobile'|
| Example FHIR Location PCA virtual | `Location-pca-virtual` | [PCA Location](https://pca.digitalhealth.gov.au/fhir/4.0/2.4.0/StructureDefinition-pca-location.html) of type 'virtual'|
| Example FHIR Location PCA physical | `Location-pca-physical` | [PCA Location](https://pca.digitalhealth.gov.au/fhir/4.0/2.4.0/StructureDefinition-pca-location.html) of type 'physical'|

#### Identifier types
The following Identifier types pertinent for the Location resource in an Australian context are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Location-Identifier-Location Specific Practice Number | `Location-Identifier-LocationSpecificPracticeNumber` | [Location Specific Practice Number Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-locationspecificpracticenumber.html) |
| Location-Identifier-NATA Site Number | `Location-Identifier-NATASiteNumber` | [AU NATA Site Number Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-natasitenumber.html) |
| Location-Identifier-Delivery Point Identifier | `Location-Identifier-dpid` | [AU Delivery Point Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-deliverypointidentifier.html) |
| Location-Identifier-Geocoded National Address File | `Location-Identifier-gnaf` | [AU G-NAF Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-gnafidentifier.html) |

### Organization
#### Resource flavours
The following flavours of the Organization resource are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Example FHIR Organization core spec | `Organization-corespec` | [Core R4 Organization](https://hl7.org/fhir/R4/organization.html) |
| Example FHIR Organization AU Base | `Organization-aubase` | [AU Base Organization](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-organization.html) |
| Example FHIR Organization AU Core | `Organization-aucore` | [AU Core Organization](https://build.fhir.org/ig/hl7au/au-fhir-core/StructureDefinition-au-core-organization.html) |

#### Identifier types
The following Identifier types pertinent for the Organization resource in an Australian context are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Organization-Identifier-HPI-O | `Organization-Identifier-HPI-O` and `hpio` | [AU HPI-O Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-hpio.html) |
| Organization-Identifier-PAI-O Identifier | `Organization-Identifier-PAI-O` and `paio` | [AU PAI-O Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-paioidentifier.html) |
| Organisation-Identifier-CSP Registration Number | `Organisation-Identifier-CSPRegistrationNumber` and `csp` | [AU CSP Registration Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-cspregistrationnumber.html) |
| Organization-Identifier-Australian Business Number | `Organization-Identifier-AustralianBusinessNumber` and `abn` | [AU Australian Business Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-australianbusinessnumber.html) |
| Organization-Identifier-Australian Company Number | `Organization-Identifier-AustralianCompanyNumber` and `acn` | [AU Australian Company Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-australiancompanynumber.html) |
| Organization-Identifier-Australian Registered Body Number | `Organization-Identifier-AustralianRegisteredBodyNumber` and `arbn` | [AU Australian Registered Body Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-australianregistredbodynumber.html) |
| Organization-Identifier-NATA Accreditation Number | `Organization-Identifier-NATAAccreditationNumber` | [AU NATA Accreditation Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-nataaccreditationnumber.html) |
| Organization-Identifier-Pharmacy Approval Number | `Organization-Identifier-PharmacyApprovalNumber` | [AU Pharmacy Approval Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-pharmacyapprovalnumber.html) |

### Patient
#### Resource flavours
The following flavours of the Patient resource are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Example FHIR Patient core spec | `Patient-corespec` | [Core R4 Patient](https://hl7.org/fhir/R4/patient.html) |
| Example FHIR Patient AU Base | `Patient-aubase` | [AU Base Patient](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-patient.html) |
| Example FHIR Patient AU Core | `Patient-aucore` | [AU Core Patient](https://build.fhir.org/ig/hl7au/au-fhir-core/StructureDefinition-au-core-patient.html) |

#### Identifier types
The following Identifier types pertinent for the Patient resource in an Australian context are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Patient-Identifier-IHI | `Patient-Identifier-IHI` and `ihi` | [AU IHI](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-ihi.html) |
| Patient-Identifier-MedicareNumber | `Patient-Identifier-Medicare` | [AU Medicare Card Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-medicarecardnumber.html) |
| Patient-Identifier-DVA | `Patient-Identifier-DVA` | [AU DVA Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-dvanumber.html) |
| Patient-Identifier-healthcarecardnumber | `Patient-Identifier-healthcarecardnumber` | [AU Health Care Card Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-healthcarecardnumber.html) |
| Patient-Identifier-pensionerconcessioncardnumber | `Patient-Identifier-pensionerconcessioncardnumber` and `pen` | [AU Pensioner Concession Card Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-pensionerconcessioncardnumber.html) |
| Patient-Identifier-commonwealthseniorshealthcardnumber | `Patient-Identifier-commonwealthseniorshealthcardnumber` and `csn` | [AU Commonwealth Seniors Health Card Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-cwlthseniorshealthcardnumber.html) |
| Patient-Identifier-medicalrecordnumber-hpioscoped | `Patient-Identifier-medicalrecordnumber-hpioscoped`, `mrn` and `hpio` | [AU Medical Record Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-medicalrecordnumber.html) |
| Patient-Identifier-medicalrecordnumber-abnscoped | `Patient-Identifier-medicalrecordnumber-abnscoped`, `mrn` and `abn` | [AU Medical Record Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-medicalrecordnumber.html) |
| Patient-Identifier-insurancemembernumber | `Patient-Identifier-insurancemembernumber` | [AU Insurance Member Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-insurancemembernumber.html) |

### Practitioner
#### Resource flavours
The following flavours of the Practitioner resource are supported:
| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Example FHIR Practitioner core spec | `Practitioner-corespec` | [Core R4 Practitioner](https://hl7.org/fhir/R4/practitioner.html) |
| Example FHIR Practitioner AU Base | `Practitioner-aubase` | [AU Base Practitioner](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-practitioner.html) |
| Example FHIR Practitioner AU Core | `Practitioner-aucore` | [AU Core Practitioner](https://build.fhir.org/ig/hl7au/au-fhir-core/StructureDefinition-au-core-practitioner.html) |

#### Identifier types
The following Identifier types pertinent for the Practitioner resource in an Australian context are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Practitioner-Identifier-HPI-I | `Practitioner-Identifier-HPI-I` and `hpii` | [AU HPI-I](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-hpii.html) |
| Practitioner-Identifier-PBS Prescriber Number | `Practitioner-Identifier-PBSPrescriberNumber` | [AU PBS Prescriber Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-pbsprescribernumber.html) |
| Practitioner-Identifier-Care Agency Employee Identifier | `Practitioner-Identifier-CareAgencyEmployeeIdentifier` | [AU Care Agency Employee Identifier](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-careagencyemployeeidentifier.html) |
| Practitioner-Identifier-Ahpra Registration Number | `Practitioner-Identifier-AhpraRegistrationNumber` | [AU Ahpra Registration Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-ahpraregistrationnumber.html) |
| Practitioner-Identifier-PCA Practitioner Identifier | `Practitioner-Identifier--pca-practitioner-identifier` | [PCA Practitioner Identifier](https://pca.digitalhealth.gov.au/fhir/4.0/StructureDefinition-pca-practitioner-identifier.html) |

### PractitionerRole
#### Resource flavours
The following flavours of the PractitionerRole resource are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Example FHIR PractitionerRole core spec | `PractitionerRole-corespec` | [Core R4 PractitionerRole](https://hl7.org/fhir/R4/practitionerrole.html) |
| Example FHIR PractitionerRole AU Base | `PractitionerRole-aubase` | [AU Base PractitionerRole](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-practitionerrole.html) |
| Example FHIR PractitionerRole AU Core | `PractitionerRole-aucore` | [AU Core PractitionerRole](https://build.fhir.org/ig/hl7au/au-fhir-core/StructureDefinition-au-core-practitionerrole.html) |

#### Identifier types
The following Identifier types pertinent for the PractitionerRole resource in an Australian context are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| PractitionerRole-Identifier-Medicare Provider Number | `PractitionerRole-Identifier-MedicareProviderNumber` | [AU Medicare Provider Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-medicareprovidernumber.html) |
| PractitionerRole-Identifier-Employee Number | `PractitionerRole-Identifier-EmployeeNumber` | [AU Employee Number](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-employeenumber.html) |
| PractitionerRole-Identifier-National Provider Identifier At Organisation | `PractitionerRole-Identifier-NationalProviderIdentifierAtOrganisation` | [AU National Provider Identifier At Organisation](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-nationalprovideridentifieratorganisation.html) |

### RelatedPerson
#### Resource flavours
The following flavours of the RelatedPerson resource are supported:

| Snippet Name | Prefix   | Aligns to structure |
| ------------ | -------- | ----------- |
| Example FHIR RelatedPerson core spec | `RelatedPerson-corespec` | [Core R4 RelatedPerson](https://hl7.org/fhir/R4/relatedperson.html) |
| Example FHIR RelatedPerson AU Base | `RelatedPerson-aubase` | [AU Base RelatedPerson](https://hl7.org.au/fhir/4.1.0/StructureDefinition-au-relatedperson.html) |
| Example FHIR RelatedPerson AU Core | `RelatedPerson-aucore` | [AU Core RelatedPerson](https://build.fhir.org/ig/hl7au/au-fhir-core/StructureDefinition-au-core-relatedperson.html) |

#### Identifier types
All of the  Australian context Patient related Identifier types can also be used in RelatedPerson resources. See above.

