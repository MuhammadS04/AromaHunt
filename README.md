# AromaHunt

Phase 0 — Setup (1–2 days)

Repo, CI, TS base; RN (Expo) app shell; Node API skeleton; pick DB (Neon + pgvector or Typesense).

Phase 1 — Data & search (1–2 weeks)

Define schema + load seed data (e.g., small curated CSV or an open dataset).

Implement /search (name/brand/notes) and /fragrance/:id.

Implement similar/dupe endpoint via embedding similarity (MVP).

Caching & simple analytics (search count, top queries).

Phase 2 — App UX polish (3–7 days)

Search with typeahead; result filters (notes, family, brand).

Detail page with pyramid & “Similar/Dupes”.

Error states, empty states, basic accessibility.

Phase 3 — Beta add-ons (later)

Compare two fragrances side-by-side.

Save favorites (local, then user accounts).

Simple taste quiz → personalize suggestions.

Price/store integration spike.



ChatGPT (GPT-5 Thinking) for planning, spec, and code scaffolding; o1-style models for deep reasoning on algorithms.

Claude 3.5 Sonnet for long-context refactors and doc writing.

Gemini 1.5 Pro for huge JSON/CSV ingestion during data wrangling.

Open-source locally: Llama 3.1 70B (via Ollama/LM Studio) if you want private, offline assistance.

Code copilots & builders

Cursor (great choice) or Windsurf for repo-wide edits.

GitHub Copilot for inline completion; Copilot Chat for quick test scaffolds.

Retrieval & eval

LlamaIndex or LangChain only if you add RAG later (overkill for MVP search).

Evals: write lightweight smoke tests for search relevance (e.g., expected dupes for a few anchor scents).

Rough data/algorithm notes you can reuse

Index text: name, brand, family, notes_top, notes_heart, notes_base, accords.

Vector text: accords + all_notes joined; embed → store in pgvector.

Similarity score (simple):
0.6 * cosine(embeddings) + 0.2 * Jaccard(note_sets) + 0.2 * Jaccard(accord_sets)
Tune weights later using a small labeled set of “good dupes”.

References (so you know what’s out there)

FragranceFinder API (search + dupes endpoints) and its community post. 
RapidAPI
Reddit

Open Beauty Facts public API/datasets for cosmetics ingredients. 
world.openbeautyfacts.org
Kaggle

Kaggle fragrance datasets (Fragrantica/Parfumo) useful for prototyping (watch licenses). 
Kaggle
+1

Discussion indicating no official Fragrantica API → scraping is common but fraught. 
Fragrantica

Wikiparfum as a public reference engine for note/family discovery. 
Wikiparfum
