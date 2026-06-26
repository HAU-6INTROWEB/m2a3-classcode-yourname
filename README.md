# Module 2 – Activity 3 – Your Portfolio: Styling From Your Design System

Your portfolio now has structure (Activity 1) and a projects grid (Activity 2).
The last step is the **visual layer** - applied using **only your design system
from Week 2**. This is your high-fidelity deliverable, for real.

A design system just means: **decide your values once, then reuse them.** No new
syntax today - your "system" is a short **legend** at the top of `styles.css`,
and your job is to follow it everywhere.

## What to do

### 1. Fill in your details

Open `student.json` and fill in every field (keep it **identical** to your other
activities; the `classCode` must match your repo name):

```json
{
  "classCode": "1234",
  "fullName": "Juan Dela Cruz",
  "studentNumber": "2026-12345",
  "studentEmail": "juan.delacruz@hau.edu.ph",
  "personalEmail": "juan@example.com",
  "githubAccount": "juandelacruz"
}
```

### 2. Apply your system

> **Work in the [`src/`](src/) folder.** Everything else is course plumbing -
> leave it alone.

This activity ships with a **starter**: [`src/index.html`](src/index.html) is a
portfolio shell that already uses the component classes `.nav-link`, `.btn`, and
`.card`, and [`src/styles.css`](src/styles.css) has a **legend block** ready to
fill plus the components **partly styled as a worked example** (a few values
done, the rest left as `TODO`).

> **Bring your own portfolio:** replace the shell's placeholder content with your
> Activity 2 page. Just keep the `.nav-link`, `.btn`, and `.card` classes.

1. Fill in the **system legend** at the top of `styles.css` - your real values
   from Week 2 (background, text, primary, accent, type sizes, spacing, fonts).
2. Finish styling the component classes (`.nav-link`, `.btn`, `.card`) using
   **only values from your legend**. The rule to live by: **if a value is not in
   your legend, it does not go in the file.**
3. Apply the Week 2 rules: **60-30-10** (neutral dominates, accent only on
   buttons/links/key actions), a **2–3 size** type scale, and an **8-point**
   spacing scale.
4. Check **contrast**: body text at least **4.5:1** against its background. Run
   questionable pairings through the WebAIM Contrast Checker.

> **Style by class, not by element.** Put shared styling on `.card` once, so
> every card inherits one rule. **Minimal means minimal** - no extra colours or
> decoration outside your system. You are graded on **system discipline**, not
> flourishes.

> **Heads up:** real systems store these values as variables (`:root` + `var()`)
> so one change updates everything - you'll meet that later. For now, your system
> is the legend at the top of the file.

## Set up your repo

1. **Create from the template** - *Use this template → Create a new repository*.
2. **Owner = the `HAU-6INTROWEB` course org.**
3. **Name it** `m2a3-<classcode>-yourname`. The `<classcode>` must match
   `student.json`.
4. **Make it Private.**

```bash
git clone https://github.com/HAU-6INTROWEB/m2a3-<classcode>-yourname.git
cd m2a3-<classcode>-yourname
```

## Running the tests

```bash
npm install
npm test
```

This activity is graded by **9 tests** (1 point each). They check:

- ✅ `styles.css` is linked and has rules in it
- ✅ no inline `style=""` attributes
- ✅ a system-legend comment block is kept at the top of `styles.css`
- ✅ the `.nav-link` component is styled
- ✅ the `.btn` component is styled
- ✅ the `.card` component is styled
- ✅ colour, type (`font-family`), and spacing are applied
- ✅ the page actually uses the `.nav-link`, `.btn`, and `.card` classes
- ✅ `student.json` is completely filled in

The tests check that you styled by class with real values; **60-30-10,
contrast, and overall discipline are judged from the page preview.**

## Confirm your submission

When your tests pass locally, **commit and push**:

```bash
git add -A
git commit -m "Activity 3 complete"
git push
```

Pushing triggers the **Autograde** workflow. Open the **Actions** tab, then the
latest **Autograde** run, and confirm the green ✅ check, the "9 / 9 tests
passed" summary, and the 📸 page-preview link.
