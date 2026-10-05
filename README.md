# Creator Assertions Working Group :: Trust List (draft)

This repository contains a **pre-draft proposal** for a CAWG Trust List: the trust anchors, certificate policy and governance needed so validators can recognise X.509 certificates issued to CAWG members for signing [identity assertions](https://cawg.io/identity/) (`cawg.x509.cose`).

It follows the model of the [C2PA Trust List](https://spec.c2pa.org/specifications/specifications/2.4/specs/C2PA_Specification.html#_trust_lists) and fills in the *CAWG trust configuration* that the identity assertion specification already defines but has not yet populated.

> **Status:** Working proposal. Nothing here has been adopted by the CAWG or DIF. The repository name `cawg-trust-list` is provisional.

## Why

Identity assertion v1.3 says a validator maintains a *CAWG trust configuration* (accepted EKUs → accepted certificate policies + trust anchors) and requires `id-kp-documentSigning`, but defines no certificate policy or trust anchors for it. Until **31 March 2027**, an interim model accepts publicly trusted S/MIME certificates (organisation-, sponsor- or individual-validated) and the IPTC Origin Verified News Publishers List. After that date there is nothing for validators to trust unless a list like this exists.

## Contents

The specification draft starts at [docs/modules/ROOT/pages/index.adoc](docs/modules/ROOT/pages/index.adoc). It covers:

* how the CAWG Trust List plugs into the existing CAWG trust configuration;
* the CAWG certificate policy (membership vetting, profile, revocation);
* governance: CA admission and removal, list operation and publication;
* transition from the interim S/MIME model;
* open questions for the working group.

## Governance

This specification is intended to be subject to:

* The W3C Patent Policy (2004) as described in the [license.md](./license.md) file.
* The DIF [Code of Conduct](https://bit.ly/DIF_code_of_conduct).
* The DIF [CAWG Charter](https://github.com/decentralized-identity/org/blob/main/Org%20documents/WG%20documents/DIF_CAWG_WG_charter_v1.pdf).
* The DIF [CAWG Operating Addendum](https://github.com/decentralized-identity/org/blob/main/Org%20documents/WG%20documents/DIF_CAWG_WG_Operating_Addendum_v1.pdf).

## Site build process

The site content is built using [Antora](https://antora.org), which takes AsciiDoc (.adoc) files and renders them to HTML.

## Local preview

1. Install a current version of [Node.js](https://nodejs.org/en/download/).
2. Install Antora and other project dependencies:

```
npm install
```

3. Build the site:

```
npx antora antora-playbook-local.yml
```

Then open `build/site/index.html` in a browser. Antora has no live preview, so re-run the build after each change.
