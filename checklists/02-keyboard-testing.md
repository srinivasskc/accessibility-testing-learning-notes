# Keyboard Accessibility – Accessibility Testing Notes

Keyboard accessibility means a user can navigate and use a website or app **only with a keyboard** (no mouse or touch). This is very important for users with motor disabilities, screen reader users, and even power users who prefer keyboard shortcuts.

## 🔹 Why Keyboard Accessibility Matters

* Many people cannot use a mouse due to motor or visual impairments.
* Screen reader users often rely on keyboard navigation.
* Helps power users work faster (Tab, Enter, Space, Arrow keys).
* Improves overall usability → if it works with keyboard, it usually works better for everyone.

## 🔹 How to Test Keyboard Accessibility

### ✅ Quick Steps

1. **Unplug your mouse / disable touchpad.**
2. Use only the **Tab**, **Shift+Tab**, **Enter**, **Space**, and **Arrow keys** to move around.
3. Try to access all interactive elements (links, buttons, inputs, menus).
4. Check that focus order is logical and visible.
5. Check that you can activate all actions with keyboard (e.g., submit forms, open dialogs).
6. Make sure you can exit pop-ups, modals, or dropdowns with **Esc** or standard keys.

## 🔹 Tools You Can Use

* **Tab key** → the simplest, most effective tool.
* **WAVE Toolbar** → highlights focusable elements.
* **axe DevTools** → reports missing keyboard access.
* **Accessibility Insights** (Microsoft) → keyboard checks included.
* **Screen readers** (NVDA, JAWS, VoiceOver, TalkBack) → combine with keyboard navigation.


## 🔹 Common Issues Found

* Elements not reachable by keyboard (no focus).
* Focus trap → stuck inside modal or popup.
* Missing visible focus indicator (you can tab, but don’t see where).
* Wrong focus order (jumps randomly on page).
* Custom controls (dropdowns, sliders) not keyboard accessible.
* Can’t dismiss modal with **Esc**.
* Some actions require mouse only (hover menus, drag-and-drop).


## 🔹 Quick Checklist

* [ ] Every interactive element is reachable with **Tab/Shift+Tab**
* [ ] Focus order is logical (follows visual reading order)
* [ ] Visible focus indicator is always present (outline or highlight)
* [ ] All actions can be triggered with **Enter/Space**
* [ ] Custom components (menus, sliders, dropdowns) are keyboard accessible
* [ ] No keyboard traps (can always tab away or use Esc to exit)
* [ ] Modals, dialogs, popups can be closed with **Esc**
* [ ] Tested with a screen reader + keyboard to confirm usability


## 🔹 Mapping with Accessibility Standards

| Standard / Guideline                              | Reference                                                                                                                       | What It Says About Keyboard Accessibility                                 |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| **WCAG 2.1 – Success Criterion 2.1.1 (Keyboard)** | [W3C WCAG 2.1](https://www.w3.org/TR/WCAG21/#keyboard)                                                                          | All functionality must be operable through a keyboard interface.          |
| **WCAG 2.1 – SC 2.1.2 (No Keyboard Trap)**        | Same as above                                                                                                                   | Users should not get stuck in one part of the content with keyboard only. |
| **Section 508 (US Govt.)**                        | [Section 508 Standards](https://www.section508.gov/manage/laws-and-policies/)                                                   | Requires full keyboard access for all functions.                          |
| **EN 301 549 (EU)**                               | [EN 301 549 v3.2.1](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/03.02.01_60/en_301549v030201p.pdf)                | Mirrors WCAG 2.1 requirements for keyboard accessibility.                 |
| **Android Accessibility Guidelines**              | [Android Dev Docs](https://developer.android.com/guide/topics/ui/accessibility)                                                 | Apps must support navigation with external keyboards.                     |
| **iOS Accessibility Guidelines**                  | [Apple HIG – Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility/overview/introduction/) | iOS apps should be operable with hardware keyboards and Switch Control.   |

