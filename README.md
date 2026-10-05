# Creator Assertions Working Group :: Trust Framework (pre-draft)

This repository contains a **pre-draft proposal** for the CAWG Trust Framework: the baseline requirements and designation criteria by which CAWG recognises external trust governance partners for [identity assertions](https://cawg.io/identity/).

It is intended as input to the CAWG 2.0 work on baseline requirements and designation criteria, planned for late November to December 2026.

> **Status:** Working proposal. Nothing here has been adopted by CAWG. The repository name `cawg-trust-list` is provisional and predates the move to a trust framework model.

## The model

* **Two layers.** CAWG sets the framework and baseline requirements and decides which partners qualify (designation). External organisations operate trust lists, registries, conformance programs and industry-specific validation. CAWG does not operate registries, CAs or conformance programs.
* **Identity and role are separate.** Credential issuers attest *who you are*. Industry bodies such as the IPTC attest *what you are* (news organisation, musician, …).
* **Trust is not CAWG membership.** A signer is trusted because a designated partner verified their identity, not because they participate in CAWG.
* **Multiple credential types.** X.509 is profiled now, populating the CAWG trust configuration already defined in identity assertion 1.3. A vLEI profile is a placeholder pending the vLEI task force.

## Why now

Identity assertion 1.3 relies on an interim trust model (publicly trusted S/MIME certificates and the IPTC list) for assertions generated on or before 31 March 2027, with an extension to 31 August 2027 proposed. That was always a stopgap. A designated partner needs to be in place before the end date.

## Contents

The draft starts at [docs/modules/ROOT/pages/index.adoc](docs/modules/ROOT/pages/index.adoc):

1. Introduction: background, two layers, identity vs role, trust vs membership, scope
2. Framework overview: parties and how trust flows
3. Baseline requirements
4. Credential-type profiles: X.509, vLEI (placeholder)
5. Designation: criteria, process, terms, suspension and withdrawal, designation register
6. Validator requirements
7. Transition from the interim trust model
8. Open questions

## Governance

CAWG is transitioning from a Decentralized Identity Foundation working group to an independent Joint Development Foundation project under the Linux Foundation. This draft is intended to be subject to the W3C Patent Policy (2004), as described in [license.md](./license.md), which CAWG intends to carry forward.

## Local preview

The site is built with [Antora](https://antora.org) from AsciiDoc sources.

1. Install a current version of [Node.js](https://nodejs.org/en/download/).
2. Install dependencies:

```
npm install
```

3. Build the site (Antora reads committed content, so commit changes first):

```
npx antora antora-playbook-local.yml
```

Then open `build/site/index.html` in a browser.
