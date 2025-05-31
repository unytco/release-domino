# Domino Dictionary

#### links to related docs

- [Test Plan](./1_0_testing_plan.md)
- [Domino Setup](../README.md)
- [Testing Documentation, Phase 3](./3_0_phase_3_testing_details.md)
- [Domino Dictionary](./3_2_domino-dictionary.md)
- [Intro to Smart Agreements (Three Layers)](./3_1_intro_to_smart_agreements.md)
- [Templates and Smart Agreements Library Repo](https://github.com/unytco/rave_library)
- [Feedback](https://github.com/orgs/unytco/projects/5/views/1)

## A glossary of terms related to Domino

**Action Table**
: Displays in-process transactions that are Actionable (requiring your action) or Pending (awaiting another's action).

**Accept**
: The action taken by a Receiver to formally acknowledge and receive Fuel Credits or Service Units into their account balance.

**Agent**
: A participant's identifier in a Domino Alliance, represented by a public/private key pair, used for all interactions and transactions.

**Agreement Code Template (Template)**
: Defines core reusable logic for Smart Agreements, including input/output schemas and execution code.

**Code Sheet (Data Record)**
: A flexible Data Record for custom logic, price sheets, or other publishable data referenced by participants.

**Compute Transaction Fee Agreement**
: A System Agreement within the Global Configuration that determines how Transaction Fees are calculated and their payment threshold.

**Conversion Table (Data Record)**
: A Data Record defining a fixed price by equating a number of Service Units to 1 Fuel Credit.

**Credit Limit**
: The amount below zero an Agent can spend in Fuel Credits, determined by the System Credit Limit Computation agreement in their Domino Alliance.

**Data Records**
: Stored content (e.g., Conversion Table, Recipe, Code Sheet) referenced by Smart Agreements, often for service pricing.

**DePIN (Decentralized Physical Infrastructure Networks)**
: Networks Domino primarily supports, focusing on high-volume, low-cost transactions for real-world services.

**DMNO (Decentralized Microtransaction Network Orchestration)**
: An acronym that the name Domino is derived from, representing its function in orchestrating decentralized microtransactions amongst members of a peer-to-peer network.

**Domino**
: Decentralized software for microtransaction accounting, enabling communities to run their own peer-to-peer Domino Accounting Alliances.

**Domino Accounting Alliance (Domino Alliance)**
: A community running its own custom instance of Domino, with its own rules, Fuel Credit Unit, and Smart Agreements.

**Executor**
: An Agent authorized to perform the execution of a Smart Agreement, transforming its inputs into outputs according to its defined rules.

**Fee Percentage**
: The percentage rate charged as a Transaction Fee on Spend transactions, defined in the Global Configuration.

**Fee Trigger**
: The threshold defined in the Global Configuration prior to which accumulated Transaction Fees must be paid.

**Fees Owed**
: Transaction Fees that have accrued from an Agent's activities but have not yet been paid.

**Fuel Credit**
: The generic term for the primary, internal payment unit of account within a Domino Alliance. Each Domino Alliance will choose a name for their communities own Fuel Credit.

**Global Config**
: The overall ruleset, including System Agreements, governing a Domino Alliance for a specific Global Configuration Window.

**Global Config Window**
: The specific period during which a particular Global Configuration is active and its rules are in effect.

**Identicon**
: A unique, colorful visual image generated from an Agent's public key to help in recognizing and differentiating Agents.

**Invoice**
: A request for Fuel Credits sent from one Agent to another Agent.

**Ledger Details**
: A modal in the interface showing an Agent's Fuel Credits Balance, Fees Owed, Unclaimed credits, and Credit Limit.

**Library (Templates and Agreements Library)**
: A central repository within Domino where participants in that Domino Alliance can create, find, and interact with Agreement Code Templates and Smart Agreements.

**Parked (Transaction Type)**
: A transaction status indicating a submission of content (e.g. an invoice, attestation) to a Smart Agreement.

**ParkedSpend (Transaction Type)**
: A transaction representing the sending of Fuel Credits by a Spender directly to a Smart Agreement.

**Pay**
: The action taken by a Spender to send Fuel Credits, sometimes of thier own initiative, sometimes in response to an Invoice, and other times as a way of interacting with a Smart Agreement.

**Proof of Service Agreement (Service Network)**
: A Smart Agreement used within a Service Network for Service Providers to prove that services have been rendered and for Payors to Park Spends as payment for such services.

**Purchase Agreement (Service Network)**
: A Smart Agreement governing the purchase of Fuel Credits from a particular Service Network within that Domino Alliance, with payment in that Service Network's Outside Currency.

**Recipe (Data Record)**
: A Data Record defining a "basket of goods" where 1 Fuel Credit equates to a bundle of one or more Service Units in specified quantities.

**Receiver**
: An Agent designated to receive Fuel Credits or Service Units in a transaction or as an outcome of a Smart Agreement.

**Redemption Agreement (Service Network)**
: A Smart Agreement governing the redemption of Fuel Credits by a Service Network's Service Providers, redeeming into that Service Network's Outside Currency. 

**Redemption Fee**
: Not explicitly defined as a standard system-wide fee. Any such fees are to be defined by a Service Network's custom Redemption Agreement logic or pricing structure.

**Role (in Smart Agreement)**
: Defines a class of Agents (e.g., "Vendor," "Customer") and grants specific authorizations for interacting with a Smart Agreement.

**Sales Agent (in Service Network)**
: An Agent authorized within a Service Network to manage the sale of Fuel Credits for an Outside Currency and process redemptions.

**SAVED (Smart Agreement Verifiable Execution Doc)**
: The immutable documentation resulting from the valid execution of a Smart Agreement by an Executor, published for verification. Any application participant can validate that the Smart Agreement was executed appropriately.

**Service Fee**
: A charge that can be levied for services rendered or transactions processed. Can be defined within Smart Agreements.

**Service Network**
: An organization within a Domino Alliance, set up by that Alliances Global Admin, that defines its own configuration, services, and typically uses specific Smart Agreements for its operations. 

**Service Network Console** (Previously Update Service-Network Properties. UI update in progress.)
: The current name for the admin interface where a Service Network Administrator defines and stewards a Service Network's Configuration.

**Service Network Admin** (Previously Lane Editor(s). UI update in progress.)
: An Agent authorized by the Global Admin to manage and make changes to a specific Service Network's Configuration.

**Service Network Config** (Previously Update Service-Network Details. UI update in progress.)
: The specific ruleset for a Service Network, effective for a defined period, governing interactions with its associated Smart Agreements.

**Service Units**
: Quantifiable units, distinct from Fuel Credits, used for tracking specific forms of service provision within a Domino Alliance. An agents balance in a particular Service Unit will typically move in the opposite direction (up / down) of the Fuel Credits involved in that same transaction, if it changes at all.

**Smart Agreements**
: Customizable, agent-centric programs in Domino that define rules and logic for interactions and transactions, an alternative to blockchain smart contracts.

**Spend**
: The action of an Agent sending Fuel Credits to another Agent or to a Smart Agreement.

**Spender**
: An Agent that authorizes a transaction that involves debiting Fuel Credits from their account, such as a direct Spend or payment via a Smart Agreement.

**System Agreements**
: Core agreements defined within the Global Configuration of a Domino Alliance, such as the Compute Credit Limit Agreement and Compute Transaction Fee Agreement.

**Transaction Fee**
: A fee, typically a percentage, charged by a Domino Alliance when Fuel Credits are spent, as defined in its Global Configuration.

**Unclaimed (Credits)**
: Fuel Credits that have been allocated or sent to an Agent but have not yet been formally accepted by them into their balance.