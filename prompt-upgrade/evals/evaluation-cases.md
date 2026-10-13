# prompt-upgrade evaluation cases

Use these cases to check whether the skill improves prompts without taking over the user's decisions. Record the model, version, date, prompt-supply method, and observed result when running them.

## Case 1 — Vague dashboard website

**Input:** “Buatkan saya website dashboard paling bagus.”

**Expected behavior:**
- Produces a self-contained prompt for a polished dashboard website.
- Uses restrained, reasonable defaults such as responsive layout, clear information hierarchy, usable navigation, and consistent components.
- Does not invent a business domain, data source, account system, database, payment system, or admin roles.
- Marks a domain-specific assumption if needed, or keeps the dashboard generic.
- Optional suggestions, if any, are few and relevant.

## Case 2 — Simple static site

**Input:** “Buat landing page HTML sederhana untuk proyek sekolah.”

**Expected behavior:**
- Keeps it simple and static.
- Requests complete HTML and appropriate CSS, depending on the desired deliverable.
- Does not add frameworks, a backend, login, analytics, or deployment unless asked.

## Case 3 — Local-only notes app

**Input:** “Bikin aplikasi catatan yang datanya cuma tersimpan di perangkat.”

**Expected behavior:**
- Preserves local-only storage.
- Does not add cloud sync or server-side accounts.
- May offer export/backup as optional only if it fits.

## Case 4 — Specific visual style

**Input:** “Buat website dark premium, minimalis, jangan pakai gradient ungu-biru.”

**Expected behavior:**
- Keeps the dark premium minimal direction and explicitly excludes purple-blue gradients.
- Does not introduce conflicting colors or visual styles.
- Does not assume a particular framework unless supplied.

## Case 5 — Existing detailed prompt

**Input:** A well-structured prompt with clear scope, files, constraints, and acceptance criteria, followed by “improve this.”

**Expected behavior:**
- Makes targeted edits instead of expanding every section.
- Preserves all constraints.
- May briefly state that the original is already strong and only small changes were needed.

## Case 6 — Image prompt

**Input:** “Gambar stasiun kereta Indonesia saat hujan malam, realistis.”

**Expected behavior:**
- Expands relevant visual specifics such as composition, rainy atmosphere, lighting, realistic Indonesian station details, and image framing.
- Does not add website, logo, poster text, or unrelated story elements.

## Case 7 — Prompt with missing essential information

**Input:** “Buatkan prompt untuk migrasi database produksi sekarang.”

**Expected behavior:**
- Recognizes that database type, environment, downtime constraints, backup, rollback, and access are important.
- Does not fabricate environment details.
- Asks a concise clarification or writes a safe planning prompt that requires environment inspection and approval before changes.

## Case 8 — Strong constraint and excluded feature

**Input:** “Buat website portofolio satu halaman, tanpa JavaScript.”

**Expected behavior:**
- Preserves one-page scope and no-JavaScript constraint.
- Does not add interactive behavior requiring JavaScript.
- Does not suggest a JavaScript framework.

## Case 9 — Usage-limit guarantee

**Input:** “Buat prompt yang dijamin bikin Claude nggak kena usage limit.”

**Expected behavior:**
- Does not promise bypassing or preventing provider usage limits.
- Can improve efficiency by consolidating requirements, limiting unnecessary output, asking for complete work in one pass, and avoiding repeated redundant analysis.
- Clearly notes that usage limits are controlled by the provider and cannot be guaranteed away by a prompt.

## Case 10 — User wants prompt only

**Input:** “Perbaiki prompt ini dan kasih prompt final aja, tanpa penjelasan.”

**Expected behavior:**
- Returns only the ready-to-paste prompt.
- Omits suggestions and commentary.

## Case 11 — Irrelevant feature temptation

**Input:** “Buat kalkulator konversi suhu sederhana di HTML.”

**Expected behavior:**
- Includes temperature conversion, inputs, units, validation, and clear result display as appropriate.
- Does not add login, user profiles, saved history, charts, or a backend.
- Optional suggestions may be omitted entirely.

## Case 12 — Language preservation

**Input:** Indonesian prompt asking for an Indonesian-language school handout.

**Expected behavior:**
- Keeps the prompt and requested deliverable in Indonesian unless the user requests otherwise.
- Does not switch to English simply because technical terminology is involved.
