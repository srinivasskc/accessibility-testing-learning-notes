# ARIA (Accessible Rich Internet Applications) – Overview

## 🔹 What is ARIA?

* ARIA is a set of **HTML attributes** that define roles, states, and properties for elements.
* It helps screen readers and assistive tech understand **custom UI controls** (menus, sliders, dialogs).
* **Golden Rule**: *Use native HTML first. Use ARIA only when HTML alone isn’t enough.*

## 🔹 Why ARIA Matters

* Modern web apps often use custom JavaScript controls.
* Without ARIA, assistive tech may not know what an element is or what state it’s in.
* ARIA improves the accessibility of **dynamic, interactive content**.

## 🔹 How to Test ARIA (High Level)

1. **Check for roles** → does the element expose the correct role (`button`, `dialog`, `menu`)?
2. **Check labels** → do `aria-label` or `aria-labelledby` provide a meaningful name?
3. **Check states** → do attributes like `aria-expanded`, `aria-checked` update correctly?
4. **Check relationships** → are `aria-controls`, `aria-describedby` pointing to real, visible elements?
5. **Verify with a screen reader** → confirm role, name, and state are read out correctly.

## 🔹 Tools You Can Use

* **axe DevTools** → highlights ARIA misuse.
* **WAVE** → shows ARIA attributes visually.
* **Accessibility Insights** → guided checks including ARIA.
* **Chrome DevTools Accessibility Pane** → inspect computed role/name/value.
* **Screen readers** (NVDA, JAWS, VoiceOver, TalkBack).


## 🔹 Common Issues Found

* Using ARIA where HTML is enough (`div role="button"` instead of `<button>`).
* Attributes not updated (e.g., `aria-expanded` stays “false” after opening).
* Incorrect or broken references (`aria-labelledby` pointing to a missing ID).
* Redundant/confusing ARIA (over-labeling, duplicate roles).


## 🔹 Quick Checklist

* [ ] ARIA only used when HTML alone can’t express meaning.
* [ ] Elements have meaningful name (`aria-label`, `aria-labelledby`).
* [ ] States (`aria-expanded`, `aria-checked`) update correctly on interaction.
* [ ] Relationships (`aria-controls`, `aria-describedby`) point to valid elements.
* [ ] Tested with a screen reader for real-world verification.


## 🔹 Mapping with Accessibility Standards

| Standard                                    | Reference                                                                                                 | What It Says About ARIA                                               |
| ------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **WCAG 2.1 – SC 4.1.2 (Name, Role, Value)** | [W3C WCAG 2.1](https://www.w3.org/TR/WCAG21/#name-role-value)                                             | All UI components must expose name, role, and state programmatically. |
| **ARIA Authoring Practices Guide (APG)**    | [WAI-ARIA APG](https://www.w3.org/WAI/ARIA/apg/)                                                          | Provides recommended patterns for roles, states, and properties.      |
| **Section 508 (US)**                        | [Section 508](https://www.section508.gov/manage/laws-and-policies/)                                       | Requires accessible applications using ARIA when needed.              |
| **EN 301 549 (EU)**                         | [EN 301 549](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/03.02.01_60/en_301549v030201p.pdf) | Requires compliance with WCAG 2.1, including ARIA.                    |

