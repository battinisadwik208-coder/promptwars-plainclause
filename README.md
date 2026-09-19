# PlainClause

PlainClause is a privacy-first legal-information assistant for PromptWars Virtual's **AI for Legal Assistance & Access** challenge. It turns pasted agreements, policies, offer letters, rental clauses, and notices into a cautious plain-language brief.

## What it does

- Extracts obligations, deadlines, data-sharing terms, restrictions, and money-related clauses.
- Produces questions a user can take to a qualified legal professional.
- Supports live Gemini analysis with a user-provided API key that remains in the current browser tab.
- Includes a transparent offline demo mode when no key is provided.
- Never presents itself as a lawyer or a substitute for professional advice.

## Run locally

Open `index.html` in a modern browser. No server or dependency installation is required.

For live Gemini analysis, expand **Use live Gemini analysis**, enter a Gemini API key for the current session, and click **Analyze document**. The browser calls the Gemini Developer API directly; PlainClause has no backend and does not store the key.

## Privacy and safety

Do not paste passwords, identity numbers, confidential client data, or documents you are not allowed to process. PlainClause is an educational prototype. Results can be incomplete or wrong and must be checked against the original document and a qualified professional.

## PromptWars submission checklist

- Live prototype URL
- Public GitHub repository under 10 MB
- Project description
- Explicit GenAI architecture mapping
- Walkthrough under four minutes showing live data entry and Gemini output

## GenAI architecture

`index.html` → `app.js` → Gemini Developer API `generateContent` endpoint (when the user supplies a key). If no key is supplied or the request fails, the app uses a local keyword-based fallback and labels it clearly. No secret is committed.
