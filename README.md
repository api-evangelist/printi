# Printi (printi)

Printi is a Brazilian online commercial print marketplace founded in 2012 and based in Barueri / São Paulo. It sells business cards, flyers, stationery, labels and stickers, packaging, brochures and folders, and promotional items through an online configurator that prices each job dynamically by format, paper, finish, and quantity. Printi is a **Cimpress** brand — Vistaprint took a minority stake in 2014 and Cimpress acquired a majority stake in 2020 — and sits in the same Cimpress portfolio as Vistaprint.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/printi/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/printi/refs/heads/main/apis.yml)

## API Access Model — read this first

Printi does **not** currently expose a live, documented, self-serve public developer API.

- Printi **formerly** ran a public developer portal at `developer.printi.com.br` titled **"Printi API"** (hosted on ReadMe, with a "Run in Postman" button). That subdomain **no longer resolves in DNS** and the portal appears **decommissioned**. Only its homepage is preserved in the Wayback Machine (closest snapshot 2024-08-29).
- The host `api.printi.com.br` today returns an internal Angular back-office app (`Printi Admin - Main Page`), **not** public API documentation. Its `/health` endpoint returns `200`, while `/v1`, `/docs`, `/swagger`, and `/openapi.json` return `404`.
- The former US property `printi.com` now redirects to `www.printi.com.br`.
- Programmatic and reseller integration is **partner-gated** — channeled through Cimpress's mass-customization / developer platform and Printi's "Comprar com Vendedor" reseller channel — rather than an open public API.

Because there is no live public specification, this entry is an **honest gated / retired-portal stub**. The API areas listed below are **MODELED** (see `endpointsModeled: true` in `review.yml`) from the historical portal and observable storefront behavior. They are **not** verified endpoints, and no OpenAPI, plans, rate-limits, FinOps, or collection artifacts were fabricated.

## Tags

- Printing
- Print on Demand
- Commercial Print
- Marketplace
- Ecommerce
- Brazil
- Cimpress
- Partner Gated

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs (modeled — not verified endpoints)

### Printi Products Catalog API

Modeled catalog surface for browsing Printi's printable product lines (business cards, flyers, stationery, labels, packaging, promotional items) and their configurable options — format, paper stock, finish, and quantity tiers. Inferred from the retired `developer.printi.com.br` portal and the live storefront configurator.

- **Human URL:** [https://www.printi.com.br](https://www.printi.com.br)

### Printi Quotes and Pricing API

Modeled quoting surface that returns a price for a chosen product configuration — product, format, paper, finish, quantity, and delivery — mirroring the storefront's dynamic configurator (for example flyers from 250 units). Printi prices per job at quote time rather than from a fixed public price list, so there is no public tiered plan catalog.

- **Human URL:** [https://www.printi.com.br](https://www.printi.com.br)

### Printi Orders API

Modeled order surface for submitting an accepted quote as a print order, attaching artwork, and tracking production and delivery status. Inferred from the retired Printi developer portal and Printi's reseller ("Comprar com Vendedor") flow; in practice this capability is partner-gated today via Cimpress's platform.

- **Human URL:** [https://www.printi.com.br](https://www.printi.com.br)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/printi)
- [Website](https://www.printi.com.br)
- [Reseller](https://www.printi.com.br/comprar-com-vendedor)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
