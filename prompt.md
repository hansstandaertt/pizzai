# Securex AI Platform Presentation — Reusable Prompt / Design Brief

Use this as the reusable context/prompt to recreate or evolve the presentation later.

---

# Goal of the presentation

Create a modern, branded, HTML-based Reveal.js slide deck for an internal Securex “PIZZAI Session” presentation.

The presentation explains:

* what AI is
* why AI exploded recently
* what LLMs are
* what MCP servers are
* how the Securex AI platform is architected
* how OpenWebUI and Codex are used
* real use cases
* responsible AI usage

The tone should be:

* practical
* hands-on
* enterprise-minded
* architecture-aware
* not hype-driven
* approachable and collaborative

The session is meant to feel like:

> “hands-on pizza workshop about enterprise AI”

NOT:

> “corporate AI keynote”

---

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

---

# Core narrative of the presentation

## 1. AI is not new

Explain:

* AI history
* recent explosion
* transformers
* GPUs
* usability

Key message:

> ChatGPT was the usability breakthrough.

---

## 2. LLM explanation

Explain:

* probabilistic next-token prediction
* “autocomplete on steroids”
* limitations
* hallucinations

Key message:

> AI sounds intelligent but still requires grounding and validation.

---

## 3. MCP explanation

Explain:

* MCP = Model Context Protocol
* AI connecting to tools
* enterprise context

Analogy:

> “An LLM without MCP is like a smart employee without an access badge.”

---

## 4. Securex AI architecture

Important strategic slide.

Show:

* OpenWebUI for general users
* Codex CLI for developers
* Azure APIM as governance layer
* Azure AI Foundry / GPT model
* MCP integrations
* Jira / Confluence / Bitbucket

Architecture message:

> We are not deploying a chatbot. We are building a governed AI platform.

---

## 5. OpenWebUI usage

Explain:

* AI workbench
* upload documents
* summarize content
* reusable prompts
* assistants
* knowledge retrieval

Goal:

> make AI concrete for colleagues

---

## 6. Codex section

Explain:

* developer productivity
* code understanding
* repository reasoning
* tests/refactoring
* integration with MCP context

Message:

> one AI platform, different entry points

---

## 7. Use cases

Examples:

* documentation summaries
* Jira refinement
* meeting summaries
* onboarding
* stakeholder communication
* architecture assistance

---

## 8. Responsible AI

Important final maturity section.

Explain:

* AI can be wrong
* validate output
* context quality matters
* AI assists, not decides
* governance matters

---

# Important architectural positioning

The presentation should subtly communicate:

* maturity
* governance
* reusable AI capability
* platform thinking
* enterprise architecture mindset

Without sounding:

* bureaucratic
* overengineered
* theoretical

---

# Desired audience feeling

After the presentation people should feel:

* AI is approachable
* Securex is building something mature
* this is practical
* this can help me tomorrow
* architecture/governance actually matters
* this is more than “just ChatGPT”
