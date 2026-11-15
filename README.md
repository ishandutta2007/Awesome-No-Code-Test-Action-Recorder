# Awesome-No-Code-Test-Action-Recorder

# Awesome No-Code Test Action Recorder

> A curated list of top No-Code Test Action Recorder platforms — both SaaS/Hosted commercial solutions and open-source alternatives for recording user interactions and converting them into automated test scripts.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [Sector Overview & Market Dynamics](#-sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
- [Open-Source Software](#-open-source-software)
  - [Playwright Codegen](#playwright-codegen)
  - [Chrome DevTools Recorder](#chrome-devtools-recorder)
  - [Selenium IDE](#selenium-ide)
  - [UI Recorder](#ui-recorder)

---

## 🌐 Sector Overview & Market Dynamics

The global automated testing market is estimated at **$25B–$35B** (projected to exceed **$80B+ by the early 2030s** at a ~14–16% CAGR), propelled by continuous integration/continuous delivery (CI/CD) pipelines and generative AI adoption. The sector remains **highly fragmented** rather than winner-take-all; enterprise legacy suites (Tricentis, OpenText), high-scale cloud execution grids (BrowserStack, Sauce Labs), agile modern test frameworks (Cypress, Playwright), and specialized scriptless AI startups continually compete and coexist across diverse browser, mobile, and enterprise application stacks.

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted No-Code Test Action Recorder platforms. These are not open-source but are included as reference points for feature comparison.

| Platform | Company Valuation / Scale | Type | Starting Pricing | Free Tier / Trial Limit | Key Highlights | Best For |
|---|---|---|---|---|---|---|
| **Testim Recorder** | ~$4.5B valuation (Parent: Tricentis; acquired for $200M; ~$425M ARR) | Free Puppeteer recorder with codeless comparison | Paid plans start at ~$450/mo (Essentials tier based on parallel execution slots) | Permanent free Community Plan (up to 1,000 test runs/month after 14-day trial) | Free Puppeteer recorder converting interactions into Puppeteer code alongside codeless tests, with real-time updates and AI element locators. | Developers using Puppeteer wanting to accelerate test creation with a recorder that generates real Puppeteer code. |
| **BrowserStack Low-Code Automation** | $4B valuation (~$250M ARR; Series B unicorn) | AI-powered recorder within BrowserStack platform | Starts at $29/mo (Live manual testing) or $99/mo (Automate testing, billed annually) | Free trial with 30 min Live / 100 min Automate; unlimited access for qualified open source | AI-powered validations (visual, text, element presence), intelligent wait timeouts, custom JS actions, API simulation, and conditional loops. | Teams in the BrowserStack ecosystem wanting AI-assisted recording with built-in validation and debugging tools. |
| **mabl Trainer** | ~$400M valuation (~$25M–$35M ARR; $76M raised) | AI-powered low-code test recorder | Starts at ~$499/mo (quote-based based on test execution volume and tier) | 14-day free trial with full platform access (no permanent free tier) | Plain-language step descriptions, generative AI test authoring, self-healing tests, visual assertions, and local MCP server for AI agent integration. | Teams wanting AI-assisted recording with plain-language step descriptions and MCP integration for AI agents. |
| **Cypress Studio** | ~$60M+ valuation / $18M–$20M ARR ($55M+ venture raised) | Interactive test recorder within Cypress App | Starter plan is $0/mo; paid plans start at $67/mo (Team plan billed annually) | Permanent free Starter tier: 500 recorded test results/mo, up to 10 users, 30 days data retention | Embedded recorder in Cypress App generating native Cypress commands (`.click()`, `.type()`, etc.); selector priority strategy (`data-cy`, `data-test`, `id`). | Teams already writing Cypress tests wanting to accelerate test creation with a recorder that generates native Cypress commands. |
| **Ghost Inspector Recorder** | Bootstrapped / Acquired by SureSwift Capital (~$1M–$3M ARR) | Browser extension for recording regression tests | Starts at $109/mo (billed annually, includes 10,000 test runs/mo and 5 seats) | 14-day free trial with full features (no credit card required; no permanent free tier) | Chrome extension records user journeys and syncs to hosted continuous regression suite; schedule runs via API or cron across staging and production. | Teams wanting a simple browser-extension recorder tied to a hosted regression testing service, particularly for continuous monitoring. |

---

## 🟩 Open-Source Software

Self-hosted, community-driven No-Code Test Action Recorder tools. The open-source ecosystem spans **built-in codegen tools**, **browser-native recorders**, and **legacy recorders with active forks**.

### Playwright Codegen
**Stack:** Node.js / Python / Java / .NET | **License:** Apache-2.0
Playwright includes a built-in **Codegen** tool that opens a browser window for interaction and generates test code in real time . It analyzes the rendered page and recommends the best locator, prioritizing **role, text, and test ID locators**, and improves locators when multiple elements match to reduce flakiness . You can record actions (click, fill) and assertions (visibility, text, value) by clicking toolbar icons, with support for emulation of viewports, devices, color schemes, geolocation, language, and timezone . Generated code can be copied directly to your editor . **Key advantage:** It ships with Playwright itself, requiring no additional installation or account.
**Best for:** Teams using Playwright wanting a free, built-in recorder that generates resilient locators and supports advanced emulation scenarios.

### Chrome DevTools Recorder
**Stack:** JavaScript / Browser-native | **License:** Open Source (Chromium)
Chrome DevTools includes a **Recorder** panel that records user interactions and exports them in multiple formats: **JSON, Puppeteer, @puppeteer/replay, Cypress Test, WebPageTest custom script, WebdriverIO Test, Nightwatch Test, and Testing Library script** . Steps can be edited, removed, or configured with properties like target, asserted events, frame, timeout, and selectors . The `chrome.devtools.recorder` API allows extensions to customize the export and replay functionality . **Trade-off:** It is a browser-native tool rather than a standalone platform, and generated code quality depends on the target framework.
**Best for:** Developers wanting a free, zero-install recorder built into Chrome that can export to multiple test frameworks.

### Selenium IDE
**Stack:** Browser Extension | **License:** Apache-2.0
Selenium IDE is the long-standing browser extension for recording and replaying Selenium tests, with support for implicit locators and DOM exploration . **Important status:** The original Selenium IDE is now documented as a **legacy** tool, with the Selenium project's current documentation focusing on Selenium WebDriver rather than the IDE . While the extension remains available, its active development and feature evolution have slowed compared to modern alternatives like Playwright Codegen and Chrome DevTools Recorder.
**Best for:** Teams with existing Selenium IDE test suites or those wanting a familiar, browser-extension-based recorder, accepting its legacy status.

### UI Recorder
**Stack:** Node.js | **License:** Open Source (npm)
UI Recorder is a **zero-cost UI test case recorder** positioned as a more powerful Selenium IDE alternative . It supports all user operations including key events, mouse events, alerts, file uploads, drag, SVG, and Shadow DOM, with **mobile native app recording** via macaca . Features include recording without interference, test files saved locally, multiple expectation types (val, text, displayed, enabled, selected, attr, css, url, title, cookie, localStorage, sessionStorage), Faker.js mock support, common test case reuse, parallel testing, i18n (en, zh-cn, zh-tw), screenshots after each step, HTML and JUnit reports, and cross-platform support (Windows, Mac, Linux) . It is Node.js-based and runs on jWebDriver .
**Best for:** Teams wanting a feature-rich, free recorder with mobile support and extensive expectation types, accepting a Node.js CLI workflow.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Generated Code | Assertions | Self-Hosted | Best For |
|----------|---------|-------|----------------|------------|-------------|----------|
| **BrowserStack** | Proprietary | Cloud | Proprietary steps | ✅ AI validations | ❌ | AI-assisted recorder + debugging |
| **Cypress Studio** | Proprietary | Cloud/Desktop | Cypress commands | ✅ (AI optional) | ❌ | Native Cypress test authoring |
| **mabl Trainer** | Proprietary | Cloud | Proprietary steps | ✅ Visual | ❌ | Plain-language + MCP |
| **Testim Recorder** | Proprietary | Cloud | Puppeteer JS | ✅ Codeless | ❌ | Puppeteer code generation |
| **Playwright Codegen** | Apache-2.0 | Node/Python/Java | Playwright code | ✅ Toolbar assertions | ✅ (Built-in) | Resilient locators + emulation |
| **Chrome DevTools Recorder** | Open Source | Browser | JSON/Puppeteer/Cypress/etc | ✅ assertedEvents | ✅ (Browser) | Multi-framework export |
| **Selenium IDE** | Apache-2.0 | Extension | Selenium scripts | ✅ | ✅ | Legacy Selenium suites |
| **UI Recorder** | Open Source | Node.js | jWebDriver code | ✅ 11 types | ✅ | Mobile + extensive expectations |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source No-Code Test Action Recorder tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The recorder landscape has shifted decisively toward **framework-native codegen tools**. **Playwright Codegen** is the strongest open-source choice, shipping with the framework itself and generating resilient locators with role/text/test-id priority . **Chrome DevTools Recorder** offers unmatched export flexibility, supporting Puppeteer, Cypress, WebdriverIO, Nightwatch, and Testing Library from a single recording . **Selenium IDE** is now documented as legacy, with the Selenium project focusing on WebDriver rather than the IDE . **Katalon Recorder**, once a popular Selenium IDE alternative, is **no longer actively maintained** by the Katalon team, with no further feature development, updates, or security patches planned . For mobile recording, **UI Recorder** remains a viable open-source option via macaca integration . Commercial platforms like BrowserStack and mabl add AI-powered validations and debugging that open-source recorders do not match, but the core recording capability is well-covered by Playwright and Chrome DevTools.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
