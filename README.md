# HFvZ Setup

#### links to related docs

- [Test Plan](./testing_docs/1_0_testing_plan.md)
- [HFvZ Setup](./README.md)
- [Phase 1 Testing Details](./testing_docs/1_1_phase_testing_details.md)
- [Intro to RAVEs (Three Layers)](./testing_docs/1_2_three_layers_of_raves.md)
- [Sample Code for Creating RAVEs](./testing_docs/rave_templates)
- [Feedback](https://github.com/orgs/unytco/projects/5/views/1)

# Intro
HFvZ is a Holochain based application for creating agent-centric, peer-to-peer, Mutual Credit accounting systems with smart contract like functionality.

We are working with potential partner projects like yours as we build out this software to ensure that it meets the needs of your team as well as your community of users.

### Overview
This [Test Plan](./testing_docs/1_0_testing_plan.md) document gives a bit of a overview of the sorts of UX / UI feedback that we are seeking at present.

### Installation

Download the appropriate version for your system.

[Windows](https://github.com/unytco/hfvz-releases/releases/download/v0.2.0/co.unyt.hfvz-0.2.0-setup.exe)

[Linux App-Image](https://github.com/unytco/hfvz-releases/releases/download/v0.2.0/co.unyt.hfvz-0.2.0.AppImage)

[Linux Debian](https://github.com/unytco/hfvz-releases/releases/download/v0.2.0/co.unyt.hfvz_0.2.0_amd64.deb)

[Mac Apple Silicon (M1/M2/M3/M4)](https://github.com/unytco/hfvz-releases/releases/download/v0.2.0/co.unyt.hfvz-0.2.0.dmg)

Mac Intel (no release available)

All of those can be found in in the 
[Releases](
https://github.com/unytco/hfvz-releases/releases) section of the [Github Repo for HFvZ](https://github.com/unytco/hfvz-releases/)


### Setup
Note: The release for your operating system may not be code signed yet, so you may need to right click to open the file.

When you open HFvZ on your operating system for the first time, it will create a set of public and private keys for you that you can use to interact with others. These are stored in a private keystore (Lair) on your own machine and are used during future uses. 



### Orientation
HFvZ is software that runs locally on your computer and connects with other instances to form a peer-to-peer network.

During Phase 1, all testers will be joining a single peer network and will be able to send and receive transactions from anyone else in the test network.

For this Phase of testing, you will not need to create a password to log in to your copy of the HFvZ. If you lose your device or delete the software (and your private key), you will lose the ability act as that agent (including the ability to control any test currency that has been sent to you account). (Local) Password login is a feature that we can incorporate in a later release.

Once you have opened HFvZ, you can test out different types of transactions. To start with, in this version, each agent will have a credit limit of 100 units.

All of you will be using the software as a super user with the ability to not only engage in transactions, but to create new RAVEs (smart contract like functionality). Any Code Template, Executable Agreement or RAVE that you create will be visible to other users. 

Clicking on your identicon (on the right side) will copy your public key to the clipboard. You can then share that with others through whatever other medium you have available. 

They will enter it on their own copy of HFvZ when doing things like sending you an invoice (a request for payment) or a promise (a sending of payment) or when choosing you to serve as the executor of a RAVE.

To get started, you will want to install the software on a couple of devices so you can try sending, executing, and receiving transactions. 

Next, dive into the [Test Plan](./testing_docs/1_0_testing_plan.md).




