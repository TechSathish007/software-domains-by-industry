# Contributing

Thanks for wanting to improve **Software Domains by Industry**. This is a reference guide, so the bar is accuracy and clarity rather than feature count.

## Ways to help

- **Fix a mistake** — a wrong fact, a stale example, a typo, a broken link.
- **Sharpen an India example** — name the real product, scheme, or regulator and say what makes it distinctive.
- **Add depth** — a hard problem the entry misses, or a more representative stack.
- **Improve accessibility or performance** — the page should stay usable on a low-end phone.
- **Suggest a new domain** — keep the list at 72 only if a change is a genuine swap; otherwise open an issue to discuss scope first.

## Making a change

The whole project is a single file, `Software_Domains_by_Industry.html`. All content lives in one JavaScript array:

```js
const DATA = [ /* one object per domain */ ];
```

Each entry has the same shape:

| Field | Type | What it holds |
|-------|------|---------------|
| `id` | string | URL-safe slug, also the anchor (`#fintech`) |
| `num` | string | Display number, `01`–`72` |
| `title` | string | Domain name |
| `tag` | string | One-line summary on the card |
| `def` | string | Definition — what the software is |
| `covers` | string[] | Sub-areas the domain spans |
| `hard` | string | What makes the engineering hard |
| `india` | string | How it plays out in India, with named examples |
| `stack` | string[] | A representative technology stack |
| `one` | string | The single thing worth remembering |

### Steps

1. **Fork** the repository and create a branch (`fix/upi-settlement-note`).
2. **Edit** the `DATA` array (or the surrounding HTML/CSS/JS if the change is structural).
3. **Check it in a browser** — open the file locally and confirm the card, search and detail view still work. There is no build step and no test suite; the browser is the test.
4. **Open a pull request** with a short description: what changed, why, and a source for any factual claim.

## House style

- **Concrete over abstract.** Say what the software does, not what it "enables".
- **Honest about difficulty.** If something is hard, say why — regulation, adversarial users, latency, safety.
- **India-first examples.** Prefer Indian regulators, rails, and companies where they exist (RBI, NPCI/UPI, Aadhaar, SEBI, TRAI, and so on).
- **Cite authorities for facts.** Government portals and regulators over blog posts. If you state something time-sensitive, add a source in the PR.
- **Keep entries comparable.** Every domain uses the same fields and roughly the same depth.

## Images

If you add a cover image, use an **openly licensed** one (Creative Commons or public domain) from a source such as Wikimedia Commons, and add its attribution and licence to the **Sources & methodology** section in the page. Do not add images you cannot license.

## Licensing of contributions

By contributing, you agree that your contribution is licensed under the project's [MIT License](LICENSE), and that you have the right to submit it.
