# AI Usage Log: PIXEL MYSTERY (CAPTCHA reimagined)

**AI assistant:** Claude (Anthropic), chat interface
**Log started:** 23 Oct 2026
**Maintained by:** Claude, updated after each exchange. The team should add entries for work done in other tools.

## 1. Project summary
A CAPTCHA-inspired pixel puzzle game. One pixel-art scene is reused across four levels: (1) rebuild the image from pieces, (2) solve riddles by clicking objects, (3) spot a change, (4) spot the unusual situation. Runs in the browser with no backend.

## 2. Tools in the team workflow
| Tool | Used for | Logged by |
|---|---|---|
| Claude | Planning, prompts, starter code, documentation | This file |
| Pixel AI | Scene artwork | Team (add prompts and settings) |
| Sound AI | Sound effects | Team |
| Stitch | UI design (teammate) | Team |
| Antigravity | Level 1 logic, from prompts written with Claude | Team (add outputs and edits) |
| Replit | Hosting and testing | Team |

## 3. Interaction log
| # | Date | Request (summary) | What Claude produced | Status |
|---|---|---|---|---|
| 1 | 23 Oct 2026 | Design a playable CAPTCHA-style game about "what makes us human" | "Humanity Check": single-file browser game with 4 challenge types (draw circle, bouba/kiki, Müller-Lyer illusion, rhythm tap), 3 random per run, 30 s timers, pass/fail feedback, restart. Published as a web page. | Delivered. Not tested on real devices. |
| 2 | 23 Oct 2026 | Which human features bots lack, for CAPTCHA design | Advice list: motor imperfection, perceptual quirks, embodiment, subjective judgment, plus design cautions (accessibility, privacy, combine signals) | Advice only |
| 3 | 23 Oct 2026 | Workflow for a 3-level puzzle using Replit, Antigravity, Stitch, Pixel AI, Sound AI | Step-by-step pipeline (spec, art, audio, UI, build, host, test). Tool meanings were assumed and flagged. | Advice only |
| 4 | 23 Oct 2026 | Split the work among exactly 4 people | 4 roles with deliverables, handoffs and timeline | Advice only |
| 5 | 23 Oct 2026 | Explain Levels 1 and 2 from the Pixathon spec, with roadmap | Detailed explanation, state design, 10-step roadmap, common mistakes | Advice only |
| 6 | 23 Oct 2026 | Build the logic for Levels 1 and 2 | Starter project `pixel-mystery/` (index.html, style.css, script.js): 3-strip rebuild, 2-riddle hunt, hotspots in percent, scoring once per level, `?debug` mode | Delivered. **Not run in a browser.** Placeholder hotspots need real measurements. |
| 7 | 23 Oct 2026 | Best AI tool for Level 1 logic | Recommended Antigravity (code agent), Replit for run/deploy | Advice only |
| 8 | 23 Oct 2026 | Antigravity prompt for Level 1 with best piece count | Recommended 6 pieces (3x2) with reasoning; full prompt | Prompt delivered |
| 9 | 23 Oct 2026 | Same prompt, but UI is built by a teammate | Rewritten prompt: separate logic engine (`level1.js`, API and events), bare test harness, self-tests | Prompt delivered |
| 10 | 23 Oct 2026 | Next steps after pasting prompt | Review checklist, manual tests, handoff steps | Advice only |
| 11 | 23 Oct 2026 | Feature list for Level 2 | 25 features in priority groups, data needed, riddle tips | Advice only |
| 12 | 23 Oct 2026 | Create and maintain an AI log | This file | Delivered |
| 13 | 23 Oct 2026 | User shared localhost test page for Level 1 and asked for a fix prompt | Claude could not open the local page (it only runs on the user's machine). Provided a diagnose-then-fix prompt for Antigravity and asked for a screenshot or description of the problem. | Prompt delivered. Problem not yet identified. |
| 14 | 23 Oct 2026 | User uploaded screenshot of Level 1 test page showing errors | Read the screenshot: "Image failed to load" and "canvas.toDataURL is not a function". Diagnosed two separate causes (image path/file, and likely OffscreenCanvas or non-canvas object). Provided a targeted fix prompt. | Prompt delivered. Fix not yet confirmed. |
| 15 | 23 Oct 2026 | Fastest-result Antigravity prompt for Level 2 | One prompt covering a logic engine (`level2.js`), `hotspots.json`, `riddles.json`, a bare test harness with a hotspot calibration tool, and self-tests, based on the 25-feature list (entry 11). | Prompt delivered. Not yet run. |
| 16 | 23 Oct 2026 | User pasted Antigravity's report that the two Level 1 errors were fixed | Gave a verification checklist. Noted the fix is the agent's claim until the user confirms it on screen. | Awaiting user's test result |
| 17 | 23 Oct 2026 | Change Level 1 to 3 pieces only | Gave a one-line config change (COLS=3, ROWS=1), an Antigravity prompt to apply and re-test it, and noted the trade-off (only 6 orderings, 2 possible start states). Matches the Pixathon brief's exact-3-strips rule. | Not yet applied or tested |
| 18 | 23 Oct 2026 | Level 2 prompt for Antigravity with frontend and backend (game logic) | Single prompt: DOM-free logic engine (`level2.js`) plus a themed playable page (`level2.html`, `level2.css`, `level2-ui.js`), data files, a `?calibrate` hotspot tool, and self-tests. Replaces the logic-only prompt from entry 15 when a UI is wanted. | Prompt delivered. Not yet run. |
| 19 | 23 Oct 2026 | Request for the full AI log of the conversation | Re-issued this file with all entries 1 to 19. | Delivered |

## 4. Human vs AI contribution
- **Human (team):** Pixathon brief and four-level concept, scene artwork from Pixel AI, tool choices, role assignments, final testing and decisions.
- **AI (Claude):** Planning, prompts, starter code, feature lists, documentation.
- **Not yet done by anyone:** Levels 3 and 4, real hotspot measurements, sound, final UI integration.

## 5. Verification status
- Humanity Check and `pixel-mystery/` starter code were written but **not executed or tested by Claude**.
- Piece-count and difficulty figures (for example, solve times) are estimates, not measured results.
- Tool descriptions (Antigravity, Stitch, Pixel AI, Sound AI) were assumed and should be checked against current versions.

## 6. Open items
- [ ] Measure hotspots for the real scene
- [ ] Run the Antigravity-generated Level 1 and record test results
- [x] Antigravity prompt for Level 2 (entries 15 and 18)
- [ ] Confirm Level 1 fix and 3-strip change work (entries 14, 16, 17)
- [ ] Run Level 2 output and calibrate hotspots
- [ ] Levels 3 and 4
- [ ] Add team entries for Pixel AI, Sound AI, Stitch, Antigravity and Replit work
