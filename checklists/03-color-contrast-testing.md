# Color Contrast – Accessibility Testing Notes

**Color contrast** means there should be enough difference between text (or important UI elements) and the background so that people can read or see them easily. Low contrast text or icons can make apps and websites unusable for users with low vision, color blindness, or when viewed in bright light.

## 🔹 Why Color Contrast Matters

* Helps people with low vision or color blindness read text.
* Improves readability in difficult conditions (e.g., sunlight glare).
* Ensures compliance with WCAG standards.
* Better contrast = better usability for **everyone**, not just people with disabilities.

## 🔹 How to Test Color Contrast

### ✅ Quick Steps

1. Identify text, icons, and important visual elements.
2. Use a **contrast checker tool** → enter foreground (text) and background colors.
3. Verify that contrast meets **WCAG requirements**:

   * Normal text → **4.5:1** ratio (minimum)
   * Large text (≥18pt or bold 14pt) → **3:1** ratio
   * UI components and graphical objects (icons, form fields, buttons) → **3:1** ratio

## 🔹 Tools You Can Use

* **WebAIM Contrast Checker** → [contrastchecker.com](https://webaim.org/resources/contrastchecker/)
* **WAVE Toolbar** → highlights low contrast issues.
* **axe DevTools** (browser extension) → flags contrast failures.
* **Lighthouse** (Chrome DevTools → Audits → Accessibility).
* **Color Contrast Analyzer (CCA)** by Paciello Group → desktop app.
* **Color Oracle** → simulates color blindness.
* **Mobile Testing** → use TalkBack/VoiceOver and accessibility scanner apps (like Android Accessibility Scanner).

## 🔹 Common Issues Found

* Light gray text on white background.
* Placeholder text with very low contrast.
* Buttons with text that blends into background color.
* Disabled elements not visible enough.
* Icons or status indicators (e.g., red/green) without enough contrast.
* Relying only on **color** to convey meaning (e.g., error message only in red).

## 🔹 Quick Checklist

* [ ] All normal text has contrast ratio ≥ 4.5:1
* [ ] Large text (≥18pt or bold 14pt) has contrast ratio ≥ 3:1
* [ ] Icons and graphical objects have contrast ratio ≥ 3:1
* [ ] Placeholder text is readable (not too light)
* [ ] Disabled states are distinguishable
* [ ] Color is **not the only indicator** (use text, icons, shapes as well)
* [ ] Tested with automated tools (axe, WAVE, Lighthouse)
* [ ] Verified manually in real-world conditions (bright light, low brightness, color blindness simulation)

---

## 🔹 Mapping with Accessibility Standards

| Standard / Guideline                         | Reference                                                                                                                       | What It Says About Color Contrast                                                                  |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **WCAG 2.1 – SC 1.4.3 (Contrast Minimum)**   | [W3C WCAG 2.1](https://www.w3.org/TR/WCAG21/#contrast-minimum)                                                                  | Text and images of text must have a contrast ratio of at least 4.5:1 (normal) or 3:1 (large).      |
| **WCAG 2.1 – SC 1.4.11 (Non-text Contrast)** | Same                                                                                                                            | UI components and graphical objects must have at least 3:1 contrast ratio against adjacent colors. |
| **Section 508 (US Govt.)**                   | [Section 508 Standards](https://www.section508.gov/manage/laws-and-policies/)                                                   | Requires compliance with WCAG 2.0 AA (includes color contrast).                                    |
| **EN 301 549 (EU)**                          | [EN 301 549 v3.2.1](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/03.02.01_60/en_301549v030201p.pdf)                | Requires compliance with WCAG 2.1 AA color contrast.                                               |
| **Android Accessibility Guidelines**         | [Android Dev Docs](https://developer.android.com/guide/topics/ui/accessibility)                                                 | Text and UI elements must meet minimum contrast ratios.                                            |
| **iOS Accessibility Guidelines**             | [Apple HIG – Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility/overview/introduction/) | Ensure sufficient contrast between foreground and background colors.                               |