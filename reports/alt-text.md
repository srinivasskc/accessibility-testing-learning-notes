# ALT Text in Accessibility Testing

When we test for accessibility, one of the most basic and important checks is **ALT text** (Alternative Text). 

## What is ALT Text?

ALT text is used to describe images on webpage. For users who cannot see the image, screen readers will read out this description.

## Why is ALT Text Important?

* **For visually impaired users** → They can understand what the image means.
* **For low-bandwidth users** → When images fail to load, ALT text is displayed instead.
* **For SEO (indirect benefit)** → Search engines also use ALT text to understand image content.

If ALT text is missing or written poorly, then people who depend on **screen readers** cannot understand the purpose of the image. This directly impacts **inclusivity**.

A good ALT text helps users understand the **purpose** of the image, not just what it looks like.

## How to Test ALT Text

1. **Check if ALT text exists**
   * Inspect the HTML/DOM of the page → look for the `alt` attribute on `<img>` tags.

2. **Check if ALT text is meaningful**
   * Does it describe the purpose of the image?
   * Example: Instead of *“image123.png”*, write *“Scan Button”*.

3. **Test with a Screen Reader**
   * On iOS → VoiceOver
   * Navigate the screen and listen to how the image is read aloud.

4. **Check for redundancy**
   * Avoid repeating the same text multiple times (e.g., ALT text that just says *“button button”*).

5. **Check for max length for ALT Text**
   * There is no strict hard limit for HTML Spec.

| Source                           | Max Length Guidance                  |
| -------------------------------- | ------------------------------------ |
| **WCAG / W3C**                   | No strict limit; must be short       |
| **HTML Spec**                    | No maximum specified                 |
| **Screen Reader Behavior**       | Narration may chunk around 125 chars |
| **Accessibility Best Practices** | \~125–150 characters recommended     |


## Common Issues Found in ALT Text Testing

* **Missing ALT text** → Screen reader just says *“image”*.
* **Non-informative ALT text** → e.g., “pic1.jpg” or “icon.png”.
* **Overly long ALT text** → Too much detail confuses users.
* **Decorative images with ALT text** → Decorative images should have empty ALT (`alt=""`) so they are skipped.
* **Clickable images without ALT text** → Users will not know where the link goes.


## 🔹 Automated Tools for ALT Text Testing

### **1. WAVE (Web Accessibility Evaluation Tool)**

* **Type:** Browser extension & online tool
* **How it helps:** Highlights images without ALT text or with redundant/empty ALT.
* **Link:** [https://wave.webaim.org](https://wave.webaim.org)


### **2. LambdaTest Accessibility Testing Tool**

* **Type:** Browser extension (Chrome)
* **How it helps:** Automated accessibility scans → flags missing or non-descriptive ALT attributes.
* **Link:** [https://www.lambdatest.com/accessibility-testing-tools](https://www.lambdatest.com/accessibility-testing-tools)

### **3. axe DevTools (Deque)**

* **Type:** Browser extension (Chrome, Firefox, Edge)
* **How it helps:** Automated accessibility scans → flags missing or non-descriptive ALT attributes.
* **Link:** [https://www.deque.com/axe](https://www.deque.com/axe)


### **4. Lighthouse (Google Chrome DevTools)**

* **Type:** Built into Chrome (Audits → Accessibility)
* **How it helps:** Reports missing ALT text and other accessibility issues.
* **Link:** Open Chrome DevTools → “Lighthouse” tab
* **Reference:** [https://developer.chrome.com/docs/lighthouse/accessibility/scoring](https://developer.chrome.com/docs/lighthouse/accessibility/scoring)

### **5. Accessibility Insights**

* **Type:** Microsoft tool (desktop app & browser extension)
* **How it helps:** Automated and guided checks, including ALT text issues.
* **Link:** [https://accessibilityinsights.io](https://accessibilityinsights.io)


### **6. Screen Readers for Verification** *(Manual, but essential)*

* **NVDA** (Free, Windows)
* **JAWS** (Paid, Windows)
* **VoiceOver** (Built into macOS/iOS)
* **TalkBack** (Built into Android)


## 🔹 Pro Tip for Testers

* **Automated tools** → Catch **missing ALT** or empty attributes quickly.
* **Manual testing with screen readers** → Validate **quality & usefulness** of ALT text.
* **Hybrid approach** → Use both.


✅ Example workflow:

1. Run **axe DevTools** or **WAVE** on the page → list all images with missing ALT.
2. Use **NVDA** or **VoiceOver** to confirm how those images are read out loud.
3. Report issues: *“ALT text missing for logo image,”* or *“ALT text redundant: button button.”*


## Takeaway

As testers, we should not only check if ALT text exists, but also check if it is **useful, accurate, and helps the user**.
