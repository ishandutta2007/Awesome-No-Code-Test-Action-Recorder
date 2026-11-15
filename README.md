# Awesome-No-Code-Test-Action-Recorder

# Awesome No-Code Test Action Recorder

> A curated list of top No-Code Test Action Recorder platforms — both SaaS/Hosted commercial solutions and open-source alternatives for recording user interactions and converting them into automated test scripts.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [BrowserStack Low-Code Automation](#browserstack-low-code-automation)
  - [Cypress Studio](#cypress-studio)
  - [mabl Trainer](#mabl-trainer)
  - [Testim Recorder](#testim-recorder)
  - [Ghost Inspector Recorder](#ghost-inspector-recorder)
- [Open-Source Software](#-open-source-software)
  - [Playwright Codegen](#playwright-codegen)
  - [Chrome DevTools Recorder](#chrome-devtools-recorder)
  - [Selenium IDE](#selenium-ide)
  - [UI Recorder](#ui-recorder)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted No-Code Test Action Recorder platforms. These are not open-source but are included as reference points for feature comparison.

### BrowserStack Low-Code Automation
**Type:** AI-powered recorder within BrowserStack platform
BrowserStack's Low-Code Automation provides an intuitive recorder that captures user actions and converts them into automated test steps without coding . Key features include **AI-powered validations** (visual, text, and element presence checks), intelligent wait timeouts to reduce flakiness, custom JavaScript actions, API steps for backend simulation, conditional loops, and dynamic test data . It is positioned for teams already using BrowserStack for cross-browser testing who want to accelerate test authoring without writing code .
**Best for:** Teams in the BrowserStack ecosystem wanting AI-assisted recording with built-in validation and debugging tools.

### Cypress Studio
**Type:** Interactive test recorder within Cypress App
Cypress Studio lets you generate and extend E2E tests by recording real interactions in your app, translating each action into Cypress commands in real time . It supports `.click()`, `.type()`, `.check()`, `.uncheck()`, and `.select()` actions, with manual assertion addition and inline code editing . **Studio AI** (requires Cypress Cloud account) automatically recommends assertions as you record, with a free Starter plan available . It uses a priority strategy for selectors: `data-cy`, `data-test`, `data-testid`, `data-qa`, `name`, `id`, `class`, then tag and attributes .
**Best for:** Teams already writing Cypress tests wanting to accelerate test creation with a recorder that generates native Cypress commands.

### mabl Trainer
**Type:** AI-powered low-code test recorder
mabl Trainer records browser and mobile test steps with **plain language descriptions** that capture intent, with multilingual support . It includes **generative AI test creation**, variable management with source attribution, database query steps, visual assertions for file downloads, and a local MCP server for connecting AI clients to mabl testing tools . It is positioned for teams wanting low-code test authoring with strong AI assistance.
**Best for:** Teams wanting AI-assisted recording with plain-language step descriptions and MCP integration for AI agents.

### Testim Recorder
**Type:** Free Puppeteer recorder with codeless comparison
Testim offers a **free Puppeteer recorder** that captures UI interactions and generates JavaScript code compatible with Puppeteer, with the Testim codeless test viewable alongside for comparison . Changes made in the codeless tab automatically update the Puppeteer code in real-time . Testim claims recordings provide a **60-70% jumpstart** on coded Puppeteer tests, automating much of the setup code . The broader Testim platform uses AI to keep tests stable as code changes .
**Best for:** Developers using Puppeteer wanting to accelerate test creation with a recorder that generates real Puppeteer code, accepting the Testim ecosystem.

### Ghost Inspector Recorder
**Type:** Browser extension for recording regression tests
Ghost Inspector's Chrome extension lets you record actions on your website, sync them to the Ghost Inspector service, and run them continuously as regression tests . Tests can be recorded on staging and executed via API on code changes, or recorded on live sites and run at set intervals . It requires a Ghost Inspector account and does not collect or use your data .
**Best for:** Teams wanting a simple browser-extension recorder tied to a hosted regression testing service, particularly for continuous monitoring.

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
