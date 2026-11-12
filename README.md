# ZAYU Forever Atlas

**Personal World of Warcraft addon discovery and research tool for Windows.**

> **Status:** v1.0.1 prototype · non-commercial hobby project · unofficial and not affiliated with CurseForge, Overwolf, Blizzard Entertainment, or addon authors.

ZAYU Forever Atlas helps players discover and compare World of Warcraft addons in a searchable, visual catalog. It is designed for players who want to review recently updated or newly published projects and quickly understand their purpose, including through **optional French-language AI summaries**.

The tool is not a mod hosting platform, an addon installer, or a replacement for CurseForge. Each listing links back to its original CurseForge project.

## Interface

The prototype includes three main sections: a **scan center**, an **AI prompt / JSON import assistant**, and a **searchable visual library**. Screenshots are available in the project preview package; they use illustrative/demo data and do not demonstrate a successful live CurseForge scan.

## What the prototype does

- Provides a Windows desktop UI built with **Python, pywebview, HTML, CSS, and JavaScript**.
- Lets users browse and organize addon titles, descriptions, images where available, and links to their original project pages.
- Supports two discovery views: **recently updated** and **recently created** addons, with duplicate detection across views.
- Provides optional **user-initiated AI prompt generation** to summarize descriptions in French. AI processing is performed outside the application when the user chooses to send the prompt to an AI service and manually import the response as JSON.
- Includes search, filters, list/card views, and image galleries when a project provides suitable images.
- Contains an optional **Chrome extension for manual, user-initiated capture** of pages that the user can access normally; it does not attempt to defeat captchas or access restrictions.

**Current limitations:** the automated website collection path may receive HTTP 403. Live collection and the Windows executable build have not yet been fully validated on a user PC. Available project data and gallery images depend on CurseForge and the individual addon pages.

## Intended CurseForge API integration

We are requesting access to the **official CurseForge third-party API** to retrieve addon metadata using authorized endpoints instead of relying on website scraping. The intended information includes:

- addon/project names, IDs, and original CurseForge URLs;
- descriptions and relevant version metadata;
- project icons and screenshots, if provided;
- update and release information to assist discovery.

API requests would be user-initiated, paginated, rate-conscious, and subject to the applicable API terms. The official API may not provide the same sorting options as the website: for example, release date is not always equivalent to project creation date.

**Data handling and permissions:** the prototype supports a user-local catalog, but we are seeking clarification or explicit authorization before enabling persistent storage of **API-derived** metadata or sending **API-derived** descriptions to external AI services. An API key will not be committed to this repository or shared in logs. Features that cannot comply with the granted API terms will be adjusted or disabled.

The application **does not distribute, download, mirror, or rehost addon files**. Any future distribution feature would require the necessary permissions from authors and the platform.

## Audience and business model

- **Audience:** World of Warcraft players, especially French-speaking users exploring addons.
- **Purpose:** personal discovery, comparison, organization, and understanding of addon projects.
- **Business model:** none. No ads, subscriptions, donations, affiliate revenue, or software sales are planned.
- **Attribution:** original authors retain ownership of their content; links lead users to the original CurseForge project pages.

## Prototype installation (Windows)

The current prototype requires **Python 3.11+** and a Windows environment with Edge WebView2. For the application source and installer, use the project's locally distributed v1.0.1 prototype package; this repository is initially intended as a public project description for the API access application.

The prototype is still under development and is not yet represented as a production-ready, fully tested release.

## Development roadmap

1. Confirm official third-party API access and permitted data-handling practices.
2. Validate authorized discovery, metadata, and screenshot endpoints on a real Windows system.
3. Improve data accuracy, attribution, duplicate handling, and error diagnostics.
4. Polish the French-language catalog and evaluate compliant options for summaries and storage.

## Compliance and credits

CurseForge and Overwolf are trademarks of their respective owners. World of Warcraft and Blizzard Entertainment are trademarks of Blizzard Entertainment. The project is an independent fan-made utility and is **not endorsed by or affiliated with** those parties.

API documentation and conditions: [CurseForge support](https://support.curseforge.com/).

**Contact:** via the GitHub repository owner, [Zarctus](https://github.com/Zarctus).
