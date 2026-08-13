# Kindly — Customer Review Assistant

Triage customer reviews and prepare editable multilingual responses for approval. Project 08 in the Jamil Darwish Automation Lab.

## Modes

- **Demo:** transparent local rules classify reviews and draft English, German, or Arabic replies.
- **AI:** your model drafts a more contextual reply through the private local API proxy.

## Quick start

Requires Node.js 22+.

```bash
git clone https://github.com/Jamilof1/customer-review-assistant.git
cd customer-review-assistant
npm install
npm run dev
```

For AI mode, copy `.env.example` to `.env`, add `AI_API_KEY`, and restart. PowerShell: `Copy-Item .env.example .env`.

## Provider configuration

Defaults: OpenAI Responses API and `AI_MODEL=gpt-5`. Compatible chat APIs can use their own base URL/model with `AI_API_STYLE=chat`. Credentials stay in the server process; `.env` is excluded from Git.

## Features

- Rating, sentiment, topic, and priority signals.
- Editable English, German, and Arabic drafts.
- Optional AI response based on the active review and language.
- Human approval queue, copy, and case-note export.

## Commands

`npm run dev` starts client + API, `npm test` runs tests, `npm run build` creates `dist/`, and `npm start` serves it.

## Responsible use

Demo inputs remain local. AI mode sends the active review to the configured provider only after a click. Names, translations, facts, compensation, and promises require human review. Nothing is published automatically.

MIT — built by [Jamil Darwish](https://jamildarwish.com/).
