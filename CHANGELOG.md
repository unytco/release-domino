# Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Released

## [0.7.0]

### Updated

- add rhai helper functions for raves [#74](https://github.com/unytco/hfvz/pull/74)
- add a Custom RAVE Instructions for inputs [#75](https://github.com/unytco/hfvz/pull/75)

## [0.6.1]

### Updated

- ui: network sync checks for pool definition and code templates required to start transactions [#73](https://github.com/unytco/hfvz/pull/73)

## [0.6.0]

### Updated

- dna updates for multi unyt support [#65](https://github.com/unytco/hfvz/pull/65)
- ui updates for multi unyt support [#66](https://github.com/unytco/hfvz/pull/66)
- ui admin portal to setup pool [#67](https://github.com/unytco/hfvz/pull/67)
- direct transaction upgraded to support multiple unyts [#68](https://github.com/unytco/hfvz/pull/68)
- endpoints to create an invoice auto updates the reference units to be negative [#70](https://github.com/unytco/hfvz/pull/70)
- validation: check input and output against code_template schema [#71](https://github.com/unytco/hfvz/pull/71)
- validation: check parked_promises unyt_allocation against rave outputs unyt_allocation [#72](https://github.com/unytco/hfvz/pull/72)

## [0.5.0]

- broken release due to build issues in the kangaroo repo

## [0.4.0]

### Updated

- Ability to set a optional list of executors to an executable agreement [#50](https://github.com/unytco/hfvz/pull/50)
- Ability to create a parked promise for multiple parked invoices [#51](https://github.com/unytco/hfvz/pull/51)
- Update Example Code Templates documents [#51](https://github.com/unytco/hfvz/pull/51)
- new endpoint to get sorted requests to spend to run aggregate spends [#51](https://github.com/unytco/hfvz/pull/51)
- add init script to create templates and agreements in the pool admin tab [#56](https://github.com/unytco/hfvz/pull/56)
- update to include all RAVE actions to be triggered from the Executable Agreement Table [#58](https://github.com/unytco/hfvz/pull/58)
- add/update validation rules [#61](https://github.com/unytco/hfvz/pull/61)
  - code_template: check titles that can only be commited by the progenitor
  - remove the credit_limit_override from the DNA properties and move that logic based on the progenitor existence
  - accept validates ExecutionInstances
  - raves validates its executed code
- compatible with holochain v0.4.1 [#62](https://github.com/unytco/hfvz/pull/62)

### Changed/Fixed

- `SendExecutorParkedInvoiceNotification` link to `SendExecutorParkedPromiseNotification` [#49](https://github.com/unytco/hfvz/pull/49)
- ui code template form reorder inputs boxs [#52](https://github.com/unytco/hfvz/pull/52)
- ui upgrades that enables aggregate spends [#52](https://github.com/unytco/hfvz/pull/52)
- Ability to execute a rave without a parked promise or parked invoice [#53](https://github.com/unytco/hfvz/pull/53)
- bug: notification not showing for the request to spend in raves [#54](https://github.com/unytco/hfvz/pull/54)
- update zfuel to 0.2.1 (type updated to u64) [#57](https://github.com/unytco/hfvz/pull/57)
- standardization of RAVE outputs [#60](https://github.com/unytco/hfvz/pull/60)
- ui: Actionable Transactions table for promises and invoices easier to interact with [#63](https://github.com/unytco/hfvz/pull/63)

## [0.3.0]

### Updated

- build process in kangaroo

## [0.2.0]

### Updated

- bump for hashspace

## [0.1.3]

### Changed/Fixed

- credit_limit RAVE expects typo fix `claiming_agent_pubkey` [#46](https://github.com/unytco/hfvz/pull/46)
- update admin tab to pool admin and reorder [#47](https://github.com/unytco/hfvz/pull/47)
- update swim lane tab to update parent about swim lanes existence [#47](https://github.com/unytco/hfvz/pull/47)
- update ui to update counts when tables change [#47](https://github.com/unytco/hfvz/pull/47)

## [0.1.2]

### Updated

- update app icons and hc-spin/holochain-client library [#44](https://github.com/unytco/hfvz/pull/44)
- Update RAVE flow that removes parked_invoice and parked_promise dependencies on each other [#45](https://github.com/unytco/hfvz/pull/45)
- remove parked_invoice_signature from code_template and payload from parked_invoice [#45](https://github.com/unytco/hfvz/pull/45)

## [0.1.1]

### Updated

- implemented a credit-limit check for promises and parked-promises [#40](https://github.com/unytco/hfvz/pull/40)
- update payment endpoints to check credit and auto apply credit RAVE [#41](https://github.com/unytco/hfvz/pull/41)
- parked_invoice: change from Record to Link type && parked_promise uses executor as the target [#42](https://github.com/unytco/hfvz/pull/42)
- ui credit_check on accept_transaction while accepting an invoice [#43](https://github.com/unytco/hfvz/pull/43)

## [0.1.0]

### Updated

### Changed/Fixed

### Removed
