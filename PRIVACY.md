# Privacy checklist before publishing your portfolio

This template intentionally ships with fictional sample content only.

Before making your customized fork public, check that you did **not** commit:

- Private phone numbers, personal email addresses or messaging IDs you do not want public
- Home address, ID numbers, student IDs or other unique identifiers
- Private resume PDFs or portfolio ZIP archives
- Internal company screenshots, dashboards, documents or unpublished metrics
- API keys, tokens, `.env` files, analytics secrets or cloud credentials
- Private photos that you do not have permission to publish
- Sensitive metadata embedded in images or downloadable files
- Old sensitive content in Git history

Recommended final scan:

```bash
git grep -nEi 'phone|email|token|secret|api[_-]?key|password|private'
git log --all --stat
```

For a sensitive project, prefer creating a fresh repository from the sanitized template instead of converting an old private repository to public.
