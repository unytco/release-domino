# Intro to Smart Agreements

#### links to related docs

- [Test Plan](./1_0_testing_plan.md)
- [HFvZ Setup](../README.md)
- [Testing Documentation, Phase 3](./3_0_phase_3_testing_details.md)
- [Domino Dictionary](./domino-dictionary.md)
- [Intro to RAVEs (Three Layers)](./1_2_three_layers_of_raves.md)
- [RAVE Library Repo](https://github.com/unytco/rave_library)
- [Feedback](https://github.com/orgs/unytco/projects/5/views/1)

## Agent Centric Smart Agreements

Smart Agreements are the closest thing in Domino's Agent Centric architecture to Blockchain-based Smart Contracts, though they rest upon a different architecture of cryptographic mechanisms as well as a different social physics, namely that content authored by an agent is stored in a structure (a hash chain) that establishes the order of that particular agent's actions. These actions and their ordering are then validated by a deterministic, but random group of other agents participating in that Domino Accounting Alliance application. Each Agent has their own hash chain (we call it a source chain), that stores the actions they have taken, in the order that they took it, from their own perspective. Each action includes a reference to the action that immediately preceded it.

## Why Agent Centric

So what? Einstein understood 120 years ago that there was no such thing as a global ordering of events. This was a key component of his theory of special relativity.

Well, whereas blockchains resort to various mechanisms to generate a social agreement about a global ordering of events, Domino instead makes use of Holochain's agent-centric ordering of events paradigm, and layers validation rules on top of that in situations where some social agreement about the ordering of events across multiple agents is desirable. You could think of that as enabling the creation of agreement about the ordering of particular sets of events (consensus about the order of those events relative to one another) but tuneable for the specific contexts faced by -- and needs of -- the community rather than resorting to a one-size-fits-all "global consensus" approach.

## Benefits

This unique agent-centric foundation provides Domino Smart Agreements with some features and affordances that are unavailable to blockchain based, or server based architectures. These include:

- parallel action taking and distributed transaction processing,
- reduced duplicative computational work,
- improvements in resource efficiency,
- which enables the software to run on ordinary hardware with lower bandwidth consumption,
- empowering a broader base of participants to participate (not just those who can afford to buy and maintain specialized equipment), and
- reductions in transaction fees relative to other systems.
- It also unlocks support for offline transactions in certain contexts.

## Mechanics of Smart Agreements

A Smart Agreement is simply code (i.e. text) and references to other code that defines how a particular set of inputs will be transformed into a set of outputs, where those inputs will come from, and who is authorized to perform an execution (i.e. a transformation of a particular set of inputs into outputs -- in accordance with the execution code and other agreement rules).

## SAVED: A Record of Verifiable Execution

An Execution of the Smart Agreement generates a Record, or Documentation of the Execution. This Execution Document can be examined by any other Alliance member, who can verify that it has been executed validly. Consequently, we describe the resulting Record of Execution as a "Smart Agreement, Verifiably Executed and Documented" or SAVED. So even though a particular party performed the execution, any party can independently verify that the execution was done appropriately.

A SAVED is produced after an Execution of a Smart Agreement.  It is the primary artifact resulting from that Execution, and is published by its author, the Executor, into the shared space of the Domino Accounting Alliance for a group of peers to validate, store and serve, and for any peer to reference and rely upon.

Not all Smart Agreements involve Spending and Allocating Fuel Credits.  However, Spending and Allocating Fuel Credits to some Receiver in accordance with some particular custom logic is a very common way to use Smart Agreements. After the Execution of such a Smart Agreement, the SAVED will allocate Fuel Credits to the appropriate Receiver (or Receivers). However, that Receiver will still need to Accept the Fuel Credits before their account will be credited.

This is interesting in that, the Execution is complete, the Fuel Credits have been allocated, but the Receiver themselves has to exercise their agency and choose whether to receive the credits. When they do Accept, their device also performs an independent check of the validity of the transaction. If the transaction is invalid, their device will reject the transaction. If it is valid, their device will cryptographically sign the Acceptance of the transaction.

Others aren't able to force credits onto you that you don't wish to accept. And others that attempt to commit fraud on your behalf require your collusion -- and your taking of responsibility as well.

Such activity would quickly get both them and you kicked out of the application by peers, who one-by-one, would turn away from you automatically, for having violated the rules of the Accounting Alliance.