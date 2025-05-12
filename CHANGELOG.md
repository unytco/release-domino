# Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.13.0]

### Added

- New common `Transaction` type for improved UI experience and consistency [#129](https://github.com/unytco/domino/pull/129)
  - Introduces standardized transaction states: pending, actionable, and completed
  - Replaces multiple transaction types with a unified interface
- DNA: agent_details for managing personal address book [#130](https://github.com/unytco/domino/pull/130)

### Changed

- Updated API endpoints to use the common `Transaction` type: [#129](https://github.com/unytco/domino/pull/129)
  - `get_sorted_requests_to_spend`: Now returns `Vec<Vec<Transaction>>`
  - `accept_paying_parked_invoice`: Now uses `AcceptPayingInvoices` type
  - `get_requests_to_execute_agreements`: Now uses `ExecutionRequests` type
  - `get_parked_spend`: Now returns `Vec<Transaction>`
  - `get_parked_links`: Now returns `Vec<Transaction>`
  - `get_incoming_raves`: Now returns `Vec<Transaction>`
  - `collect_from_rave`: Now returns `Transaction`
  - `get_all_my_executed_raves`: Now returns `Vec<Transaction>`
- Updated Language only on dev-ui [#132](https://github.com/unytco/domino/pull/132)

### Deprecated

- `RAVEToCollect` type is deprecated in favor of the common `Transaction` type [#129](https://github.com/unytco/domino/pull/129)

### Updated

- ActionTable component for improved transaction management [#129](https://github.com/unytco/domino/pull/129)

## [0.12.0]

### Updated

- Defined common `Transaction` type for all actions[#124](https://github.com/unytco/domino/pull/124)
- Documentation of zome calls[#124](https://github.com/unytco/domino/pull/124)
- Testing: improved tests for credit checks [#125](https://github.com/unytco/domino/pull/125)
- Added possible_actions to the `Transaction` type [#126](https://github.com/unytco/domino/pull/126)
- Testing: improved tests for fees dropoff and collections [#127](https://github.com/unytco/domino/pull/127)
- ui: bug fix on the parked spend form to parse the payload [#128](https://github.com/unytco/domino/pull/127)
- ui: updated interact as button to show descriptions

## [0.11.0]

### Updated

- validation: reviewed validation for links [#118](https://github.com/unytco/domino/pull/118)
- validation: credit check for sales-agent [#118](https://github.com/unytco/domino/pull/118)
- create link from EA to RAVE to collect all the RAVE's that were executed for a EA [#118](https://github.com/unytco/domino/pull/118)
- UI: create custom conversion sheets [#119](https://github.com/unytco/domino/pull/119)
- upgraded UI workspace to maintain multiple UI skins [#121](https://github.com/unytco/domino/pull/121)
- improved rave_engine with tests [#123](https://github.com/unytco/domino/pull/123)

## [0.10.0]

### Updated

- revisiting validations [#112](https://github.com/unytco/domino/pull/112)
- default role_name is always set to lower-case and ui displays as pascal case [#113](https://github.com/unytco/domino/pull/113)
- ui: rave action buttons do not expect an executor if it already provided, and executor button does not show up if you are not the executor [#113](https://github.com/unytco/domino/pull/113)
- data blob: ability to add a record that could be used to reference as an input in the RAVE[#114](https://github.com/unytco/domino/pull/114)
- validate `_lane` RAVE's based on the swim-lane rules [#115](https://github.com/unytco/domino/pull/115)
- ui: clone and edit executable agreement [#115](https://github.com/unytco/domino/pull/115)
- sales-agent: specific endpoints for purchase and redemption [#115](https://github.com/unytco/domino/pull/115)
- ui: use custom sales-agent endpoints [#115](https://github.com/unytco/domino/pull/115)
- documentation: added new architecture docs for purchase and redemption [#115](https://github.com/unytco/domino/pull/115)

### Removed

- removed service_fees RAVE from SLRaveAgreements [#114](https://github.com/unytco/domino/pull/114)

## [0.9.1]

### Updated

- ui: persist data on rave transaction models [#111](https://github.com/unytco/domino/pull/111)

## [0.9.0]

### Updated

- code-template: update to allow updates [#82](https://github.com/unytco/domino/pull/82)
- exported rave library into a git submodule [#83](https://github.com/unytco/domino/pull/83)
- exported rave engine into a rust crate [#84](https://github.com/unytco/domino/pull/84)
- fee-collection: use aggregate spend rave to collect fees [#86](https://github.com/unytco/domino/pull/86)
- validation: check that fees owed is not higher than the fee trigger amount [#87](https://github.com/unytco/domino/pull/87)
- update aggregate receive rave to \_\_system_transaction_fee_collection [#88](https://github.com/unytco/domino/pull/88)
- ui: update code template table to show a dropdown arrow to expand the code template table [#89](https://github.com/unytco/domino/pull/89)
- ui: add unclaimed balance to the ledger status [#89](https://github.com/unytco/domino/pull/89)
- ux: add a toggle icon to the pool display to expand the pool display [#90](https://github.com/unytco/domino/pull/90)
- ui: setup common styles for the interface [#90](https://github.com/unytco/domino/pull/90)
- export rave instructions from the rave engine crate [#91](https://github.com/unytco/domino/pull/91)
- create a client for the domino app called `piecework_cli`
- Executable Agreement: add a new field `title` [#92](https://github.com/unytco/domino/pull/95)
- ui: Persist Content in Agreement Interaction Modal(s) [#96](https://github.com/unytco/domino/pull/96)
- ui: add a new field `title` to the Executable Agreement table [#97](https://github.com/unytco/domino/pull/97)
- validation: credit limit needs to be checked with the appropriate pool definition and if it has expired [#98](https://github.com/unytco/domino/pull/98)
- ui: rename rave lib to code lib [#100](https://github.com/unytco/domino/pull/100)
- rename: promise -> spend [#101](https://github.com/unytco/domino/pull/101)
- rename pool definition variable system_rave_agreement [#102](https://github.com/unytco/domino/pull/102)
- transaction fees and trigger defined in pool definition [#104](https://github.com/unytco/domino/pull/104)
- ui: display current applied credit limit for user [#105](https://github.com/unytco/domino/pull/105)
- rename application to domino [#106](https://github.com/unytco/domino/pull/106)
- new swimlane implementation [#107](https://github.com/unytco/domino/pull/107)
- upgrading a new endpoint to get the current pool definition [#108](https://github.com/unytco/domino/pull/108)
- update holochain dependencies to use latest versions (v0.4.2) [#109](https://github.com/unytco/domino/pull/109)
- executable agreements with roles to specify input rules [#110](https://github.com/unytco/domino/pull/110)

## [0.8.0]

### Updated

- UI: updated to load rave library from rave library dir [#78](https://github.com/unytco/domino/pull/78)
- RAVE library: added conditional forward and aggregate receive raves [#79](https://github.com/unytco/domino/pull/79)
- validations: checks the output amount against the spendd amount [#79](https://github.com/unytco/domino/pull/79)
- RAVE library: conditional forward check units transferred [#80](https://github.com/unytco/domino/pull/80)
- UI: handles amount sign based on the endpoints used [#81](https://github.com/unytco/domino/pull/81)

## [0.7.0]

### Updated

- add rhai helper functions for raves [#74](https://github.com/unytco/domino/pull/74)
- add a Custom RAVE Instructions for inputs [#75](https://github.com/unytco/domino/pull/75)

## [0.6.1]

### Updated

- ui: network sync checks for pool definition and code templates required to start transactions [#73](https://github.com/unytco/domino/pull/73)

## [0.6.0]

### Updated

- dna updates for multi unyt support [#65](https://github.com/unytco/domino/pull/65)
- ui updates for multi unyt support [#66](https://github.com/unytco/domino/pull/66)
- ui admin portal to setup pool [#67](https://github.com/unytco/domino/pull/67)
- direct transaction upgraded to support multiple unyts [#68](https://github.com/unytco/domino/pull/68)
- endpoints to create an invoice auto updates the reference units to be negative [#70](https://github.com/unytco/domino/pull/70)
- validation: check input and output against code_template schema [#71](https://github.com/unytco/domino/pull/71)
- validation: check parked_spends unyt_allocation against rave outputs unyt_allocation [#72](https://github.com/unytco/domino/pull/72)

## [0.5.0]

- broken release due to build issues in the kangaroo repo

## [0.4.0]

### Updated

- Ability to set a optional list of executors to an executable agreement [#50](https://github.com/unytco/domino/pull/50)
- Ability to create a parked spend for multiple parked invoices [#51](https://github.com/unytco/domino/pull/51)
- Update Example Code Templates documents [#51](https://github.com/unytco/domino/pull/51)
- new endpoint to get sorted requests to spend to run aggregate spends [#51](https://github.com/unytco/domino/pull/51)
- add init script to create templates and agreements in the pool admin tab [#56](https://github.com/unytco/domino/pull/56)
- update to include all RAVE actions to be triggered from the Executable Agreement Table [#58](https://github.com/unytco/domino/pull/58)
- add/update validation rules [#61](https://github.com/unytco/domino/pull/61)
  - code_template: check titles that can only be commited by the progenitor
  - remove the credit_limit_override from the DNA properties and move that logic based on the progenitor existence
  - accept validates ExecutionInstances
  - raves validates its executed code
- compatible with holochain v0.4.1 [#62](https://github.com/unytco/domino/pull/62)

### Changed/Fixed

- `SendExecutorParkedInvoiceNotification` link to `SendExecutorParkedSpendNotification` [#49](https://github.com/unytco/domino/pull/49)
- ui code template form reorder inputs boxs [#52](https://github.com/unytco/domino/pull/52)
- ui upgrades that enables aggregate spends [#52](https://github.com/unytco/domino/pull/52)
- Ability to execute a rave without a parked spend or parked invoice [#53](https://github.com/unytco/domino/pull/53)
- bug: notification not showing for the request to spend in raves [#54](https://github.com/unytco/domino/pull/54)
- update zfuel to 0.2.1 (type updated to u64) [#57](https://github.com/unytco/domino/pull/57)
- standardization of RAVE outputs [#60](https://github.com/unytco/domino/pull/60)
- ui: Actionable Transactions table for spends and invoices easier to interact with [#63](https://github.com/unytco/domino/pull/63)

## [0.3.0]

### Updated

- build process in kangaroo

## [0.2.0]

### Updated

- bump for hashspace

## [0.1.3]

### Changed/Fixed

- credit_limit RAVE expects typo fix `claiming_agent_pubkey` [#46](https://github.com/unytco/domino/pull/46)
- update admin tab to pool admin and reorder [#47](https://github.com/unytco/domino/pull/47)
- update swim lane tab to update parent about swim lanes existence [#47](https://github.com/unytco/domino/pull/47)
- update ui to update counts when tables change [#47](https://github.com/unytco/domino/pull/47)

## [0.1.2]

### Updated

- update app icons and hc-spin/holochain-client library [#44](https://github.com/unytco/domino/pull/44)
- Update RAVE flow that removes parked_invoice and parked_spend dependencies on each other [#45](https://github.com/unytco/domino/pull/45)
- remove parked_invoice_signature from code_template and payload from parked_invoice [#45](https://github.com/unytco/domino/pull/45)

## [0.1.1]

### Updated

- implemented a credit-limit check for spends and parked-spends [#40](https://github.com/unytco/domino/pull/40)
- update payment endpoints to check credit and auto apply credit RAVE [#41](https://github.com/unytco/domino/pull/41)
- parked_invoice: change from Record to Link type && parked_spend uses executor as the target [#42](https://github.com/unytco/domino/pull/42)
- ui credit_check on accept_transaction while accepting an invoice [#43](https://github.com/unytco/domino/pull/43)

## [0.1.0]

### Updated

### Changed/Fixed

### Removed
