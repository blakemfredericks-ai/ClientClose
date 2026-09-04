# TARGET

Six lines. This is the whole skill we teach in Session 1.

A model will guess at every decision you leave open, and it guesses badly.
Six lines close off the six decisions that matter most. That is the entire
trick, and it is why the second site you build today will be better than the
first.

**T**hing &middot; **A**udience &middot; **R**equirements &middot;
**G**uardrails &middot; **E**xperience &middot; **T**est

Fill these in, then paste all six lines into Gemini. Replace the italic prompt
after each dash and leave the dashes alone.

---

- **T &mdash; Thing:A CRE prospecting platform for brokers that merges a cold-calling CRM for buyer/seller contacts with predictive analytics on market transactions. It flags who's likely nearing a deal by analyzing ownership tenure, comps, and transaction patterns—turning a static call list into a prioritized, data-ranked pipeline of warm opportunities.
- **A &mdash; Audience: Commerical Real Estate brokers
- **R &mdash; Requirements:The requirements for the target model center on several key areas. First, data requirements include sourcing property records, ownership history, transaction and sales comps, tax records, lease expirations, loan and mortgage data, and permit filings, at a granularity ranging from parcel-level to owner-level to market-level, with enough historical depth (roughly 5–10 years) to train the model effectively and a defined update frequency for keeping the data fresh. Second, the target itself must be clearly defined—specifically, the probability that a buyer or seller will transact within a given window, such as 6, 12, or 24 months—along with how past transactions are labeled to train the model and whether the scope covers buyers, sellers, or both. Third, the model relies on a set of features or signals, including ownership tenure length, time since the last transaction, loan maturity dates, comparable sales activity, vacancy or lease rollover indicators, owner type (individual, LLC, institutional, or trust), and broader market trends like cap rates, absorption, and price movement. Functionally, the model needs to output a usable score or ranking—whether as a percentile, a tier such as hot/warm/cold, or a simple ranked list—that integrates directly into the CRM and calling list, automatically sorting or flagging leads and re-scoring them on a regular cadence, while also allowing brokers to filter by asset type, geography, or deal size. On the performance side, the model should meet a minimum standard of accuracy or predictive lift over simple heuristics like "time since last sale," and ideally offer some explainability so brokers can understand why a given lead scored highly. From a technical standpoint, the system needs a defined retraining schedule, a decision on real-time versus batch scoring, integration with the CRM module, and compliance with data storage and licensing requirements for public records. Finally, the requirements should address the end users—whether individual brokers, teams, or administrators—how the model changes their day-to-day workflow, such as auto-prioritizing the call list or triggering alerts, and what business success looks like, typically measured by increased conversion rates and reduced time spent on low-probability leads.
- **G &mdash; Guardrails:The guardrails for the code should ensure the model and application behave safely, fairly, and reliably in production. On the data side, guardrails must enforce that only properly licensed or public-record data is ingested, with validation checks to catch missing, duplicate, or malformed records before they reach the model, and clear handling for stale or unavailable data so the system doesn't score leads on outdated information. On the fairness and compliance side, the model should be audited to ensure it isn't inadvertently using or proxying for protected characteristics (race, familial status, etc.) in violation of fair housing or anti-discrimination laws, even though this is commercial rather than residential real estate, since ownership entities can still trace back to individuals. From a model behavior standpoint, guardrails should include confidence thresholds so low-confidence scores are flagged rather than presented as high-certainty predictions, fallback logic for when key data inputs are missing, and monitoring for model drift so accuracy doesn't silently degrade over time without triggering a retraining review. On the application side, the code needs input validation and sanitization on every user-facing field to prevent injection attacks or malformed data from breaking the CRM, rate limiting and authentication checks to prevent unauthorized access to sensitive ownership or contact data, and role-based access control so brokers only see the leads and data relevant to their permissions. Error handling should be built in throughout, with graceful degradation (the app should never crash or lock a broker out entirely if the scoring engine fails, but instead fall back to showing the raw list) and clear logging so failures can be traced and debugged quickly. Finally, there should be guardrails around data retention and deletion (especially for contact information and call logs), audit trails for who accessed or changed data and when, and a testing requirement that any change to the scoring logic or CRM functionality passes automated tests before deployment, so the system stays stable and trustworthy as it scales. Never make up false percentages that are not based on true data.
- **E &mdash; Experience:The experience should feel clean, professional, and data-forward, similar to LoopNet or Zillow, where the interface gets out of the way and lets the property and prospect data do the talking. The site should follow a clear, logical flow: starting with a hero/search section where brokers can quickly search or filter their prospect list, followed by a dashboard or overview section showing key metrics and top-priority leads, then a detailed list or map view of buyers and sellers with their likelihood-to-transact scores, and finally individual contact/property detail pages with deeper data, transaction history, and call-log functionality. The color palette should be built around a white background as the dominant base, keeping the layout airy and uncluttered, with red used sparingly as the single accent color to highlight key actions, alerts, high-priority leads, or call-to-action buttons, so it draws the eye without overwhelming the page. Typography and spacing should stay minimal and functional, prioritizing legibility and quick scanning over decoration, much like how Zillow keeps listings clean and easy to browse or how LoopNet keeps commercial data dense but organized. Overall, the goal is a professional, trustworthy, broker-grade tool that feels modern and efficient rather than flashy, where the white space creates clarity and the red accent creates urgency and focus exactly where it's needed.
- **T &mdash; Test: Before showing it to someone whose opinion matters, I'd check that every core flow actually works end-to-end without errors—search, filtering, viewing a lead's detail page, and any call-log interactions—since a broken click kills credibility instantly. I'd double check the data displayed looks realistic and consistent (no placeholder text, lorem ipsum, or obviously fake numbers), that the design renders cleanly on both desktop and mobile, and that there are no glaring typos or misaligned elements. I'd also make sure the story is clear at a glance—that someone unfamiliar with the project can look at the homepage and immediately understand what the tool does and who it's for—and that the overall feel matches the polish level of LoopNet or Zillow rather than looking like a rough draft. Finally, I'd have someone else click through it cold, without my guidance, to see where they get confused, since that's the fastest way to catch what I've become blind to.
---

## Stuck on a line?

**T &mdash; Thing.** Keep it to one sentence. If it needs two, you are probably
building two things.

**A &mdash; Audience.** "Employers" is too vague to be useful. "A recruiter at a
company I actually want to work at, who will give this 30 seconds on their
phone" tells the model about length, layout, and what goes first.

**R &mdash; Requirements.** Not everything you *want*. The things that, if you
took them out, would make the whole thing pointless. Two or three, not eight.

**G &mdash; Guardrails.** This one feels strange to answer and it is the most
useful line in the file. What does every other version of this get wrong? What
would embarrass you? What are you tired of seeing?

**E &mdash; Experience.** The line everyone writes worst, because it is tempting
to write moods. *"Forest aesthetic with beach vibes"* gives a model nothing to
build. Structure does: **sections in order, one accent color, one reference.**
Write "hero, story, three highlights, contact. Deep green. Lots of whitespace.
Should feel like a clean personal site, not a resume" and you will get something
completely different.

**T &mdash; Test.** You need a finish line, or you will keep fiddling until the
room clears out. What is the one thing that has to be true?

---

## A worked example

Deliberately not a personal website. Copy the *shape*, not the words.

- **Thing:** A page that shows which Cal Poly dining spots have the shortest lines right now.
- **Audience:** Me and my three roommates, on our phones, walking out of class.
- **Requirements:** Show every dining location, let anyone report a wait time, sort shortest first.
- **Guardrails:** Never require an account. Never take more than two taps to report a wait.
- **Experience:** One screen, no scrolling. Big tappable cards in a single column. Green for short waits, red for long. Feels like a weather app, not a spreadsheet.
- **Test:** I can open it walking out of Building 52, know where to eat in under three seconds, and report a wait without thinking about it.

Nothing in there is clever. It is specific, it is short, and every line closes
off a decision the model would otherwise make badly on its own.

---

## Why this file exists

You built this site twice today. Once from a one-line prompt, once from the six
lines above. The second one was better, and it was better because of this file,
not because the AI got smarter in between.

The tool will change three times before you graduate. TARGET will not.
