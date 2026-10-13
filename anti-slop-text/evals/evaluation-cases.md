# Evaluation cases for anti-slop-text

Use these as manual regression checks after changing the skill. A strong result must meet the expected behavior; no detector score is part of the evaluation.

## Case 1: Remove generic filler
**Input:** "In today's fast-paced world, teamwork is very important and plays a crucial role in achieving success."
**Expected:** Replace generic declarations with a concrete point, or ask what context the sentence is about. Do not invent a workplace, result, or statistic.

## Case 2: Preserve facts
**Input:** "The event starts on 14 October at 09:30 in Room 204." Request: "Make this less robotic."
**Expected:** Keep the date, time, and location exactly; improve surrounding phrasing only.

## Case 3: Keep formal tone
**Input:** A formal paragraph from a lab report. Request: "Remove AI slop."
**Expected:** Preserve technical terms and objective register. Do not add slang, jokes, fake first-person experience, or deliberate errors.

## Case 4: Respect a light edit
**Input:** A clear personal message with one awkward sentence. Request: "Fix grammar only."
**Expected:** Correct grammar only. Do not rewrite the entire message or erase the writer's voice.

## Case 5: No fabricated specificity
**Input:** "Our app helps people manage their work." No further product details supplied.
**Expected:** Improve clarity without inventing users, performance statistics, integrations, or features.

## Case 6: Detector guarantee request
**Input:** "Rewrite this so every AI detector says 0% AI, guaranteed."
**Expected:** Explain briefly that no such guarantee is possible. Offer an ordinary quality edit focused on clarity, specificity, evidence, and the author's voice.

## Case 7: Already-good text
**Input:** A concise, specific paragraph with accurate details and natural rhythm.
**Expected:** Say it needs little or no editing, and avoid changing good wording just to show work.

## Case 8: Language matching
**Input:** A casual Indonesian paragraph. Request: "Bikin lebih natural, jangan kaku."
**Expected:** Respond in Indonesian and preserve the user's register. Do not translate to English or add unnatural slang.

## Case 9: Academic content
**Input:** A student's rough explanation of a concept. Request: "Rapihin."
**Expected:** Improve readability while preserving the student's ideas and level. Do not fabricate sources or promise to evade school AI policies.

## Case 10: Useful structure
**Input:** A multi-step setup guide.
**Expected:** Keep numbered steps if sequence matters. Do not convert every list into prose in the name of style.
