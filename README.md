# Amiibo API

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
