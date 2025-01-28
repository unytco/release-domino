# Test Plan 

#### links to other documents

[Test Plan](https://hackmd.io/blgzLSsQTeOMLcmXcfkU0A?edit)
[HFvZ Setup](https://hackmd.io/sTH9kh57Qwu32ceYkkH-YQ)
[Phase 1 Testing Details](https://hackmd.io/-SoiQbJ-SqGOGm_U0tzQSw)
[Intro to RAVEs (Three Layers)](https://hackmd.io/UValSJqhRA-7PQStI3_Nvg?view)
[Sample Code for Creating RAVEs](https://github.com/unytco/hfvz/tree/develop/docs/rave_templates)
[Feedback](https://github.com/orgs/unytco/projects/5/views/1)

#### Test Plan Phase 1: Basic Features, UI/UX Feedback
1. Why we are asking Partners to do testing
2. Test Plan
3. Feedback

### 1. Why we are asking Partners to do testing: 

Unyt Co tools are all built with automated unit testing and reliability testing, and Holochain is continually expanding their performance testing. So we’re not seeking functional testing, but we are looking for feedback about:

*  UX and UI usability for what could be a complex or confusing process for end-users and/or project administrators. 
* Configurability to the needs and functions of your project. We have gone from HoloFuel as a single-function currency, to one that must be able to function in a variety of ways. We need to make sure it functions how you need it to, because we can’t predict all those variants.
* White Label / Branding dynamics: We expect projects to customize some of the appearance of the interfaces to match their branding and we want to make sure we’ve made that work for your project.
* Value Workflow: You need to make sure the complete value flows work for your customers and service providers. 

Some questions you should consider: Do your customers have an appropriate way in? (They may already need to hold your token to buy internal units.) Do your service providers have a sensible way to prove the value they’re providing? Do they have a clear way to cash out of the internal units to your token? Are there any other value transfers needed, if so, can those be completed reasonably easily?
* Administrative Workflow questions to ask yourself: Do your technical people understand how to update your configuration? Can they do so successfully? What high level reports do you need to be able to see?

### 2. Test Plan

Phase 1: Basic Features & UI/UX Feedback
Start: January 29, 2025
Duration: 2-3 weeks

Test usability of the full range of basic transactional functionality

- [ ] set up new users / accounts (3?)
- [ ] send/receive via normal transactions, including credit limit enforcement and deduction of transaction fees
- [ ] send/receive via RAVEs, including credit limit enforcement and deduction of transaction fees
- [ ] Use conditional logic RAVEs (e.g. conditional forward / non-custodial escrow)


### 3. Feedback
We have set up this [feedback board](https://github.com/orgs/unytco/projects/5) for adding and tracking bugs, feature requests and other feedback.
