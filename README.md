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
