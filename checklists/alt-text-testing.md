# ALT Text – Accessibility Testing Notes

 ALT text (Alternative Text) is used to describe images for users who rely on screen readers. Good ALT text makes sure everyone can understand the purpose of an image, even if they cannot see it.

## 🔹 Why ALT Text Matters

* Helps visually impaired users (read by screen readers).
* Shows up if images don’t load.
* Improves usability and sometimes SEO.


## 🔹 How to Test ALT Text

### ✅ Quick Steps

1. **Check if ALT text exists**

   * Web → `alt` attribute in `<img>`
   * Android → `contentDescription`
   * iOS → `accessibilityLabel`

2. **Use a screen reader**

   * NVDA (Windows, free)
   * JAWS (Windows, paid)
   * VoiceOver (iOS/macOS)
   * TalkBack (Android)
     👉 Listen: does it make sense?

3. **Ask:** *Does this text describe the purpose, not just the look?*


## 🔹 Tools You Can Use

* **WAVE** (browser extension) – shows missing/empty ALT.
* **axe DevTools** (Chrome/Firefox/Edge) – automated accessibility scan.
* **Lighthouse** (Chrome DevTools → Audits → Accessibility).
* **Accessibility Insights** (Microsoft).
* **Screen Readers** – NVDA, JAWS, VoiceOver, TalkBack.

## 🔹 Common Issues Found

* **Missing ALT** → screen reader just says *“image”*.
* **Meaningless ALT** → *“pic1.jpg”*, *“icon.png”*.
* **Redundant ALT** → *“button button”*.
* **Too long** → ALT text should be concise (under \~125 characters).
* **Decorative images not skipped** → should use empty ALT (`alt=""`).
* **Clickable images not described properly** → should describe the **action** (“Pay Now” not “green button”).


## 🔹 Quick Checklist

* [ ] ALT text present for all important images/icons
* [ ] ALT text is **short** (under \~125 characters)
* [ ] ALT text describes **purpose**, not appearance
* [ ] Decorative images skipped (`alt=""`)
* [ ] Functional images describe the **action** (e.g., “Send Money”)
* [ ] No redundancy (avoid “button button”)
* [ ] Verified with a screen reader (NVDA / JAWS / VoiceOver / TalkBack)
* [ ] Automated tool scan run (WAVE / axe / Lighthouse)


## 🔹 Mapping with Accessibility Standards

| Standard / Guideline                                      | Reference                                                                                                                       | What It Says About ALT Text                                                                                   |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **WCAG 2.1 – Success Criterion 1.1.1 (Non-text Content)** | [W3C WCAG 2.1](https://www.w3.org/TR/WCAG21/#non-text-content)                                                                  | All non-text content that is presented to the user has a text alternative that serves the equivalent purpose. |
| **Section 508 (US Govt.)**                                | [Section 508 Standards](https://www.section508.gov/manage/laws-and-policies/)                                                   | Requires text alternatives for all non-text elements.                                                         |
| **EN 301 549 (EU Accessibility Standard)**                | [EN 301 549 v3.2.1](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/03.02.01_60/en_301549v030201p.pdf)                | Mandates compliance with WCAG 2.1 AA, including ALT text for images.                                          |
| **Android Accessibility Guidelines**                      | [Android Dev Docs](https://developer.android.com/guide/topics/ui/accessibility)                                                 | Images must have `contentDescription` unless decorative.                                                      |
| **iOS Accessibility Guidelines**                          | [Apple HIG – Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility/overview/introduction/) | Images and icons should use `accessibilityLabel` to describe their purpose.                                   |

