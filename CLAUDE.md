# studio10a.com — web desk

Static site (GitHub Pages, custom domain via Cloudflare DNS/cache). `index.html` = studio home (story, Room 10A, services); `voicesuite.html` = Voice Suite product page; `assets/voicesuite/` = screenshots, cover, `manual.pdf` (the **Help** guide - file name stays `manual.pdf`). Push = publish; only push when asked.

## Working
- Local preview: launch.json config "site" (python http.server on :8735) - verify there, not via file://.
- Live check after a push: `curl -s "https://studio10a.com/voicesuite.html?v=$RANDOM" | grep ...` in an until-loop; Cloudflare refreshes in ~30 s.
- Theme: dark default, toggle stored in localStorage `s10a-theme`, synced across pages; screenshots come in pairs `.shot.if-dark` / `.shot.if-light`. The Browser pane's mobile preset force-darkens light pages (artifact) - judge at desktop width.
- Screenshots of the plugins: dark/light via the harness snapshot tools in the voice-suite repo (`S10A_NO_SPLASH=1 UISnapT|UISnapVT out.png 1280x760`; light = `ui.darkMode` 0 in the suite settings file, then restore 1).

## Copy rules
- Voice: plain, producer to producer. "Free, coffee optional" / "buy us a coffee" - never "donation / donationware". Tagline exactly **"Sounds better"**. **Help / help guide**, never "manual". Room 10A: **Gautham**, **Naveen**.
- Claims: VoiceLab clip mode = ARA2 hosts (Studio One, Cubase, Nuendo, REAPER, Cakewalk). VoiceLab Track + TextLab = any VST3/AU host incl. Logic Pro, GarageBand. No AAX / Pro Tools. Enhance = user's own free Gemini/Groq key; same ElevenLabs per-character pricing as the website (say "saves credits", never "cheaper").
- Version strings (update each release): hero kicker "version x.y.z", spec row "Version", footer "vx.y.z · release notes" (the only release-notes link - keep it in the footer, low-key).

## Payhip
Listing payhip.com/b/rBIPg mirrors the site copy (title carries the version, description ends with "Version x.y.z (date)"). Edited through Saurabh's Chrome by the supervisor; files ≤10 MB can be uploaded by Claude, the Mac pkg cannot.

## Money
Domain / Cloudflare / tool costs are not kept here - one line into `~/Studio10A-Brain/Inbox.md` for accounts.
