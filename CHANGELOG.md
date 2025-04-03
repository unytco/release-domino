# Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.9.1]

### Updated

- ui: persist data on rave transaction models [#111](https://github.com/unytco/piecework/pull/111)

## [0.9.0]

### Updated

- code-template: update to allow updates [#82](https://github.com/unytco/piecework/pull/82)
- exported rave library into a git submodule [#83](https://github.com/unytco/piecework/pull/83)
- exported rave engine into a rust crate [#84](https://github.com/unytco/piecework/pull/84)
- fee-collection: use aggregate spend rave to collect fees [#86](https://github.com/unytco/piecework/pull/86)
- validation: check that fees owed is not higher than the fee trigger amount [#87](https://github.com/unytco/piecework/pull/87)
- update aggregate receive rave to \_\_system_transaction_fee_collection [#88](https://github.com/unytco/piecework/pull/88)
- ui: update code template table to show a dropdown arrow to expand the code template table [#89](https://github.com/unytco/piecework/pull/89)
- ui: add unclaimed balance to the ledger status [#89](https://github.com/unytco/piecework/pull/89)
- ux: add a toggle icon to the pool display to expand the pool display [#90](https://github.com/unytco/piecework/pull/90)
- ui: setup common styles for the interface [#90](https://github.com/unytco/piecework/pull/90)
- export rave instructions from the rave engine crate [#91](https://github.com/unytco/piecework/pull/91)
- create a client for the piecework app called `piecework_cli`
- Executable Agreement: add a new field `title` [#92](https://github.com/unytco/piecework/pull/95)
- ui: Persist Content in Agreement Interaction Modal(s) [#96](https://github.com/unytco/piecework/pull/96)
- ui: add a new field `title` to the Executable Agreement table [#97](https://github.com/unytco/piecework/pull/97)
- validation: credit limit needs to be checked with the appropriate pool definition and if it has expired [#98](https://github.com/unytco/piecework/pull/98)
- ui: rename rave lib to code lib [#100](https://github.com/unytco/piecework/pull/100)
- rename: promise -> spend [#101](https://github.com/unytco/piecework/pull/101)
- rename pool definition variable system_rave_agreement [#102](https://github.com/unytco/piecework/pull/102)
- transaction fees and trigger defined in pool definition [#104](https://github.com/unytco/piecework/pull/104)
- ui: display current applied credit limit for user [#105](https://github.com/unytco/piecework/pull/105)
- rename application to piecework [#106](https://github.com/unytco/piecework/pull/106)
- new swimlane implementation [#107](https://github.com/unytco/piecework/pull/107)
- upgrading a new endpoint to get the current pool definition [#108](https://github.com/unytco/piecework/pull/108)
- update holochain dependencies to use latest versions (v0.4.2) [#109](https://github.com/unytco/piecework/pull/109)
- executable agreements with roles to specify input rules [#110](https://github.com/unytco/piecework/pull/110)

## [0.8.0]

### Updated

- UI: updated to load rave library from rave library dir [#78](https://github.com/unytco/piecework/pull/78)
- RAVE library: added conditional forward and aggregate receive raves [#79](https://github.com/unytco/piecework/pull/79)
- validations: checks the output amount against the spendd amount [#79](https://github.com/unytco/piecework/pull/79)
- RAVE library: conditional forward check units transferred [#80](https://github.com/unytco/piecework/pull/80)
- UI: handles amount sign based on the endpoints used [#81](https://github.com/unytco/piecework/pull/81)

## [0.7.0]

### Updated

- add rhai helper functions for raves [#74](https://github.com/unytco/piecework/pull/74)
- add a Custom RAVE Instructions for inputs [#75](https://github.com/unytco/piecework/pull/75)

## [0.6.1]

### Updated

- ui: network sync checks for pool definition and code templates required to start transactions [#73](https://github.com/unytco/piecework/pull/73)

## [0.6.0]

### Updated

- dna updates for multi unyt support [#65](https://github.com/unytco/piecework/pull/65)
- ui updates for multi unyt support [#66](https://github.com/unytco/piecework/pull/66)
- ui admin portal to setup pool [#67](https://github.com/unytco/piecework/pull/67)
- direct transaction upgraded to support multiple unyts [#68](https://github.com/unytco/piecework/pull/68)
- endpoints to create an invoice auto updates the reference units to be negative [#70](https://github.com/unytco/piecework/pull/70)
- validation: check input and output against code_template schema [#71](https://github.com/unytco/piecework/pull/71)
- validation: check parked_spends unyt_allocation against rave outputs unyt_allocation [#72](https://github.com/unytco/piecework/pull/72)

## [0.5.0]

- broken release due to build issues in the kangaroo repo

## [0.4.0]

### Updated

- Ability to set a optional list of executors to an executable agreement [#50](https://github.com/unytco/piecework/pull/50)
- Ability to create a parked spend for multiple parked invoices [#51](https://github.com/unytco/piecework/pull/51)
- Update Example Code Templates documents [#51](https://github.com/unytco/piecework/pull/51)
- new endpoint to get sorted requests to spend to run aggregate spends [#51](https://github.com/unytco/piecework/pull/51)
- add init script to create templates and agreements in the pool admin tab [#56](https://github.com/unytco/piecework/pull/56)
- update to include all RAVE actions to be triggered from the Executable Agreement Table [#58](https://github.com/unytco/piecework/pull/58)
- add/update validation rules [#61](https://github.com/unytco/piecework/pull/61)
  - code_template: check titles that can only be commited by the progenitor
  - remove the credit_limit_override from the DNA properties and move that logic based on the progenitor existence
  - accept validates ExecutionInstances
  - raves validates its executed code
- compatible with holochain v0.4.1 [#62](https://github.com/unytco/piecework/pull/62)

### Changed/Fixed

- `SendExecutorParkedInvoiceNotification` link to `SendExecutorParkedSpendNotification` [#49](https://github.com/unytco/piecework/pull/49)
- ui code template form reorder inputs boxs [#52](https://github.com/unytco/piecework/pull/52)
- ui upgrades that enables aggregate spends [#52](https://github.com/unytco/piecework/pull/52)
- Ability to execute a rave without a parked spend or parked invoice [#53](https://github.com/unytco/piecework/pull/53)
- bug: notification not showing for the request to spend in raves [#54](https://github.com/unytco/piecework/pull/54)
- update zfuel to 0.2.1 (type updated to u64) [#57](https://github.com/unytco/piecework/pull/57)
- standardization of RAVE outputs [#60](https://github.com/unytco/piecework/pull/60)
- ui: Actionable Transactions table for spends and invoices easier to interact with [#63](https://github.com/unytco/piecework/pull/63)

## [0.3.0]

### Updated

- build process in kangaroo

## [0.2.0]

### Updated

- bump for hashspace

## [0.1.3]

### Changed/Fixed

- credit_limit RAVE expects typo fix `claiming_agent_pubkey` [#46](https://github.com/unytco/piecework/pull/46)
- update admin tab to pool admin and reorder [#47](https://github.com/unytco/piecework/pull/47)
- update swim lane tab to update parent about swim lanes existence [#47](https://github.com/unytco/piecework/pull/47)
- update ui to update counts when tables change [#47](https://github.com/unytco/piecework/pull/47)

## [0.1.2]

### Updated

- update app icons and hc-spin/holochain-client library [#44](https://github.com/unytco/piecework/pull/44)
- Update RAVE flow that removes parked_invoice and parked_spend dependencies on each other [#45](https://github.com/unytco/piecework/pull/45)
- remove parked_invoice_signature from code_template and payload from parked_invoice [#45](https://github.com/unytco/piecework/pull/45)

## [0.1.1]

### Updated

- implemented a credit-limit check for spends and parked-spends [#40](https://github.com/unytco/piecework/pull/40)
- update payment endpoints to check credit and auto apply credit RAVE [#41](https://github.com/unytco/piecework/pull/41)
- parked_invoice: change from Record to Link type && parked_spend uses executor as the target [#42](https://github.com/unytco/piecework/pull/42)
- ui credit_check on accept_transaction while accepting an invoice [#43](https://github.com/unytco/piecework/pull/43)

## [0.1.0]

### Updated

### Changed/Fixed

### Removed
