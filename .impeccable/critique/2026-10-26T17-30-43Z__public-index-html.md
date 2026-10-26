---
target: the homepage
total_score: 25
max_score: 36
na_heuristics: 7
p0_count: 0
p1_count: 3
target_identity: "file:/Users/marcosrios/Documents/HelloRivers design-shop 2026/public/index.html"
target_fingerprint: "sha256:5df431b8eb2e4bded9b5668779ca0aed5ff1930e24a23eb325de13dd9532985b"
target_path: /Users/marcosrios/Documents/HelloRivers design-shop 2026/public/index.html
timestamp: 2026-10-26T17-30-43Z
slug: public-index-html
---
Method: dual-agent (A: design review · B: detector + browser evidence)

## Design Health Score

| # | Heuristic | Score | Key Issue |
|---|---|---|---|
| 1 | Visibility of System Status | 3 | Inline errors and post-submit status work; nothing says the button opens the email app |
| 2 | Match System / Real World | 3 | Plain first-person copy; "UX/UI design" still jargon for owners |
| 3 | User Control and Freedom | 3 | Menu exits work; mailto hand-off leaves the site |
| 4 | Consistency and Standards | 2 | Six different CTA labels to one form; b6 "See how it works" goes to #support; nav lacks How it works / Contact |
| 5 | Error Prevention | 3 | Good field types and defaults; mailto-only fails silently without a mail client |
| 6 | Recognition Rather Than Recall | 3 | Cards preselect the service |
| 7 | Flexibility and Efficiency | n/a | Single landing page |
| 8 | Aesthetic and Minimalist Design | 2 | Services listed 3 times (bento, support list, receipt); hosting pitched 4 times |
| 9 | Error Recovery | 3 | Specific, kind errors; cleared on first keystroke even if still invalid; layout shifts |
| 10 | Help and Documentation | 3 | FAQ covers cost, Spanish, hosting; nothing on timeline |
| **Total** | | **25/36** | **Acceptable (69%)** |

## Design Specificity Verdict

LLM: mostly authored (riso offset type, tape, receipt, graph-paper note, draggable wordmark, portrait, honest proof). Templated slip: six-card services bento with art on only two cards. "I stick around." is the most specific idea but the layout only supports it once.

Deterministic scan: CLI 8 findings. low-contrast (blue on #CC1479) false positive: never renders; all rendered text passes AA except aria-hidden riso decoration layers. cramped-padding on .setup-card refuted (48px padding). 6 hard-offset shadows intentional style. Browser overlay: 7 anti-patterns (6 shadows + 1 bounce easing on FAQ "+"). Structural: heading outline clean, all fields labelled, all imgs have alt, no overflow at 375. Tap targets under 44px on mobile: nav "Work with me", work-card buttons (40px), Copy (36px).

## Priority Issues

1. [P1] Mobile hero loses punch: fit-to-width headline renders ~44/44/31px at 375px; "I stick around." smallest line; portrait below the fold. Fix: re-break lines on mobile (e.g. "I stick" / "around."), raise per-line sizing, refit on orientation change. -> adapt / typeset
2. [P1] Offer repeated 3-4 times (bento 6, setup list 4, receipt 5; hosting 4x) stretching the page and burying monthly support. Fix: cut bento to 4 (fold social + hosting into monthly support), turn receipt into "What a month with me looks like", merge or drop the domain note. -> distill / layout
3. [P1] Spanish-speaking owner hits an English-only form at the commitment moment. Fix: Spanish line above the form pointing to WhatsApp, make "¡Se habla español!" a link (WhatsApp prefill in Spanish), WhatsApp first for that path. -> clarify
4. [P2] Mailto hand-off not announced; no reply-time line. Fix: microcopy under button "Opens your email app with this note ready to send"; add a realistic reply time only if Marcos confirms one. -> clarify / harden
5. [P2] CTA sprawl and wiring: six labels to one form, b6 CTA target mismatch, small tap targets (40px, Copy 36px), nav lacks How it works. Fix: standardize labels, rename b6 CTA "See monthly support", 44px min targets, add a nav link. -> polish

## Persona Red Flags

- Jordan: "UX/UI design" unexplained; 6 cards + 5 receipt items; no price anchor.
- Riley: mailto fails silently without a client; email error clears on first keystroke while still invalid; focused first invalid field scrolls its label under the fixed nav; error text inside label is read twice by screen readers.
- Casey: ~2,000px of bento before proof on mobile; "Ask me" wraps on the "Social media care" receipt row; "Live client site" tag covers Vanilla Bake logo; small tap targets.
- Doña Lupe (Spanish-speaking salon owner): English-only form; Spanish FAQ 4th and easy to miss; "Se habla español" is decorative, not a path; WhatsApp listed second.

## Minor Observations

- Header links lack a <nav> landmark.
- Invalid and focused fields look identical (both pink offset shadow).
- Paper grain overlay sits above the nav.
- Domain note floats left with dead space on desktop.
- Vanilla Bake preview shows Spanish copy; if it was built bilingual, say so (verify first).

## Questions to Consider

- If monthly support is why people hire you, why does a six-card menu of one-off services come first?
- What if "¡Se habla español!" opened a Spanish WhatsApp chat?
- Would a deeper Vanilla Bake story do more than any number of service cards?
