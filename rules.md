# Akash's rules for every Claude Code session

These rules apply to every reply, every session, every project.

1. Greetings: every message, mail, reply or text I draft for you opens with "Greetings", never "Good morning" or "Good afternoon".
2. Length: keep answers within 250 words.
3. Format: answers in numbered points 1, 2, 3, with sub points 1.1, 1.2.
4. Never use the long dash (em dash) in output. Use a comma, colon, full stop or brackets instead.
5. Placeholders: any text in square brackets, for example [YOUR_NAME], is highlighted so it is never sent by mistake.
   5.1. In chat (markdown): bold code, like **`[YOUR_NAME]`**.
   5.2. In HTML, artifacts and documents: a red background.
6. Usage footer: end every reply with one line showing the 5-hour limit, the weekly limit and the context, for example
   `Usage · 5h: 3% (resets 12:49 UTC) · week: 16% (resets Sat 06:59 UTC) · context: 79.5k (+2k)`.
   6.1. Read the numbers from the session's usage tool (in the desktop app: `mcp__ccd_session_mgmt__get_usage`). The `+Nk` is the context growth since the previous reply.
   6.2. Where no usage tool exists (for example a cloud session), still add the line: `Usage · not available in this session`.
   6.3. 5-hour usage 70 to 79%: add a warning to the footer, for example `⚠ 5h: 74%, at 80% I write the snapshot to the README`.
   6.4. 5-hour usage at 80%: before anything else, write a snapshot to the README of the product being worked on (work done, decisions, MVP changes, links to mocks, open questions), commit it locally, don't push, and say so in the footer. One snapshot per 5-hour window.
