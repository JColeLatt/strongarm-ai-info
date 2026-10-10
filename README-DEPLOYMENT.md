# Strong Arm Technologies — AI Discovery Kit

Prepared: 2026-10-10
Official website: https://www.strongarmtechnologies.com/home

## Purpose

Give a consistent, public, accurate description of the business that people, search engines and AI assistants can consult. This is an optional supplemental content package, NOT a ranking hack or a guarantee of AI recommendations.

## What's included

- `llms.txt` — short index of official pages and key facts (an emerging informal convention, not an accepted Google ranking requirement).
- `llms-full.txt` — detailed public business and service facts.
- `agents.md` — optional reference describing what automated agents should and should not assume. Does not grant agent authority.
- `organization.jsonld` — Schema.org Organization data template with no private physical address or phone. A standalone JSON-LD file does NOT apply schema to Google Sites merely by being hosted.
- `google-sites-business-info.md` — optional text to adapt in Google Sites, already aligned with business information available publicly.

## What is ALREADY done

The five existing Google Sites pages are live, Search Console domain ownership is verified, FAQ and services copy have been expanded, and Google Business Profile verification is pending. Do NOT request indexing repeatedly or publish contradictory business details.

## Google Sites hosting limitation

Google Sites does not allow uploading arbitrary root files such as `https://www.strongarmtechnologies.com/llms.txt` or controlling the root `robots.txt` file. Copying text onto a Google Sites page does not create a real `.txt` endpoint. Do not try to replace the root DNS CNAME, move your existing site, or delete email DNS records to add this kit.

## Deployment option A (recommended now): on-page information

1. Keep the existing Home, Services, Our Work, About Us and Contact Us pages live.
2. Compare `google-sites-business-info.md` against the existing content; only add useful, nonduplicate details (such as clear appointment-only contact guidance) to an ordinary public Google Sites page or existing About Us section.
3. Add a normal hyperlink to this content from Home or About Us if you create a new page. A page hidden from navigation with no inbound links is hard to discover.
4. Keep company name, support email, service area, contact form and service list consistent with Google Business Profile after approval.

## Deployment option B (optional): host the machine-readable files

Google Sites cannot serve these files at the main-domain root. If desired, create a SEPARATE static site (e.g. GitHub Pages) using a new public GitHub repository, without touching the existing Google Sites website or the unrelated IPTV repository.

Suggested workflow:
1. Sign into GitHub as `JColeLatt` and create a new public repository such as `strongarm-ai-info` (do not use the existing IPTV repository).
2. Upload `llms.txt`, `llms-full.txt` and `agents.md` to the repository root. Optionally include `organization.jsonld` for documentation.
3. Enable GitHub Pages under repo Settings > Pages, deploy from the main branch/root, and wait for GitHub to show a working HTTPS URL. Confirm actual URLs before sharing them. If the repository is a project site, file paths typically include `/strongarm-ai-info/`.
4. Add an unobtrusive link from an official Google Sites page to the public business-info text if desired. A separate host is NOT automatically associated with your main Google Sites page, and bot adoption of `llms.txt` is not guaranteed.
5. If you want `ai.strongarmtechnologies.com`, configure the separate host's custom domain and DNS in Squarespace later; do not alter existing `www` / MX / SPF / DKIM records. Domain changes are not needed to get started.

## Schema caveat

`organization.jsonld` is ready for sites that allow structured data scripts. The current Google Sites editor does not support placing arbitrary JSON-LD script tags in the page HTML head. A linked or separately hosted JSON-LD file is not equivalent to on-page schema markup. Because Strong Arm Technologies intentionally does not publish its home street address, avoid creating LocalBusiness structured data that invents an address just to satisfy Google's richer markup requirements.

## About robots.txt, sitemaps and search engines

Do not create a fake `robots.txt` file. Robots directives must be served at the actual host root to have effect, and an arbitrary external file cannot modify crawling policy of the Google Sites domain.

Do not submit a nonexistent `/sitemap.xml` to Search Console. Continue using URL Inspection/Pages indexing reports. Google can discover the public linked pages without an AI-specific file.

## Data safety

- The package contains NO home street address, phone number or private account information.
- Do not add credentials, client data, recovery keys, private photographs, or customer names.
- Do not promise guaranteed recovery, fixed prices, walk-in hours or instant bookings.
- Maintain `llms-full.txt` when service offerings or contact policies change.

## Validation after deployment

- Verify each published endpoint returns a genuine HTTP 200 and plain text/Markdown content.
- Verify links to all five official Google Sites pages and contact form work.
- Make sure no private residential address is visible.
- Review Google Search Console after several days or weeks for indexing, not for an immediate AI score.

## Limits and expectations

Google's official guidance: https://developers.google.com/search/docs/appearance/ai-features
Google says special AI text files are not required for AI Overviews / AI Mode. Useful content, appropriate internal linking, Business Profile accuracy, and indexability matter more.
