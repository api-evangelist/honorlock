# Honorlock (honorlock)

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
