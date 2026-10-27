### Uzay Bekaroglu

I build AI products from end to end: the prompts, model choice and cost limits, the app around them, and the tests that keep them working. I'm based in Alpharetta, GA, and I'm looking for AI / LLM engineering roles.

#### Selected work

| Project | What it is | Built with |
|---|---|---|
| **[assay](https://github.com/uzaybkr/assay)** | An eval runner for LLMs. It runs test suites on several models side by side, repeats each case to find flaky answers, can use an LLM judge, and flags regressions against an earlier run so CI fails. On two small models, it caught a prompt fix that quietly broke another case. | Python, Anthropic SDK, OpenAI-compatible APIs |
| **[Maia](https://github.com/uzaybkr/maia)** | A self-care app built on Claude. Claude scores photos with vision, each task has its own model, AI spending has hard limits, and photos are encrypted and deleted every day. Runs on web, iOS and Android, in English and Turkish. | Node, SQLite, Claude API, Capacitor |
| **[Sol](https://github.com/uzaybkr/sol-assistant)** | A website assistant that only answers from the site's own content. Replies stream in, it falls back to written answers when the AI is down, it has rate limits, and it hands off to a person. | Astro, Anthropic SDK |
| **[FirstMLDL](https://github.com/uzaybkr/FirstMLDL)** | Machine learning from scratch in NumPy, from linear regression to a neural network that scores 97.55% on MNIST. | Python, NumPy |
| **[Brochure Maker](https://github.com/uzaybkr/brochure-maker)** | A two-step LLM pipeline that picks a website's relevant pages, then writes a brochure from them. Works with four providers and has a streaming Gradio UI. | Python, OpenAI-compatible APIs |
| **[Need for Evil](https://github.com/uzaybkr/Need-for-Evil-)** | Two LLMs debate in character: Shakespeare on Groq and Machiavelli on a local Ollama model. | Python, Groq, Ollama |

#### How I build with LLMs

- Each task gets its own model and token cap, and every call is logged before it goes to the provider, so the budget holds.
- I don't call a prompt or model change finished until an eval suite shows it helped, with each case repeated so a lucky single run can't fool me.
- Structured output is checked. A refused or cut-off reply counts as a failure, never as a result.
- Every AI feature has a fallback that needs no API key, so local development and provider outages don't break the product.
- Code stays small with few dependencies, and every project ships with a test suite you can run and CI.

[aetherai.global](https://aetherai.global)
