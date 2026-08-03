# Amiibo API

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

AmiiboAPI is a free RESTful API providing comprehensive data about Nintendo Amiibo figures, including character details, game series, amiibo series classifications, regional release dates, and compatible game information across 3DS, Wii U, and Nintendo Switch platforms.

## API Details

- **Base URL:** https://amiiboapi.org/api/
- **Documentation:** https://amiiboapi.org/docs/
- **Authentication:** None required
- **Rate Limits:** Not documented; caching recommended
- **License:** MIT (open source)
- **GitHub:** https://github.com/N3evin/AmiiboAPI

## Key Endpoints

| Endpoint | Description |
|----------|-------------|
| `GET /api/amiibo/` | All amiibo in the database |
| `GET /api/amiibo/?name={name}` | Filter by amiibo name |
| `GET /api/amiibo/?character={character}` | Filter by character |
| `GET /api/amiibo/?gameSeries={series}` | Filter by game series |
| `GET /api/amiibo/?amiiboSeries={series}` | Filter by amiibo series |
| `GET /api/amiibo/?type={type}` | Filter by type (Figure, Card, Yarn) |
| `GET /api/amiibo/?showgames` | Include compatible games in response |
| `GET /api/amiibo/?showusage` | Include game usage details |
| `GET /api/type/` | All amiibo types |

## Response Fields

Each amiibo object includes:
- `name` - Product name
- `character` - Character name
- `gameSeries` - Associated game series
- `amiiboSeries` - Amiibo series classification
- `type` - Figure, Card, or Yarn
- `image` - Image URL
- `release` - Regional release dates (na, eu, jp, au)
- `head` / `tail` - Hexadecimal identifiers
- `games3DS` / `gamesSwitch` / `gamesWiiU` - Compatible titles (with showgames)

## APIs.json Profile

This repository contains an [APIs.json 0.19](https://apisjson.org/) profile for the Amiibo API:

- [`apis.yml`](apis.yml) - Main APIs.json index
- [`plans/amiibo-plans-pricing.yml`](plans/amiibo-plans-pricing.yml) - Pricing plans
- [`rate-limits/amiibo-rate-limits.yml`](rate-limits/amiibo-rate-limits.yml) - Rate limit details
- [`finops/amiibo-finops.yml`](finops/amiibo-finops.yml) - Financial operations profile

## Maintainer

Kin Lane - kin@apievangelist.com
