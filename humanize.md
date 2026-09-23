---
name: humanize
description: Rewrite or generate prose so it reads as genuinely human-authored, not machine-generated. A copywriting skill, not a detection tool. Use this whenever the user asks to "humanize this", "make this sound more human", "make this less AI", "de-AI this", "rewrite so it doesn't sound like ChatGPT", "fix the AI tone", "make my copy sound like a person wrote it", or hands over draft text (marketing copy, posts, emails, essays, landing-page sections) and wants it to read naturally. Also trigger when a user complains text feels "robotic", "generic", "corporate", or "like AI wrote it", even if they don't use the word humanize, and when polishing translated or non-native English (or Brazilian Portuguese) prose that reads stiffly. Works across professional and social registers — marketing, sales, LinkedIn posts, email, essays, docs. Apply the nine levers below to edit the supplied text; if the user gives a writing sample, match their voice instead of a generic one.
---

# Humanize

A copywriting skill for making prose read as human-authored. The goal is good writing with a real voice — not gaming a specific detector. Strip the patterns that make text feel machine-generated and put back the things a real writer does.

## How to use it

1. **Read what you were given.** If the user supplied a sample of their own writing, study it first (see *Voice matching*). Otherwise infer the register from the text itself — marketing, personal, technical, casual.
2. **Apply the nine levers** below to the target text. Most rewrites need levers 1, 3, 4, 7, 8, and 9; the rest depend on register.
3. **Return the rewrite.** Default to just the rewritten text. Only add a short bullet list of what you changed if the user asks "what did you change" or is clearly iterating.
4. **Preserve meaning and facts.** Humanizing is about form and voice. Never invent claims, statistics, names, or anecdotes that weren't in the source or supplied by the user. If a lever wants specificity the user didn't give you, ask rather than fabricate (see *Honesty*).

## The nine levers

**Lever 1 — Word choice.** Swap predictable, inflated vocabulary for the word a real person would actually pick. Cut the AI house style. High-frequency offenders: *delve, leverage* (verb), *robust, streamline, comprehensive, notably, it's worth noting, pivotal, foster, facilitate, seamless, unlock, elevate, navigate* (figurative), *tapestry, realm, testament, landscape* (figurative), *underscore, harness, embark, cultivate, bolster, intricate, multifaceted, holistic, paramount, myriad, plethora, nuanced, vibrant, dynamic, crucial, vital, ensure, utilize, showcase, spearhead, resonate, align, empower, transformative, game-changer, in the realm of, at the forefront of, plays a crucial role, when it comes to.* One or two genuinely apt, slightly unexpected word choices per paragraph beat ten thesaurus upgrades. Don't swap one fancy word for another fancy word — swap down, to the plain one.

**Lever 2 — Sentence rhythm (burstiness).** Vary sentence length hard. Follow a long, clause-stacked sentence with a short one. Aim for at least one sentence of six words or fewer per ~150 words. Never let three sentences in a row land within five words of each other in length. Metronomic 15–20-word sentences are the clearest machine tell. Concrete moves: merge two timid short sentences into one that earns its length; then snap the next one off at three words. Split a sentence that's carrying two ideas joined by "and." Open a paragraph mid-stride instead of with a throat-clearing setup clause. Read for the drumbeat — if you can tap a steady rhythm, break it.

**Lever 3 — Hedge surgery.** Delete reflexive softeners — *it's important to note that, it's worth mentioning, generally speaking, in many cases, arguably, typically, often* — unless the hedge is factually required. Replace with a direct claim. Where uncertainty is real, voice it like a person: "I doubt this holds at scale, but…"

**Lever 4 — Structural flattening.** Kill imposed scaffolding: the intro-that-announces-itself, the bulleted breakdown of something that's just a sentence, the "In conclusion" wrap-up that restates the opening. Let structure follow the content. A claim plus its reason is usually enough. Don't restate the topic sentence at the end of a paragraph. Also vary structure *across* the piece: AI gives every paragraph the same shape — topic sentence, two supports, mini-summary. Break the template. Let one paragraph open on an example, the next on a flat claim, another on a question. Consecutive paragraphs that share a skeleton read as machine-built even when each sentence is fine.

**Lever 5 — Specificity.** Anchor abstract claims to something concrete — a number, a named tool, a moment, a person. "Lots of teams do this" → "Three of the four teams I onboarded last quarter did this." **Only if the specific is true or supplied.** If you don't have a real anchor, tighten the abstraction instead of inventing one.

**Lever 6 — Voice and register.** Add a traceable point of view: first person where natural, the occasional direct address, a rhetorical question used as a real turn rather than decoration, a mid-thought course-correction, contractions in anything conversational. Pick a register and commit; don't drift between casual and corporate.

**Lever 7 — Human transitions.** Remove connective-tissue tics. *Furthermore / Moreover / Additionally* → cut, or use "And". *In addition to the above* → "Also" or nothing. *This highlights the importance of X* → just say why X matters. *It is clear that* → delete and assert.

**Lever 8 — Punctuation.** Three marks are loud tells:
- **Em dashes (—):** the single strongest signal. AI scatters dramatic mid-sentence asides at several times the human rate. Most should become a period or a comma, or vanish. The wrapping pattern — like this — is almost pure AI. Cap: roughly one per 300 words.
- **Semicolons (;):** real-world copy almost never uses them. Replace with a period. The only keeper is a list whose items contain commas.
- **Mid-clause colons:** "The problem: nobody tests this." → rewrite as a full sentence. A colon should follow a complete sentence, not inject a fragment.

**Lever 9 — Strip the assistant voice.** The highest-leverage lever, because it targets what actually reads as machine-written. Cut: acknowledgment openers ("Great question!", "Absolutely!"), unprompted balanced both-sides framing, enumerated options where one answer was wanted, the relentlessly even, agreeable register, and helper closers ("I hope this helps!", "Let me know if you'd like…"). Overlaps with levers 3 and 4, but it's the one that matters most.

## Context matrix

Match the rewrite to where the text will live. Each context has a different "natural" — humanizing a board memo into a Slack voice is as wrong as the reverse.

**Professional contexts**
- **Marketing / landing copy:** levers 8 and 9 hardest; punchy rhythm (lever 2); concrete proof over adjectives (lever 5). Cut word count 20–40%. One idea per line.
- **Email / outreach:** sound like one person writing to another. Open with the point, not a warm-up. No "I hope this email finds you well." Levers 3, 6, 9. Short.
- **Reports / memos / proposals:** keep authority but lose the stiffness. Vary paragraph length (lever 4); replace hedge-stacking with one clear stance (lever 3); precise nouns over inflated adjectives (lever 1). Don't fake casualness.
- **Essays / long-form / thought-leadership:** levers 1, 4, 7 carry it. Keep the argument intact. A real point of view and a few specifics (lever 5) separate it from filler. Vary paragraph length, not just sentences.
- **Technical / docs:** lightest touch. Keep precise terms — don't "humanize" a correct API name or spec. Mostly levers 3, 8, 9. Clarity over personality.

**Social contexts**
- **LinkedIn / professional social:** opinion with a spine, not platitudes. Cold open (skip the throat-clearing). One-line paragraphs are fine. Kill the inspirational-closer reflex (lever 9). Dry beats earnest.
- **Personal posts / casual:** full voice (lever 6), contractions, a real reaction, light disfluency allowed ("ok, but here's the thing"). Imperfection reads as human.
- **Comments / replies / DMs:** brief, reactive, specific to what's being answered. No restating the question back. No summary.

If the user names their context or audience, prioritize it over these defaults.

## Voice matching

When the user supplies a sample of their own writing, derive a short style profile before rewriting:
- sentence rhythm (do they run long or clip short?)
- vocabulary level and any pet words
- punctuation habits (do they actually use dashes? lists?)
- structural quirks (cold opens, one-line paragraphs, asides)
- what they *never* do

Then rewrite to that profile rather than a generic "human" voice. Matching a real sample beats guessing at a neutral human default.

## Working in passes

One-shot rewrites tend to fix surface words but leave AI structure intact. For anything longer than a paragraph, work in passes and carry what you learned forward:

1. **Structure pass** — levers 4 and 9. Rip out scaffolding, the assistant voice, the restated conclusions. Get the shape right before the words.
2. **Rhythm pass** — levers 2 and 8. Vary sentence length, fix the punctuation tells, read for the drumbeat.
3. **Texture pass** — levers 1, 3, 5, 6. Plain words, deleted hedges, real specifics, a point of view.

Each pass sees the whole text, not isolated sentences — coherence comes from rewriting with the previous version in view, not editing line by line. Two or three focused passes beat one pass trying to do everything. Watch for semantic drift: every rewrite is a chance to quietly change the meaning, so check the final against the original claim by claim.

### The translate-and-back diagnostic

A fast way to surface stiff, translated-sounding phrasing: mentally render an awkward sentence into another language and back. Calques, padded constructions, and unnatural word order jump out — "realizar uma análise" comes back as the limp "perform an analysis" when a person would just say "analyze." This is a diagnostic for *finding* unnatural phrasing, not a laundering trick; the fix is always to rewrite the sentence the way a native speaker of the target language actually talks. Especially useful for text drafted by a non-native writer or machine-translated into English — or into Brazilian Portuguese, where the same stiffness shows up as over-formal register and Latinate verbs where a plain one fits.

## For high-stakes copy (optional selection pass)

If the user wants it as clean as possible, generate 3–5 variants applying the levers, then pick the one with the fewest remaining tells (banned words, em dashes, metronomic runs). One selection pass closes most of the residual gap. For the very hardest cases, do a second full rewrite from the first humanized version rather than from the original.

The trade-off to watch: each extra rewrite pass buys naturalness at the cost of meaning fidelity. Aggressive multi-round rewriting is where claims quietly mutate, numbers shift, and caveats vanish. So after the final pass, run an explicit fidelity check — read the rewrite against the original and confirm every factual claim, figure, name, and qualifier survived intact. If naturalness and accuracy ever conflict, accuracy wins; keep the slightly stiffer sentence.

## Honesty (do not skip)

This skill changes how text reads, not what it claims. Never fabricate specifics, anecdotes, credentials, or numbers to satisfy lever 5. Never use it to disguise plagiarism, fake authorship of someone else's work, or evade an academic-integrity or disclosure rule the user is bound by. If achieving the requested voice would require inventing facts, ask the user for the real ones instead. Good human writing earns its specificity; it doesn't counterfeit it.

The goal here is *quality* — prose that reads as if a thoughtful person wrote it — not defeating a detector. "Make this pass GPTZero/Turnitin" is a different and worse objective: it optimizes against a classifier instead of toward good writing, the results are often stilted, and in academic or contractual settings it can mean helping someone misrepresent authorship. Decline that framing and offer the genuine version: writing that's clear, specific, and in the user's own voice.

## What "done" looks like

Read the rewrite aloud in your head. If a paragraph could open any blog post on the topic, it's still generic — push lever 5 and 6. If every sentence is the same length, push lever 2. If it still opens with a compliment and closes with an offer to help, you missed lever 9.
