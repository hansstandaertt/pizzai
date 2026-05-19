
Create a modern, branded, HTML-based Reveal.js slide deck for an internal Securex “PIZZAI Session” presentation.

Context:
We are organizing a “PIZZAI” evening workshop from 17:00 to 20:30. The session includes explanation, pizza, a hands-on OpenWebUI demo, and brainstorming. The slides should guide the full session, but the focus is not on slide design. The focus is the story, flow, key messages, and facilitation structure.

Audience:
The audience is people from IT, but with mixed backgrounds:
- project managers
- business and functional analysts
- developers
- people coming from other industries
- people with limited technical AI knowledge

The explanation must be accessible, practical, and not too technical. Avoid hype and avoid assuming everyone understands AI, LLMs, APIs, or architecture.

Main outcome:
By the end of the workshop, people should leave with concrete team-specific use cases for how AI can help our IT teams.

The core story arc should be:

1. Understand why AI matters
2. Understand why this is not just “another chatbot”
3. See how our company AI platform works
4. Try it yourself in OpenWebUI
5. Brainstorm where this can help our IT teams

Important analogy:
When explaining that AI is not new, use a GPS as an accessible example:
A GPS fetches your location, evaluates possible routes, predicts travel time, reacts to traffic, and decides what instruction to give next. This shows that AI-like systems have already existed for a long time. What changed recently is not that AI suddenly appeared, but that large language models made AI much more accessible, conversational, and useful for knowledge work.

Technical setup to explain:
We use:
- a GPT model hosted on Azure
- Azure API Management as a governance and control layer
- OpenWebUI as the user-facing AI workbench
- MCP servers to connect AI to tools and company context
- on-prem Atlassian integrations:
  - Jira
  - Bitbucket
  - Confluence

Key positioning:
We are not just deploying ChatGPT.
We are building a governed internal AI platform that connects approved models, enterprise controls, and company knowledge.

Topics to cover:
- What AI is, using simple examples
- Why AI is not new
- What made AI boom in recent years
- What LLMs are, explained without heavy jargon
- Why LLMs can be useful but also wrong
- Why enterprise AI needs governance and context
- What MCP is and why it matters
- What OpenWebUI is
- How OpenWebUI can be used in daily IT work
- How Jira, Bitbucket, and Confluence integrations create practical value
- Responsible use of AI
- Hands-on demo flow
- Group brainstorming flow

Preferred narrative:
Use a “Platform to Practice” storyline:

Curiosity:
Start with familiar AI examples, especially GPS, to show that AI is already part of daily life.

Understanding:
Explain what changed with modern AI and LLMs: language became the interface, and AI became useful for knowledge work.

Trust:
Explain why the company setup matters: Azure model, APIM, OpenWebUI, MCP, and Atlassian integrations create a governed and reusable platform.

Practice:
Show practical use cases in OpenWebUI:
- summarize Confluence documentation
- refine Jira tickets
- explain technical topics in simple language
- help prepare stakeholder communication
- review or understand Bitbucket code context
- support onboarding
- generate meeting summaries or action lists
- brainstorm project risks or architecture options

Discovery:
End with hands-on exercises and brainstorming where participants identify real use cases for their own teams.

Requested output:
Create a complete storyline for the workshop, including:
- a clear session title and subtitle
- the main message of the evening
- a timed agenda from 17:00 to 20:30
- the recommended narrative flow
- suggested slide sections
- key talking points per section
- transitions between sections
- demo moments
- hands-on exercises
- brainstorming prompts
- closing message
- optional speaker notes for the most important sections

Tone:
Practical, warm, clear, enterprise-minded, and accessible.
It should feel like a hands-on pizza workshop about enterprise AI, not a corporate keynote.

I would also add this as the guiding message at the top of your own notes:

The goal is not to teach everyone the technical details of AI.
The goal is to make AI understandable, trustworthy, and concrete enough that every participant can identify where it could help their own IT work.

# Presentation format

Use:

* HTML
* Reveal.js
* fullscreen slides
* keyboard navigation
* fragment animations
* exportable to PDF

Slides should behave like real presentation slides:

* fixed 1280x720
* one slide per page
* clean transitions
* no scrolling

Use Reveal.js with:

```js
Reveal.initialize({
  hash: true,
  slideNumber: true,
  transition: 'slide',
  fragments: true,
  controlsLayout: 'bottom-right',
  progress: true,
  center: false,
  width: 1280,
  height: 720,
  margin: 0.02
});
```

---

# Branding / Style Guide

## Visual style

The presentation must visually resemble:

* securex.be
* the “PIZZAI Session” flyer
* Securex brand identity

Style keywords:

* soft
* rounded
* modern
* playful but professional
* enterprise workshop vibe
* less Azure-techy
* more human / collaborative

---

# Color palette

Use Securex-inspired colors:

```css
--purple: #4b2a67;
--purple-dark: #35184f;
--purple-soft: #efe7f5;

--teal: #008c95;
--teal-soft: #e7f6f7;

--red: #e83b55;
--red-soft: #fde8ec;

--cream: #f7fbfd;

--dark: #231f20;
--muted: #5f5a66;
```

---

# Typography

Main font:

```css
font-family: "morebi_roundedbold", Arial, sans-serif;
```

Load via:

```css
@font-face {
  font-family: "morebi_roundedbold";
  src: url("https://www.securex.be/securex/fonts/morebirounded-bold-webfont.woff") format("woff");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}
```

Typography style:

* rounded
* large titles
* generous spacing
* clean readable body text

---

# Slide layout style

Slides should:

* have rounded corners
* have a subtle top brand stripe
* have soft backgrounds
* use white cards
* have soft shadows
* use teal/purple accent colors

Top stripe:

```css
background: linear-gradient(
  90deg,
  var(--purple) 0%,
  var(--purple) 62%,
  var(--red) 62%,
  var(--red) 78%,
  var(--teal) 78%,
  var(--teal) 100%
);
```

---

# Securex logo

Use:

```txt
https://www.securex.be/Securex/images/logo-white.svg
```

Logo behavior:

* top-right
* inside purple pill
* subtle
* only ONCE per slide
* no duplicate logos
* no duplicate top banners

---

# Important Reveal.js layout fixes

To avoid visual artifacts:

* each section must be exactly 1280x720
* slides must use `width:100%; height:100%`
* use `overflow:hidden`
* disable Reveal centering
* avoid nested shadows leaking between slides

Critical fixes:

```css
.reveal section {
  height: 720px;
  width: 1280px;
  overflow: hidden;
  padding: 0 !important;
  margin: 0 !important;
}
```

And:

```css
.slide {
  width: 100%;
  height: 100%;
}
```

---

# Animation philosophy

Use subtle Reveal.js fragments:

* cards appear progressively
* timelines reveal step-by-step
* architecture layers build gradually

Avoid:

* flashy animations
* spinning effects
* gimmicks

Goal:

> calm progressive storytelling

---

# Tone of content

Use language that is:

* pragmatic
* enterprise-oriented
* understandable for non-experts
* architecture-aware
* practical
* collaborative

Avoid:

* AI hype
* buzzword overload
* “revolutionary AI”
* marketing nonsense