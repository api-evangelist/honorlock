# Honorlock (honorlock)

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

Honorlock is an online exam proctoring and academic integrity platform for higher education and professional certification. Its primary integration path is **LTI 1.3**, installed natively into LMS platforms - Canvas, Blackboard, Moodle, D2L Brightspace, Open LMS, Docebo, and Intellum - plus publisher platforms such as Pearson, McGraw Hill, and ALEKS via LMS workflows. For assessment platforms that need to embed proctoring outside an LMS, Honorlock offers a partner developer toolkit ("APIs and Elements") documented at `docs.honorlock.com`.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/honorlock/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/honorlock/refs/heads/main/apis.yml)

## Access Model (Important)

Honorlock's developer program is **sales-gated**, not self-service:

- **LTI 1.3 is the main path.** Most institutions adopt Honorlock by installing its native LTI 1.3 tool into their LMS (to a primary account or a sub-account, typically in about an hour). No bespoke API work is required for the standard LMS flow.
- **The REST API + Elements SDK is for custom assessment platforms.** Honorlock exposes a developer toolkit ("APIs and Elements") for embedding proctoring directly into a non-LMS assessment platform. It is documented at `docs.honorlock.com` but the endpoint reference is served from a client-rendered single-page app and is gated behind the partner developer program.
- **No public self-service.** There is no advertised free tier, public API key issuance, published base URL, or OpenAPI description. The custom-integrations page directs integrators to "Speak to an expert about integrating with Honorlock."

Because the endpoint reference is gated, the APIs and operations catalogued here are **modeled** from Honorlock's public integration documentation (the three-phase Enablement / Administrator Experience / Exam Taker Experience narrative), not copied from a published OpenAPI. No OpenAPI document was fabricated. See `review.yml` (`endpointsModeled: true`).

## Tags

- Proctoring
- Online Proctoring
- Academic Integrity
- Assessment
- EdTech
- LTI
- Exams
- Education

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

> Endpoints below are modeled from Honorlock's public integration documentation. Exact HTTP methods, paths, and base URL are gated behind the partner developer program.

### Honorlock Authentication API

Generate the integration and user authentication tokens that authorize an assessment platform to provision and drive Honorlock proctoring on behalf of an institution.

- **Documentation:** [https://docs.honorlock.com/api](https://docs.honorlock.com/api)

### Honorlock Users API

Create and list the users (students, instructors, administrators) that participate in proctored exams - the API-driven equivalent of what LTI 1.3 provisions automatically inside a native LMS install.

- **Documentation:** [https://docs.honorlock.com/api](https://docs.honorlock.com/api)

### Honorlock Courses API

Create and manage the courses that group exams and enrolled users when an assessment platform integrates directly rather than through an LMS.

- **Documentation:** [https://docs.honorlock.com/api](https://docs.honorlock.com/api)

### Honorlock Exams API

Create and configure proctored exams - the settings that determine which integrity controls (ID verification, browser guard, recording, room scan, live pop-in, Search and Destroy) apply to an assessment.

- **Documentation:** [https://docs.honorlock.com/api](https://docs.honorlock.com/api)

### Honorlock Exam Sessions API

Drive the exam-taker lifecycle - set up a session, verify that the test taker has completed the authentication steps (Verify Authentication), begin the proctored attempt, and close it out (End Exam Session) when the exam is submitted.

- **Documentation:** [https://docs.honorlock.com/exam-taker](https://docs.honorlock.com/exam-taker)

### Honorlock Elements & Integration SDK

Browser-side Integration SDK and Elements UI components that embed the Honorlock exam-taker experience into a custom assessment platform - browser extension verification, pre-exam authentication and room scan, and the in-exam proctoring surface. A client-side JavaScript toolkit rather than a server REST resource.

- **Documentation:** [https://docs.honorlock.com/integration-sdk](https://docs.honorlock.com/integration-sdk)

## LTI Integration

Honorlock integrates directly with LTI-compliant platforms using **LTI version 1.3**. Native LTI integrations exist for Canvas, Blackboard, Moodle, D2L Brightspace, Open LMS, Docebo, and Intellum, with support for third-party publisher platforms (Pearson, McGraw Hill, ALEKS) via LMS workflows. This is the recommended and most common integration path; the REST API and Elements SDK are the alternative for custom, non-LMS assessment platforms.

## Pricing

Honorlock uses a **flat-rate price per exam / per test taker** (rather than per-hour billing), with implementation, training, and 24/7/365 US-based support included at no extra cost. Honorlock does not publish list prices, minimums, or standard per-student rates; institutions receive a **custom quote** shaped by exam volume, modality mix, LMS scope, and premium capabilities such as Search and Destroy. Contact Honorlock directly for pricing.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/honorlock)
- [Website](https://honorlock.com)
- [Documentation](https://docs.honorlock.com)
- [Custom Integrations](https://honorlock.com/custom-integrations/)
- [LMS Integrations](https://honorlock.com/integrations/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
