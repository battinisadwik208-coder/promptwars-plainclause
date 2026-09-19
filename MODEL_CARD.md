# PlainClause model card

## Intended use
Educational legal-information assistance: make dense documents easier to read, surface questions, and help users prepare for a conversation with a qualified legal professional.

## Not intended for
- Legal advice, legal representation, or definitive legal conclusions.
- Predicting case outcomes or telling a user what they must legally do.
- Processing confidential, privileged, or highly sensitive records.
- Autonomous decisions, filings, negotiations, or communication with another party.

## Live model path
When a user supplies their own Gemini API key, PlainClause sends the document text and a constrained analysis prompt directly from the browser to the Gemini Developer API. The app requests JSON fields for summary, signals, obligations, questions, next steps, and disclaimer. The key is not stored by the app.

## Offline path
Without a key, the app uses transparent keyword checks for money, binding language, dates, and personal-data collection. This fallback is deliberately limited and labeled.

## Known limitations
- No jurisdiction, contract type, or legal-authority database is built in.
- Model output may omit important context or misunderstand a clause.
- Browser direct-to-API use requires the user to understand their key's exposure and quota settings.
- Users must verify results against the source document and seek professional advice for high-impact decisions.
