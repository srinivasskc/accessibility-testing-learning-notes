# ALT Text Testing Checklist

## 🔹 1. Presence of ALT Text

* [ ] Every **image** has an `alt` attribute (web) OR **contentDescription / accessibilityLabel** (mobile).
* [ ] No important image is missing ALT text.


## 🔹 2. Meaningfulness of ALT Text

* [ ] ALT text describes the **purpose**, not just the appearance.
* [ ] ALT text is **concise** (recommended under 125 characters).
* [ ] ALT text is **not redundant** with surrounding text.

## 🔹 3. Decorative Images

* [ ] Decorative or purely visual images have `alt=""` (empty) so they are skipped by screen readers.
* [ ] No decorative image uses misleading or unnecessary ALT text.


## 🔹 4. Functional Images (Links / Buttons)

* [ ] Clickable images (icons, logos) have ALT text that describes the **action**.
* [ ] ALT text does not repeat the role → avoid “button button.”


## 🔹 5. Consistency & Uniqueness

* [ ] Different images/icons have **unique ALT text** (not all labeled “icon” or “button”).
* [ ] Repeated elements (like multiple arrows) are either ignored (if decorative) or clearly distinguished (e.g., “Next slide,” “Previous slide”).


## 🔹 6. Testing with Tools

* [ ] Run **WAVE / axe DevTools / Lighthouse** to detect missing ALT text.
* [ ] Verify with **screen readers**:

  * NVDA (Windows)
  * JAWS (Windows, paid)
  * VoiceOver (macOS/iOS)
  * TalkBack (Android)
* [ ] Listen: Does the ALT text make sense in context?


## 🔹 7. Edge Cases

* [ ] ALT text is not overly long (no paragraphs — use captions or `aria-describedby` instead).
* [ ] Charts, graphs, or infographics have **long descriptions** elsewhere (not only ALT).
* [ ] Branding logos have ALT text that conveys the brand name.

✅ **Takeaway:** ALT text should answer the question:
👉 *“If I can’t see this image, what is the one thing I must know about it?”*
