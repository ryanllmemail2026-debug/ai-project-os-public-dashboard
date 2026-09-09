# Building Principles

These are the rules I try to use when building AI-assisted systems.

## 1. Start with the problem, not the model

I do not want to build AI features just because a model can generate something impressive. I want to identify a real bottleneck, define what success looks like, and then decide which parts should be deterministic, automated, AI-assisted, or human-controlled.

## 2. Evidence beats confidence

A model sounding certain is not proof. Important conclusions should be traceable to source evidence, validation results, logs, tests, or other durable artifacts.

## 3. Cheap intelligence first

Use rules, structured data, lexical retrieval, caching, and low-cost processing before escalating everything to an expensive model. Spend model intelligence where judgment or synthesis actually adds value.

## 4. Preserve source material; improve derived intelligence

The underlying evidence should survive model upgrades. Capture once, preserve broadly, and allow classifications, summaries, scores, and recommendations to improve over time.

## 5. Humans should own real decisions

Automation should remove repetitive work, not hide consequential choices. Money, credentials, permissions, destructive actions, privacy/publication exposure, and major product decisions deserve explicit human gates.

## 6. AI providers should be replaceable

A project should not collapse because one model, chat, or provider disappears. Durable state, clear interfaces, and evidence-based handoffs make it possible to swap tools as capabilities and economics change.

## 7. Build for failure and restart

Long-running jobs fail. Chats fill up. APIs time out. Runners disappear. Good systems should resume rather than require starting from zero.

## 8. Make the system explain itself

A fresh person or AI should be able to understand what the system is trying to do, what has been proven, what remains open, and what should happen next.

## 9. Separate prototype, proof, and production

An architecture can be interesting without being proven. A prototype can work without being production-ready. I try to label maturity honestly rather than presenting every experiment as finished.

## 10. Build things that could become businesses

My long-term interest is practical AI entrepreneurship: finding expensive, repetitive, information-heavy problems and building focused systems that make the work cheaper, faster, more consistent, or easier to understand.
