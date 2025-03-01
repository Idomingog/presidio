# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]
### Changed
#### Analyzer:
* Fixed issue when IBAN followed by all caps can't be recognized

### Removed

### Deprecated

## [2.2.23] - 16.11.2021
### Changed
#### Analyzer:
* Added multi-regional phone number recognizer.
* Fixed duplicated entities removal.
* Added sample for structured / semi-structured data in batch.
* Dependencies version bumps.

#### Anonymizer:
* Added sample for getting an identified entity value using a custom Operator.
* Changed packages/imports .
* Added repr to classes.
* Added encryption and decryption samples.
* Remove AnonymizerResult in favor of OperatorResult, for an easier anonymization-deanonymization.
* Anonymizaer and Deanonymizaer to return `operator_name` instead of `operator` in OperatorResult.

## [2.2.2] - 09.06.2021
### Changed
#### Analyzer:
* Databricks based template in Azure Data Factory docs
* Adding ORGANIZATION recognizer docs
* Bumped pydantic from 1.7.3 to 1.7.4
* Updated call to stanza via spacy-stanza
* Added DATE_TIME recognizer
* Added Medical Licence recognizer
* Bumped spacy from 3.0.5 to 3.0.6

## [2.2.1] - 10.05.2021
### Changed
#### Analyzer:
* Create CODE_OF_CONDUCT
* ADF templates docs
* Fix spark sample to run presidio in broadcast
* Ad-hoc recognizers
* Text Analytics Integration Sample
* Documentation update and samples validation
* Adding tagger to the spaCy model pipeline
* Sample notebook for remote recognizer (using Text Analytics)
* Add matplotlib to image-redactor
* Added custom lambda anonymizer
* Added add pii_verify_engine to the image-redactor


## [2.2.0] - 12.04.2021
### Changed
#### Analyzer:
Upgrade Analyzer spacy version to 3.0.5

#### Anonymizer Engine:
1. Request entity AnonymizerConfig renamed OperatorConfig
    - In OperatorConfig: anonymizer_name -> operator_name
2. Response entity AnonymizerResult renamed to EngineResult
    - In EngineResult: List[AnonymizedEntity] -> List[OperatorResult]
    - In OperatorResult: 
        - anonymizer -> operator
        - anonymized_text -> text

#### Anonymize API:
1. Response entity anonymizer renamed to operator.
2. Response entity anonymizer_text renamed to text.

#### Deanonymize:
New endpoint for deanonymizing encrypted entities by the anonymizer.

[unreleased]: https://github.com/microsoft/presidio/compare/2.2.23...HEAD
[2.2.23]: https://github.com/microsoft/presidio/compare/2.2.2...2.2.23
[2.2.2]: https://github.com/microsoft/presidio/compare/2.2.1...2.2.2
[2.2.1]: https://github.com/microsoft/presidio/compare/2.2.0...2.2.1
