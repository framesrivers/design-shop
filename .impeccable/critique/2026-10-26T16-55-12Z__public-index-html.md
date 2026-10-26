---
target: the homepage
total_score: 19
max_score: 32
na_heuristics: 7,10
p0_count: 1
p1_count: 3
target_identity: "file:/Users/marcosrios/Documents/HelloRivers design-shop 2026/public/index.html"
target_fingerprint: "sha256:6e0d69f7c16b3cff0b853728db750cdbfe6efb9554297599f909fd1e5dc7e99c"
target_path: /Users/marcosrios/Documents/HelloRivers design-shop 2026/public/index.html
timestamp: 2026-10-26T16-55-12Z
slug: public-index-html
---
Method: dual-agent (A: design review · B: detector + browser evidence)

## Design Health Score

| # | Heuristic | Score | Key Issue |
|---|---|---|---|
| 1 | Visibility of System Status | 2 | Form status is blue text under the button only; no field highlighting, no aria-invalid, error never clears after a fix |
| 2 | Match System / Real World | 3 | Receipt and steps metaphors land; "UX/UI", "scheduling-ready content" are jargon for a salon owner |
| 3 | User Control and Freedom | 3 | Menu closes on Esc/outside click; mailto hand-off is a one-way exit with no fallback |
| 4 | Consistency and Standards | 2 | "I" vs "we" voice; pink = "See services" in hero but "Start a project" elsewhere; service names vary (Hosting + care / + domains / site care) |
| 5 | Error Prevention | 2 | Whitespace-only name passes; nothing warns webmail users mailto may do nothing |
| 6 | Recognition Rather Than Recall | 3 | Cards preselect the service in the form (good, but invisible) |
| 7 | Flexibility and Efficiency | n/a | Single-page marketing site |
| 8 | Aesthetic and Minimalist Design | 2 | Service list repeated 4-5 times (bento, support list, receipt, contact intro, select, FAQ) |
| 9 | Error Recovery | 2 | Messages are friendly and specific but not tied to a field or styled as errors |
| 10 | Help and Documentation | n/a | Landing page; FAQ covers it |
| **Total** | | **19/32** | **Acceptable (59%)** |

## Design Specificity Verdict

LLM: visual system is authored (riso inks, misregistered elastic type, receipt, taped form, torn note, handwriting); content is interchangeable. Copy could belong to any freelancer, bento is a standard services grid, the person behind "I" never appears, voice is playful only visually, and the differentiator (monthly support) is buried as bento card 4.

Deterministic scan: 15 findings. Confirmed: low-contrast x4 (blue on pink CTA 2.85:1; pink on paper 2.49:1 on "one less thing!"; #5a6ba8 on paper 4.13:1 across section intros, steps, contact intro), skipped-heading (h1 -> h3 bento). Browser also found pink labels failing on yellow/white/pink cards (2.3-2.95:1) and two stragglers. False positives: cramped-padding x2 (padding lives on child), dark-glow, text-overflow (0x0 render), shape-assembled-illustration (not reproduced). Hard-offset shadows x6 are the intentional print style.

## Priority Issues

1. [P0] Inquiry depends entirely on mailto and the address is never shown on the page. Webmail users click "Write email" and nothing happens, yet get "your email app should open". Fix: show the address visibly with copy button in contact + footer, "Didn't open? Email me at..." fallback, consider a real form endpoint (Cloudflare Worker). Confirm the address (code comment says "Confirm this address before publishing"). -> clarify / harden
2. [P1] No human and no proof: full-width "Coming soon" plus an anonymous "I". Fix: show Vanilla Bake as one labelled real project beside a smaller "more on the way" card; add "Hi, I'm Marcos" block with photo/location. -> layout / clarify
3. [P1] Differentiator buried and hero CTA hierarchy inverted. H1 sells commodity services; pink primary is "See services" not "Start a project"; right half of hero empty at desktop. Fix: lead with the relationship, swap button weights, use the right column for a monthly-support teaser. -> clarify / layout
4. [P1] Contrast on primary CTAs (2.85:1) and secondary text (4.13:1), pink labels on cards (2.3-2.95:1). Fix: darker pink (#CC1479 already used on .b1) behind blue text or white text; darken --soft to ~#4A5A96; darker pink for small labels. -> colorize / polish
5. [P2] Form states and 9-option service select; footer wordmark broken (space collapses to "HELLORIVERS", only shrinks so it fills half width). Fix: field-level errors, trim values, 5 options, outcome-named button; fix wordmark spacing/fit. -> harden / polish

## Persona Red Flags

- Jordan (first-timer): "UX/UI support." in H1 means nothing; 9-option select forces a taxonomy choice; no price signal anywhere.
- Riley (stress tester): whitespace name passes; error never clears; mailto success message is false when no mail app; --content-space declared twice; ~135 lines of dead shop/template CSS; no Contact link in nav.
- Casey (mobile): ~8,350px page, contact at ~7,100px, no sticky CTA; hosting note copy 11.25px; "one less thing!" arrow detached; six 270px bento cards before any proof.
- Lucía (Spanish-speaking salon owner): no Spanish anywhere, not even "Se habla español"; jargon survives auto-translate poorly; no language preference in form; no phone/WhatsApp option.

## Minor Observations

- Domain note link has no visible action text; reads as decoration.
- H2s at display size take ~150px before thin content (Questions, Selected work).
- Receipt "Ask" column reads like price placeholders.
- Two stragglers: "support." alone in hero lede; "problem-solving." in support list.

## Questions to Consider

- If monthly support is why people hire you, why does the headline sell what every competitor sells?
- Is a big "Coming soon" more persuasive than one labelled Vanilla Bake case plus "more on the way"?
- What would one photo, one name and one line in Spanish do to inquiries?
