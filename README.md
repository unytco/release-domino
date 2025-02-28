# HFvZ Releases
![GitHub release (latest by date)](https://img.shields.io/github/v/release/unytco/hfvz-releases?style=for-the-badge)
![GitHub All Releases](https://img.shields.io/github/downloads/unytco/hfvz-releases/total?style=for-the-badge)


## Related docs
- [Test Plan](./testing_docs/1_0_testing_plan.md)
    - [Phase 1 Testing Details](./testing_docs/1_1_phase_testing_details.md)
- [How to install HFvZ app?](./README.md)
- [Intro to RAVEs (Three Layers)](./testing_docs/1_2_three_layers_of_raves.md)
- [Sample Code for Creating RAVEs](./testing_docs/rave_templates)
- [Feedback Board](https://github.com/orgs/unytco/projects/5/views/1)

## Intro
HFvZ is a Holochain based application for creating agent-centric, peer-to-peer, Mutual Credit accounting systems with smart contract like functionality.

We are working with potential partner projects like yours as we build out this software to ensure that it meets the needs of your team as well as your community of users.

## Overview
This [Test Plan](./testing_docs/1_0_testing_plan.md) document gives a bit of a overview of the sorts of UX / UI feedback that we are seeking at present.

## Installation

Download the appropriate version for your system.



| Releases    | 
| --------    | 
|    [macOS x84 (intel)](https://github.com/unytco/hfvz-releases/releases/download/v0.7.0/co.unyt.hfvz-0.7.0-x64.dmg)  |
|    [macOS arm64 (silicon)](https://github.com/unytco/hfvz-releases/releases/download/v0.7.0/co.unyt.hfvz-0.7.0-arm64.dmg.blockmap)    |
|    [Linux Debian](https://github.com/unytco/hfvz-releases/releases/download/v0.7.0/co.unyt.hfvz_0.7.0_amd64.deb)  (recomended)  | 
|    [Linux AppImage](https://github.com/unytco/hfvz-releases/releases/download/v0.7.0/co.unyt.hfvz-0.7.0.AppImage)   (read note below) | 
|    [Windows](https://github.com/unytco/hfvz-releases/releases/download/v0.7.0/co.unyt.hfvz-0.7.0-setup.exe)    | 
|    [Android]() (no release available)    |
|    [iOS]() (no release available)    |


> [!IMPORTANT]
> If you encounter sandbox-related issues, you can try running the AppImage with:
> ```bash
> ELECTRON_DISABLE_SANDBOX=1 ./hfvz.AppImage
> ```
> This is automatically configured in the latest version, but might be needed for manual execution in some cases.


All available versions can be found in the [Releases](
https://github.com/unytco/hfvz-releases/releases)

## Setup
Note: The release for your operating system may not be code signed yet, so you may need to right click to open the file.

When you open HFvZ on your operating system for the first time, it will create a set of public and private keys for you that you can use to interact with others. These are stored in a private keystore (Lair) on your own machine and are used during future uses. 

To get started, you will want to install the software on a couple of devices so you can try sending, executing, and receiving transactions. 

Next, dive into the [Test Plan](./testing_docs/1_0_testing_plan.md).


## License

[![License: CAL 1.0](https://img.shields.io/badge/License-CAL%201.0-blue.svg)](https://github.com/holochain/cryptographic-autonomy-license)

Copyright (C) 2024 - 2025, unyt.co
