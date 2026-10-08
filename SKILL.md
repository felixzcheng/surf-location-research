---
name: surf-location-research
description: Research a surf destination for a location and optional date or date range, combining timestamped observations, date-specific forecasts, seasonal guides, videos, and satellite geography into a personalized spot shortlist. Use for surf-trip research and wave suitability, rather than generic beach travel.
---

# Surf location research

Accept a country, coast, town, or named surf break plus an optional date or inclusive date range. Support inputs such as `Mirissa today`, `Weligama 2026-10-05`, and `Sri Lanka 2026-11-10 to 2026-11-17`; location-only input remains supported. Complete the first-use profile setup below before research. Produce a source-linked report in the recipient's chosen language, or the language of their request if unspecified. Translate example status labels into that language. Research live on each run; never reuse example conditions as current facts. Use the embedded Report contract below for output structure.

## First use: set up the recipient's profile

At the very beginning of first use, before researching or recommending spots, ask the recipient to provide their own surfing information and preferences. This shared skill has no personal profile or preferred language, board, stance, wave direction or wave size built in. Never import the author's or another user's profile.

Ask one compact, grouped question in the user's language:

“Before I research, please set up your own surf profile: your level (including whether you catch waves independently), board type, stance (regular/goofy/unknown), goals, comfortable breaking-wave face size, preferred wave direction or shape, reef/entry limitations or other constraints, and report language. You can mark anything unknown or say no preference.”

If the initial request already supplies some fields, acknowledge them and ask only for the missing fields. Wait for the reply before personalized research. Do not silently replace unanswered fields with defaults. If the user explicitly declines setup, proceed with a general, non-personalized report and state that personal suitability is unverified.

Use the supplied profile for the current conversation. On subsequent runs in the same conversation, reuse it and apply explicit changes without repeating the full questionnaire. In a new conversation with no recipient-confirmed profile available, ask again. Do not write personal information into the shared skill or persist it elsewhere unless the user requests that.

Rank spots against the recipient's actual goals, board and preferences. Distinguish their preferred practice size from an ability ceiling, and manageable waves from productive practice conditions. A self-reported past session does not establish competence in every break, current or wave shape. Do not infer swimming ability or reef experience. For frontside practice, goofy stance generally favors lefts and regular stance rights, but explicit direction preferences and wave suitability take priority. If stance is unknown or direction has no preference, do not invent a directional preference.

## Date input and time-aware output

Resolve the requested date before researching conditions. Accept ISO dates, named dates, `today`, `tomorrow`, and inclusive ranges. Resolve relative dates using the user's current date/time context, then print the exact calendar dates used. Treat explicit dates as destination-local calendar days unless the user specifies a timezone; show the destination timezone and exact retrieval timestamp with UTC offset. Ask only when date ambiguity materially changes the result (for example `03/04` without context). A month alone is a seasonal window, not permission to invent exact days or a year.

- **Today / now:** prioritize the latest timestamped webcam, buoy, station or local report; report observation time and age alongside the retrieval time. Distinguish offshore measurements from the actual breaking wave at the spot. Include the remaining daylight forecast windows separately. Reserve “live” for a verified live feed; a same-day clip is a dated observation, not a live feed.
- **Future dates inside the provider's actual forecast horizon:** fetch the latest forecast valid for those dates and rank daylight surf windows. Label all future conditions as forecasts, not real-time observations. Use finer windows for the next 72 hours and broader trends with lower confidence beyond that.
- **Dates beyond the available forecast horizon:** report seasonal suitability and explicitly state that a date-specific forecast is not yet available. Give the date when checking again would enter the provider's verified horizon, when calculable; do not schedule monitoring unless requested.
- **Past dates:** retrieve archived observations, footage or historical model data matching the requested dates, identifying observed versus modeled/hindcast conditions. Today's conditions do not answer a historical request. If archives are unavailable, mark historical conditions unverified.
- **Ranges spanning these categories:** split the output into historical, available forecast and out-of-range portions. Do not extend one day's data across the trip or fill gaps with seasonal averages.

With no dates, retain the year-round seasonal overview plus a separate current snapshot; do not assume the user is departing today. For dated requests, lead with date-specific conditions and keep the general destination overview brief. Re-rank the shortlist using conditions for the requested dates rather than carrying over the seasonal ranking.

For a country, group by distinct surf coasts and shortlist representative matches; for a town, examine nearby accessible alternatives; for a named break, distinguish its sections and provide a gentler fallback. Do not claim exhaustive global coverage. Resolve ambiguous place names using context; ask one question only if different plausible locations would change the research.

## Research workflow

### 1. Geography and seasonal overview

Use Surf Atlas where covered, a forecast-provider spot map (Surfline is the successor to Magicseaweed/MSW), and independent local surf-school/operator guides. Elsewhere use regional surf guides and official meteorological/marine services. MSW is a legacy discovery term, not a separate current forecast source.

Identify surf regions, good months, shoulder/transition months, wave types, access, and a few relevant non-surf activities. Cross-check the top recommendations with two independent sources when available; syndicated copies do not count twice. A guide's update date does not make every statement current. Distinguish town, beach, main reef, inside wave, and similarly named breaks. Include source disagreements rather than smoothing them away.

### 2. Candidate selection

Build a manageable shortlist, usually 4–6 spots. Give each a qualitative disposition: priority candidate, conditional candidate, or excluded for this profile. Explain the tradeoff; do not fabricate numeric suitability scores or exact ride lengths.

Prioritize wave features that serve the confirmed profile and goals, including takeoff shape, usable push, shoulder shape and ride length. Direction alone must not outweigh overall suitability. Explain how each candidate supports each stated goal and whether it is merely manageable versus productive for practice. For a user practising longboard cross-stepping, assess time to trim, walk and recover position; do not apply this goal to other users by default. Do not infer suitability from a spot name such as Lazy or Baby. Record bottom type, entry/exit, crowd pressure, and relevant tide/swell dependence. For each conditional candidate, explain what would make it unsuitable.

Waist-high refers to the actual breaking face relative to a standing surfer. It is not equivalent to offshore significant wave height or a fixed provider-specific feet scale. Do not convert swell height directly to face height. Never recommend a session just because an aggregate forecast says GOOD.

### 3. Visual evidence

Search YouTube for `<location> surf guide`, then `<spot> raw surf`, `<spot> <user board type and target wave style>`, and suitable local-language equivalents. Select an overview and spot-specific footage for the leading candidates when available. Prefer normal-day continuous rides over highlight reels.

When browser/video access is available, actually inspect relevant footage. Record the title, creator, publication date, filming date if known, chapter or inspected timestamps, and what was observed. Separate independently inspected frames/segments from publisher chapter labels and text descriptions. A still frame cannot establish ride duration or peeling speed. A transcript alone is not visual verification. Don't infer right/left from screen direction without orienting the camera and surfer.

Assess takeoff steepness, shoulder shape, sustained push, opportunities for the user's requested maneuvers, whether the rider must pump aggressively, closeouts, crowding, board type and scale. Multiple ordinary waves are better evidence than one successful ride. Label old footage as a wave-character reference, never today's conditions. If playback fails, provide verified video links as unreviewed leads and reduce confidence instead of claiming to have watched.

### 4. Requested-date observations and forecasts

Check public Instagram/TikTok accounts belonging to local surf schools, coaches, photographers, or the break; use webcams and timestamped local reports when available. School location does not prove footage location. Separate posting date from filming date; pinned posts, highlights, reposts and marketing clips are not recent observations by default.

For current requests, aim for observations within 72 hours, with same-day evidence preferred. For historical requests, match the requested date and disclose any time mismatch; current freshness thresholds do not make historical evidence invalid. Label 4–7-day material as recent context only; older or undated material is historical/unknown. This freshness convention is a reporting default, not a guarantee that conditions persisted. Record exact dates and location confidence. If access is gated or no fresh footage exists, say so. Do not message accounts, create accounts or purchase subscriptions merely to complete research.

For the leading spots, fetch forecasts valid for the requested dates or matching archives for past dates, following the date routing above. Check issue time, valid date/time, timezone, modeled surf-face height versus offshore/nearshore swell height, swell direction and period, wind speed/direction and tide station. Search snippets and pages named latest can be stale. Reject past validity dates from today's snapshot; record unknown if timestamps cannot be verified. Distinguish forecast from observation even when the provider calls it live.

Use 0–72-hour forecasts for near-term candidate windows; longer horizons are trends with greater uncertainty. For each useful daylight window, give local date/time, provider-estimated surf face height if available, primary/secondary swell height, period and direction, wind speed/direction and local offshore/onshore relation, tide height/stage and station where available, and a profile-specific verdict with confidence. Preserve units and mark unavailable fields unknown. Include source links, issue/observation timestamps and valid times. If sources disagree materially, explain the disagreement and lower confidence instead of averaging unlike quantities. Give only daylight session windows. No fresh local observation means the session recommendation remains provisional. Do not fill missing data with seasonal averages. Note reused model feeds when apparent independent forecasts share the same upstream model.

For each forecast-covered day, explicitly compare morning versus afternoon and name the preferred daylight period, with a short reason tied to wind, tide, swell and training goals. Use “both comparable”, “neither worthwhile” or “uncertain” when warranted; a relative winner does not guarantee a worthwhile session. Do not assume mornings are always cleaner or rising tide always better. Label proposed clock windows as inferred when only half-day data is available; outside the forecast horizon, mark this comparison unavailable.

Include a recommended takeoff area and distance-from-shore field for leading spots/windows. Prefer the working sandbar, reef section or observed breaking line that offers sustained open shoulders; farther offshore is not inherently better. Give approximate meters only when supported by a credible local report or a measurable, identifiable takeoff location, stating the source, reference shoreline, tide/date and uncertainty. Map measurements are approximate geometry, not proof of today's lineup or a recommended paddling distance. Without evidence, write “距岸米数未核实，按当天破浪线定位” and describe what to observe instead. Distinguish takeoff distance from usable ride length; do not invent either from still images or forecast wave height. Note shorebreak or closeouts when they undermine the training goal.

### 5. Satellite geography

Inspect Google Maps satellite imagery (or a clearly identified available alternative) for top candidates. Link the actual view/place, describe observable headlands, bay exposure, reef/rock indicators, harbor walls and plausible access. A business marker is not a takeoff coordinate. Mark approximate positions and unresolved aliases explicitly.

Do not rank consistency as mountain > breakwater > open coast. Separate (a) frequency of usable swell, (b) repeatability of the breaking location, and (c) suitability for this user. Bottom contours, swell direction/period, wind, tide and mobile sandbars interact. Headlands may shelter or focus swell; fixed reef can produce repeatable but steep waves. Satellite imagery does not establish water depth, current strength, safe entry, actual filming/imagery date or current wave size. Copyright year is not capture date. Present map-based deductions as inferences, cross-checked against local guides and video.

## Completion and quality bar

Deliver the best evidence-backed shortlist even when one platform is unavailable. Surface missing current evidence prominently; a partial evidence chain must not look like full verification. Do one direct access attempt and one reasonable alternative for a blocked source before moving on. Keep citations adjacent to claims and mark source-derived facts, direct observations and judgments distinctly.

Before delivering, verify that each top recommendation has a reason tied to the user's profile, a condition that could invalidate it, a source link, and an evidence status. Include a conservative fallback and excluded spots with reasons. Do not invent safety assurances, coordinates, video timestamps, ride lengths or current forecasts.

Return the report inline unless the user requests a saved artifact. The skill performs on-demand research; it does not continuously monitor or guarantee private Story access. No additional user input is required merely because current data is missing.


# Report contract

# Location and date report contract

Scale the length to the place. Complete the first-use profile setup in SKILL.md before producing a personalized report. Render all status labels and quoted examples in the recipient’s report language. Use the following content, with natural headings only where they help. Omit empty filler, never omit material unknowns.

1. **Verdict first:** best region/season and first spot to investigate for this user's profile. Say whether this is trip planning or a verified current session opportunity. State the resolved requested date or inclusive range, retrieval timestamp with UTC offset, destination timezone, recipient-confirmed profile, unknown fields and any assumptions. For dated requests, lead with the requested-date verdict and time-window table before the destination overview.
2. **Overview:** region distribution, core season and transition months, representative wave types, and 2–3 non-surf activities. Link a provider's spot map.
3. **Shortlist table:** spot and exact section | season | direction/bottom | fit for the recipient’s board, goals and preferences | drawback or invalidating condition | priority/conditional/excluded | evidence confidence. Distinguish the recipient’s preferred practice range from an ability ceiling; leave it unknown when not supplied. Distinguish training suitability from ability to handle a wave.
4. **Top candidate evidence cards:** guide evidence; video link with viewed timestamp or publisher chapter label; filming/publication dates; satellite link and observed geography; map inference; unresolved issues. Supply backup links when a provider is blocked.
5. **Requested-date conditions:** first provide a window table: local date/time | spot/section | observed or forecast surf-face height | swell height/period/direction | wind | tide/station | morning/afternoon preference and reason | takeoff area / evidence-backed approximate distance from shore (or unknown) | suitability and confidence | source. Split into a daily comparison table and detailed windows when that improves readability. A preferred half-day is a relative ranking, not a guarantee; allow both/neither/uncertain, and mark unavailable outside forecast coverage. Explain any inferred clock windows. For distance, include the shoreline reference, tide/date and uncertainty when measured; otherwise state “距岸米数未核实，按当天破浪线定位”. Mark missing values unknown. Then give the evidence ledger: source/account | observation vs forecast | posted/issued date | filmed/valid date and local time | exact spot confidence | finding | freshness/access status. For today, show observation age; when no fresh observation exists, explicitly conclude “近期实际浪况未核实”. Label future rows “预报”, past rows “历史观测” or “历史模型”, and dates outside the forecast horizon “仅季节参考，具体日期预报未开放”. Split mixed ranges and disclose uncovered dates. Never label future forecasts real-time conditions. List a few useful verified accounts, not invented usernames.
6. **Practical decision:** a conservative fallback suited to the supplied profile; direction options matching stated preferences; what to exclude; what must be checked on arrival. Avoid generic safety essays. If local input would resolve a specific gap, include one ready-to-copy question without sending it: “For [spot/section], do you have a continuous clip filmed today showing the takeoff and several sets? I ride [board], my level is [level], and my goals are [goals]. I prefer [wave characteristics and size]. What are the tide, bottom and entry conditions?” Fill only recipient-supplied fields and omit unknown ones.
7. **Evidence limits:** distinguish footage viewed from links merely found; identify missing forecasts, unavailable Stories, unknown image capture dates and material source conflicts. Link all material claims locally, not just in a bibliography.

## Behavioral checks during skill revision

- `Sri Lanka` on first use: ask for the recipient’s profile before research. After setup, show both coastal seasons and do not invent travel dates or a default preferred spot.
- `Bali` only: research Bali from live sources; do not inherit Sri Lanka's monsoon months, forecast thresholds or spot ranking.
- A named bay containing reef and sand peaks: don't classify every section using a single beginner-friendly label.
- A latest forecast dated three weeks ago: reject it as a current forecast, even if it says today.
- Instagram shows only old pinned reels: list the account as a lead, not a recent observation.
- User asks for powerful lefts: apply that preference with their supplied level and board, without imposing longboard-training goals.
- Only a mountain-backed satellite image is available: mark suitability unknown; do not infer a mellow or safe wave.

- `Mirissa today`: resolve the calendar date, show destination timezone and retrieval timestamp, separate observed conditions from remaining daylight forecasts; report missing live evidence honestly.
- `Weligama tomorrow`: provide only forecasts for the resolved date, not claims of observed future waves.
- `Sri Lanka 2027-06-01 to 2027-06-07` when outside the provider horizon: give seasonal guidance and no invented hourly conditions.
- A range spanning yesterday through next month: separate historical evidence, forecast coverage and seasonal-only dates.
- A past date with no accessible archive: mark unavailable rather than substituting current data.

- A regular-foot user requests frontside practice: assess suitable rights; do not inherit another user's left preference.
- A user requests longboard cross-stepping: evaluate sustained push and open shoulders. A shortboard user with different goals receives a different ranking.
- Unknown stance, board or wave-size preference: retain unknowns rather than filling in a personal default.
- First-use user explicitly declines setup: provide only general suitability, with personalization limits stated.
- Returning user in the same conversation: reuse their supplied profile and apply corrections without repeating the full questionnaire.
- Self-reported large-wave experience: retain as context, not a verified skill rating or blanket clearance for large/hollow surf.

- Morning has weaker wind but afternoon has better swell/tide: compare the tradeoff; do not automatically select morning or promise an exact best hour from half-day data.
- No measured takeoff position: describe the working breaking line and mark distance unknown, rather than suggesting a generic 50–100 m paddle.
