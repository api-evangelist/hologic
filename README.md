# Hologic

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

This is a repository for tracking the APIs, SDKs, and other developer resources for Hologic.

## APIs

Hologic publishes **no public web API**, no developer portal, no OpenAPI/GraphQL/AsyncAPI
specification, no SDK on any package registry, and no MCP server or A2A agent card. This was
established by probing nineteen Hologic-controlled hosts on 2026-09-13 — see
`x-contract-discovery` in `apis.yml` for the full probe record.

That is the expected shape for a medical device manufacturer. Hologic's integration contract is
**DICOM**, published per product as a Conformance Statement, plus HL7 v2 feeds into RIS/HIS/LIS.
Those statements are public and real — the Selenia Dimensions / 3Dimensions Acquisition Workstation
statement (MAN-05763) declares Modality Worklist FIND, MPPS, Storage, Storage Commitment Push Model,
Study Root Query/Retrieve FIND and MOVE, Print and Verification under the DICOM UID root
`1.2.840.10008` — but they ship as PDF, so no machine can read them.

## What this repository does hold

| Artifact | What it is |
|---|---|
| `llms/hologic-llms.txt` | Hologic's own `llms.txt`, served at https://www.hologic.com/llms.txt (HTTP 200, 24,799 bytes) and saved verbatim. 18 sections, 154 linked resources. |
| `well-known/` | The `/.well-known/` probe across nine hosts, plus the one document served: a valid OpenID Connect discovery document at `support.hologic.com`. |
| `authentication/` + `scopes/` | The OIDC/OAuth profile that document describes — Salesforce Experience Cloud running under Hologic's issuer, for support-community sign-in, not an API product. |
| `conformance/` | DICOM, HL7, MDS2 and the OAuth/OIDC RFC set, each with a fetched evidence URL and status. |
| `security/` | The Coordinated Vulnerability Disclosure Policy (`CoordinatedVulnerability@hologic.com`, PGP key published), the product-security hub that stands in for a trust center, and the domain security probe. |
| `lifecycle/` | The Hologic Imaging Product Obsolescence & End-of-Life Guide — the device-industry deprecation contract, dated per product. |
| `packages/` · `plans/` | Measured zeros: no client library on any registry, no published pricing. |

## Properties

- [Website](https://www.hologic.com)
- [Support](https://www.hologic.com/support)
- [Support Community Sign-in](https://support.hologic.com/s/login/)
- [Newsroom](https://www.hologic.com/about/newsroom)
- [Coordinated Vulnerability Disclosure](https://www.hologic.com/security/coordinated-vulnerability-disclosure-policy)
- [Breast & Skeletal Products Cybersecurity](https://www.hologic.com/support/usa/breast-skeletal-products-cybersecurity)
- [MDS2 Forms](https://www.hologic.com/support/usa/Breast-Skeletal-Products-Cybersecurity/MDS2-forms)
- [Product Obsolescence & End-of-Life Guide](https://www.hologic.com/end-of-life)
- [Package Inserts & IFUs](https://www.hologic.com/package-inserts)
- [Terms and Conditions](https://www.hologic.com/terms-conditions)
- [Privacy Policy](https://www.hologic.com/privacy-policy)
- [GitHub (Breast & Skeletal Health Division)](https://github.com/Hologic-BSHS)
- [LinkedIn](https://www.linkedin.com/company/hologic)
