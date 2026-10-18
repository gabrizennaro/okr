# Team OKR

Static single-page app (`index.html`) on GitHub Pages, backed by Supabase (Postgres + Auth + RLS).

- **Access**: email/password sign-up; the first user becomes admin, everyone else waits for admin approval (enforced by RLS, not just UI).
- **Model**: cycles → objectives (optionally aligned to a parent objective) → key results → check-ins (value, confidence, comment).
- **Permissions**: approved members read everything; owner/creator/admin edit objectives and KRs; admins manage cycles and members.
- Schema lives in the Supabase project `okr` (`khqlnironeighgxkdlpo`, migration `okr_schema`).

Deploy: Settings → Pages → Source: **GitHub Actions**, then merge to `main`.
In Supabase → Authentication → URL Configuration, set Site URL to the Pages URL.
