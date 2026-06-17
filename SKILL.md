---
name: football-match-comic
description: Turn football match reports, live blogs, scorelines, and user-provided match notes into fact-checked manga comic scripts, storyboards, and image prompts. Use for World Cup serial documentary comics, Champions League and domestic match recaps, derby or knockout drama, penalty shootouts, pre-match team departures, tournament chapters, non-uniform black-and-white Japanese football manga pages, key-moment extraction, captions, source-backed story outlines, and social-media slide comics.
---

# Football Match Comic

Create fact-checked football manga scripts from real football events. Support both single-match recaps and tournament-scale documentary comic series.

## Reference Router

Load only the reference needed for the task:

- Use `references/world-cup-comic-production-rules-v1.md` for tournament serials, World Cup documentary comics, social-media slide comics, 3:4 vertical pages, black-and-white Japanese manga style, visual bible rules, episode structure, and identity-text rules.
- Also use `references/world-cup-comic-production-rules-v1.md` for any single-match task that targets the social-media slide-comic style, staged fact/material research, identity anchors, or black-and-white non-uniform manga pages.
- Use `references/panel-template.md` when a reusable output skeleton is helpful for match cards, key nodes, page plans, manga page layouts, and prompt skeletons.

Keep `SKILL.md` as the execution entry point; keep detailed production rules in references.

## Modes

### Single Match Recap

Use for one completed or live match. Produce a compact match card, verified timeline, key beats, page plan, script, and prompts.

### Tournament Serial Event

Use when the user provides a tournament event point, such as "World Cup teams begin departing," "group stage upsets," "a host city prepares," "a star exits," or "final penalty shootout." Treat the event as one episode in a larger documentary comic. Follow `references/world-cup-comic-production-rules-v1.md`.

## Core Workflow

Default to staged execution unless the user explicitly asks for a fast one-pass output. Do not jump from fact research directly to storyboard and prompts when the user has not opted out of the supplement checkpoint or the pre-script adjustment checkpoint.

1. Identify the mode: single match recap or tournament serial event.
2. Use a dual-source research strategy: official sources establish facts; broader internet and Chinese media/platform sources surface visual, emotional, and public-discussion material. Do not let non-authoritative sources override official facts.
3. Verify real-world facts before scripting. Browse current sources for recent, live, just-finished, or high-stakes events. Prefer official competition pages, federation/club reports, reputable live blogs, stat providers, press conferences, and verified public posts for facts. In the same event-research pass, also run the Chinese media/platform discovery pass described below; do not postpone all Chinese-platform discovery until after the supplement checkpoint.
4. Stop after the fact package and ask whether the user has supplemental keywords, angles, screenshots, clips, player moments, fan reactions, or media hooks for a second search. Wait for the user's answer before building the material pool, unless the user explicitly requested a fast one-pass result.
5. Search broader sources for comic material when useful, including any user-supplied keywords: live photos, broadcasts, highlights, interviews, tactical analysis, media headlines, fan reactions, team social posts, and public discussion. Use these as material leads, not final fact authority.
6. Whenever online event/material research is performed, run a mandatory China platform material radar covering Weibo, Douyin, Xiaohongshu, and Bilibili alongside the official/authority search. Do this even if official/English-language research already found enough facts.
7. For tournament-wide or multi-team events, run a subject-level micro-event scan after the overview search. Overall tournament facts do not replace team-by-team, player-by-player, coach-by-coach, host-city-by-host-city, or ceremony-by-ceremony searches.
8. Separate confirmed facts from interpretation, public reaction, and manga expression. Mark uncertain details as assumptions or omit them.
9. Build a material pool, then select only elements that strengthen clarity, rhythm, or emotion. Do not add stadium, media, fan, tactical, or symbolic elements merely to make a page feel busy.
10. Extract the key beats. Prioritize goals, disallowed goals, red cards, VAR decisions, tactical swings, substitutions, saves, woodwork, stoppage time, extra time, penalties, qualification consequences, departures, arrivals, public ceremonies, and emotional turning points.
11. Build a story spine before page planning: protagonist pressure, dramatic question, suspense engine, turning-point staging, and aftertaste. Do not proceed if the spine only restates the match chronology.
12. Turn facts, selected material, and the story spine into an outline with a beginning, escalation, turning point, decisive moment, and aftertaste. Avoid news-feed summaries.
13. Choose page count by dramatic function before writing panels. Do not force too many beats into one page.
14. Stop before writing the final comic script and ask the user whether the story spine, selected materials, page count, page plan, tone, or visual focus should be adjusted. Include a concise recommendation and the tradeoffs of any obvious alternatives. Wait for the user's confirmation or requested changes before continuing, unless the user explicitly requested a fast one-pass output.
15. After the user confirms or adjusts the pre-script plan, write in Chinese by default unless the user requests another language.
16. Keep captions short and image-friendly. Preserve identity anchors: teams, key people, minute, score, and result when they matter.
17. Run a director pass after drafting the script and revise any page that reads like a match report instead of a staged manga sequence.
18. If generating images for non-commercial documentary/fan manga, preserve real football identity: national-team kit colors, recognizable patterns, player roles, hairstyles, posture, and known football body language are encouraged. Avoid sponsor logos, watermarks, and official tournament logo marks unless the user provides licensed assets or explicitly asks for them.

## Research Granularity

Use overview searches to establish the frame, then deliberately lower the search granularity for story material. A tournament-level search is good for dates, format, participants, and official consequences; it is weak for departure rituals, arrival images, ceremonies, team visits, political or cultural photo moments, locker-room material, local fan scenes, and short-video jokes.

For tournament serials, perform a micro-event scan before building the material pool:

- List the primary subjects that could carry the episode: teams, star players, coaches, host cities, fan groups, federations, public figures, ceremonies, transport moments, and training bases.
- Search at least the most story-relevant subjects individually, using specific verbs and scene nouns such as departure, arrival, welcome, send-off, airport, flight, ceremony, training camp, team photo, president, mayor, fans, chant, tears, family, luggage, bus, tunnel, and social post.
- Search both official/authority sources and social/video platforms for each subject when the episode is about atmosphere, departure, or public emotion.
- Keep a "micro-event radar" list with source, subject, scene, fact confidence, and manga value.
- If the first pass only returns schedules, groups, and formats, treat the material search as incomplete for a story-driven comic.

Use social platforms and short-video sources for story discovery, not final fact authority:

- Include platforms relevant to the audience and event, such as Weibo, Douyin, Xiaohongshu, Bilibili, TikTok, Instagram/Reels, YouTube Shorts, X/Twitter, Reddit, fan forums, and local-language sports communities.
- Extract hooks such as visual moments, jokes, chants, crowd mood, farewell rituals, arrival rituals, repeated comments, meme labels, and editing rhythms.
- Verify any concrete claim from these hooks through official accounts, original videos, reputable media, or multiple independent sources before presenting it as fact.

## China Platform Material Radar

Any task that involves online event or material research must include a China platform material radar. Run a first-pass radar during fact/material discovery, before the supplement checkpoint, then expand it after the user supplies keywords when needed. This is mandatory for match recaps, World Cup serial episodes, pre-match atmosphere, team departure/arrival stories, fan-reaction pieces, and social slide comics.

Search all four platforms separately:

- Weibo: hot-search wording, super-topic posts, federation or media posts, journalist posts, comment-section phrases, widely repeated jokes, and controversy tags.
- Douyin: short-video hooks, visible scene nouns, soundtrack/editing rhythm, comment memes, player-reaction clips, fan edits, and platform topic labels.
- Xiaohongshu: viewing-party context, city check-ins, outfit/kit culture, travel notes, fan diaries, venue guides, emotional personal posts, and visual lifestyle framing.
- Bilibili: explainer titles, fan edits, tactical videos, commentary phrases, compilation titles, danmaku-like repeated jokes when available, and long-form narrative angles.

Use platform-specific searches when direct app/search access is unavailable. Start with public web-index queries such as:

```text
site:weibo.com <event/team/player> <departure|arrival|airport|training|hot search|topic>
site:douyin.com/video <event/team/player> <出征|抵达|训练|热梗|世界杯>
site:xiaohongshu.com/explore <event/team/player> <观赛|打卡|机场|穿搭|训练基地>
site:bilibili.com/video <event/team/player> <大名单|出征|抵达|解说|复盘|热梗>
```

If web-indexed results are thin, state that limitation and still report the attempted platform radar. Do not replace the radar with generic web/news searches.

If the four platform-specific searches are thin or noisy, run a Chinese media fallback search in the same pass, using Baidu-style/open-web Chinese queries for CCTV, Xinhua, People's Daily, Sina, Sohu, Tencent, NetEase, The Paper, Dongqiudi, Hupu, and other relevant Chinese-language media or communities. This fallback supplements the platform radar; it does not replace the four-platform attempt.

Output the radar as a compact table or list with:

```text
platform
query or source
subject
scene/hook
fact confidence: confirmed / needs verification / social mood only
manga value
```

Treat China platform findings as material leads unless they come from verified official accounts or can be confirmed by authoritative sources. Concrete claims such as squads, injuries, departures, dates, quotes, scores, and disciplinary events must be verified before entering the fact package.

## Story Spine and Director Pass

Never write the final comic script immediately after fact extraction. Always produce a story spine first, then a pre-script plan and adjustment checkpoint, then draft the script, then run a director pass before prompts.

The story spine must answer:

- Protagonist pressure: whose emotional journey carries the comic?
- Dramatic question: what is the reader waiting to see resolved?
- Suspense engine: which moment should be slowed down instead of summarized?
- Turning-point staging: what must the reader feel before the decisive action?
- Aftertaste: what remains emotionally after the result?

The director pass must check:

- Camera placement: wide stadium, bench, crowd, player close-up, goalkeeper view, ball/boot inserts, or empty pitch.
- Silent panels: where waiting, hesitation, breath, or fatigue should replace action.
- Reaction panels: crowd, bench, goalkeeper, teammates, opponents, coaches, and scoreboard fragments.
- Delayed action: whether the decisive moment has enough setup to feel earned.
- Page purpose: each page must have a dramatic job, not just a list of events.

Revise before producing prompts if the script lacks suspense, reaction shots, page-level dramatic purpose, or visual rhythm.

## Pre-Script Adjustment Checkpoint

Before writing the final comic script, pause and ask the user to confirm or adjust the manga plan. This checkpoint is mandatory in staged execution after the material pool, selected materials, story spine, story outline, page-count judgment, and page plan are ready.

The checkpoint should include:

- Recommended page count and why it fits the dramatic function.
- A concise page-by-page plan with each page's dramatic job.
- The strongest recommended visual/emotional focus.
- Any risky compression, missing material, or optional alternative structure.
- A direct question asking whether to keep the plan or adjust page count, protagonist focus, tone, visual emphasis, or selected materials.

Do not include the final comic script, director pass, or image prompts until the user confirms or requests changes. If the user confirms without changes, continue from the confirmed plan. If the user requests changes, revise the plan first and ask for confirmation again when the changes materially alter the story structure.

## Output Shape

For staged execution, first produce only:

- Event point: the user's keyword, match, or episode topic.
- Fact sources: official or authoritative sources used to verify the event.
- Fact package: teams/people, date, venue, score/result when relevant, timeline, and consequences.
- Initial Chinese media/platform radar: first-pass Weibo, Douyin, Xiaohongshu, Bilibili, and Chinese-media fallback findings, clearly separated from verified facts.
- User supplement checkpoint: ask for optional keywords or material angles before the second search unless the user requested a fast one-pass output.

After the user answers the supplement checkpoint, continue with:

- Material sources: broader internet sources used for visual, emotional, tactical, or public-discussion material.
- China platform material radar: Weibo, Douyin, Xiaohongshu, and Bilibili findings, with fact confidence and manga value.
- Material pool: core event elements, environment, reactions, match-mechanism elements, symbols, and usable close-ups.
- Selected materials: explain which non-core elements are worth using and why.
- Story spine: protagonist pressure, dramatic question, suspense engine, turning-point staging, and aftertaste.
- Story outline: the distilled dramatic arc.
- Page-count judgment: explain why the event needs 1 page, 2-3 pages, 4-5 pages, or a split episode.
- Page plan: each page title, dramatic purpose, and covered beats.
- Pre-script adjustment checkpoint: ask whether the user wants to keep or adjust the story spine, selected materials, page count, page plan, tone, visual focus, or protagonist focus before the final script.

After the user confirms or adjusts the pre-script plan, continue with:

- Comic script: page number, panel role, scene, action, caption/dialogue, visual emphasis, and reading order.
- Director pass: note how the script uses camera placement, waiting, reaction shots, and delayed decisive action; revise weak pages before prompts.
- Image prompt: one prompt per manga page by default. Include cover prompts only for chapter covers, major events, social cover requests, or final collections.
- Boundary note: state what is factual and what is manga expression.

Use `references/panel-template.md` for a reusable structure.

## Tone Selection

Ask only if tone is genuinely important and absent. Otherwise infer:

- News comic: balanced, factual, editorial.
- Hot-blooded manga: exaggerated motion, heroic framing, emotional close-ups.
- Black-and-white Japanese football manga: traditional shonen sports manga, monochrome ink linework, screentone shadows, dense hatching, strong perspective football action panels, speed lines, sharp speech bubbles, crowd reaction cutaways, tactical pressure, breakthroughs, shots, and key duels. Use real-team visual identity cues and recognizable player silhouettes when they help readers understand the scene. Avoid color, photorealism, cute/chibi proportions, sponsor/logo clutter, and supernatural effects unless requested.
- Comedy four-panel: ironic captions, reaction shots, one punchline.
- Epic knockout recap: cinematic lighting, larger stakes, trophy or bracket consequences.
- Tragic exit: restrained color, empty space, missed chance, defeated body language.

## Cover Design

For serial social-media slide comics, do not add a cover to every episode by default. Start directly with manga page 1 unless the user asks for a cover.

- Use covers for chapter openings, major finals, special episodes, publication packages, and collected editions.
- Cover format: vertical first, usually 3:4 or 9:16. Mention that a 16:9 variant can be made for WeChat article headers if needed.
- The cover should not use multi-panel manga storytelling. Use one strong poster composition with a clear subject, bold title, and minimal supporting text.
- Make the cover readable as a thumbnail: large title, strong player silhouettes or duel pose, clear team color contrast, and one central symbolic object such as a ball, penalty spot, crossbar, stadium lights, trophy silhouette, or scoreboard fragment.
- Keep cover text short: title plus optional subtitle. Avoid long match summaries, dense facts, minute lists, and tiny captions.
- Use recognizable national-team kit colors, patterns, flags, player silhouettes, and symbolic design. Avoid sponsor logos, watermarks, and official tournament logo marks unless the user asks for licensed/official-asset treatment.
- The cover should promise the emotional hook of the comic, while the manga pages deliver the sequence of events.

## Manga Page Layout

For Japanese sports manga recaps, avoid standard four-panel, six-panel, or evenly spaced grid layouts unless the user explicitly asks for a grid. Use non-uniform manga page composition:

- Each generated image should be a complete manga page with multiple panels, not a single illustration of one scene. When using 2-3 images, each image is page 1/page 2/page 3 of the comic.
- Default social slide ratio is 3:4 vertical unless the user requests another format.
- Give the decisive action a large hero panel with a splash-page or double-page-spread feeling, even when the output is a single page.
- Intercut narrow reaction panels, foot/ball close-ups, goalkeeper-eye close-ups, scoreboard slivers, and crowd cutaways.
- Keep reading order clear with panel placement, motion direction, caption position, and visual rhythm.
- Let speed lines, speech bubbles, impact lettering, and sound effects participate in the composition, but keep text sparse and legible.
- Use large areas of white space or open pitch to express distance, pressure, isolation, and one-on-one duels.
- Vary panel shapes: tall vertical pressure panels, thin horizontal time-slice panels, diagonal action panels, small silent inserts, and one oversized main panel.
- Do not stack every panel as horizontal strips. Include vertical close-up panels or diagonal action panels when the page needs energy.
- Do not cram every beat onto one page. If a page would need more than 5-7 readable panels or too many captions, split the story.
- Split pages by dramatic function, not by equal event count. If a decisive event contains setup, waiting, hesitation, crowd reaction, bench reaction, performer selection, referee/VAR suspense, or shoot-out psychology, give that material its own page when needed.

## Black-and-White Brightness

Black-and-white manga means bright paper, ink linework, and controlled screentone; it does not mean dark backgrounds or black poster pages.

For manga pages, default to:

- Mostly white page background with clean panel gutters.
- Bright, readable panels with white paper showing through.
- Sparse or moderate screentone for shadows, crowds, depth, and mood.
- Heavy black only for focal silhouettes, speed lines, impact lettering, hair/uniform accents, night windows, or small dramatic inserts.
- Daylight, overcast daylight, bright airport terminals, clear training grounds, press rooms, or documentary-news lighting when the event is a departure, arrival, ceremony, training, or pre-match build-up.

Avoid unless the user explicitly asks for a dark poster style:

- Full black backgrounds.
- Dark page wash across most panels.
- Night-map compositions for interior story pages.
- Overusing "high contrast", "dramatic lighting", "glowing", "night", or "cinematic" in ways that push the model toward black-heavy art.
- Treating every manga page like a cover poster.

Differentiate cover and interior pages:

- Covers may use stronger contrast, but must still preserve readable bright areas and avoid solid black backgrounds unless requested.
- Interior story pages must prioritize clarity, white space, panel readability, and caption legibility over atmosphere.

## Text and Identity Rules

- Keep text minimal, but preserve identity anchors when needed: team names, key people, minute, score, and result.
- Prefer 5-8 information points per page at most.
- Keep each text block short; use labels, scoreboard fragments, jersey-name captions, title cards, or short speech bubbles.
- Use Chinese text by default.
- For generated images, ask for only the exact text items that should appear. If text accuracy matters, ask the model to leave clean caption spaces and add final text in post-production.
- Jersey numbers may be used when they are confirmed and useful for recognition. If numbers are not important or not verified, avoid prompting random jersey numbers.

## Fact Safety

- Never invent scorers, minutes, cards, penalty takers, or VAR calls.
- If sources conflict, mention the conflict and use the more authoritative source.
- For ongoing matches, state the timestamp of the information and avoid final language.
- Do not claim a team advanced, won a group, or was eliminated unless standings consequences are confirmed.
- For non-commercial documentary/fan manga prompts, prioritize recognizable team identity: kit colors, stripe patterns, flags, silhouettes, player names, hairstyles, body type, position, and iconic football gestures. Avoid sponsor logos, watermarks, and official tournament logo marks unless the user provides or requests licensed assets.
- Treat broadcast-observed or user-supplied micro-details that lack authoritative confirmation as staging material, not confirmed fact. Label them as user-provided, visual interpretation, or assumption in the boundary note.
- When using unconfirmed micro-details in scripts or prompts, phrase them ambiguously. For example, write "a midfielder approaches the penalty spot before the eventual taker steps in" rather than claiming a confirmed handoff of penalty-taking duty.

## Prompting Guidelines

When creating image prompts:

- Specify whether the prompt is for a social cover, chapter cover, or manga page.
- For cover prompts, specify platform-oriented vertical composition, title, subtitle, focal subject, thumbnail readability, and no multi-panel storytelling.
- For manga page prompts, specify page count, page-by-page beats, non-uniform panel layout, reading order, border style, and text constraints.
- Include only the exact text that should appear in the image.
- Use real team names, kit colors, recognizable patterns, flags, player roles, body language, hairstyles, and stadium atmosphere to identify teams. For real players, prompt for manga likeness through silhouette, posture, hair, and role rather than demanding photoreal portrait accuracy.
- Ask for clean, legible Chinese captions and no extra text. When final text must be accurate, ask for clean caption boxes and plan to overlay text later.
- For the default style, use "black-and-white Japanese football documentary manga", "non-uniform panel layout", "high contrast ink linework", "screentone shadows", and "speed lines".
- Add brightness constraints for black-and-white manga pages: "bright white paper background", "mostly white panels", "light-to-moderate screentone", "no full black background", "no dark page wash", and "keep all panels bright and readable".
- Add layout constraints when needed, such as: "Do not stack all panels as horizontal strips", "use one wide top panel", "use one diagonal action panel", and "use two stacked vertical close-up panels".

For image generation, prefer invoking the `imagegen` skill/tool after the script is stable.
