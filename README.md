# TRACE platforma znanja — Srbija (demo)

Ovo je izdvojena, isključivo srpska Jekyll verzija platforme namenjena jednostavnom demonstracionom postavljanju na GitHub Pages.

## Šta je uklonjeno

- višejezičnost i `jekyll-polyglot`
- engleske, poljske i portugalske stranice i objave
- izbor jezika
- Decap CMS (`admin/`)
- Caddy, Docker Compose, Umami i Moodle/deployment servisi
- nestandardni Jekyll plugin iz `_plugins/`
- nepotrebni demo fajlovi i slike

## GitHub Pages

1. Napravite novi GitHub repozitorijum.
2. Kopirajte **sadržaj ovog direktorijuma u koren repozitorijuma**.
3. Push-ujte na granu `main`.
4. U GitHub-u otvorite **Settings → Pages**.
5. Pod **Build and deployment → Source** izaberite **GitHub Actions**.
6. Workflow `.github/workflows/pages.yml` će izgraditi i objaviti sajt.

Workflow koristi GitHub-ov Jekyll Pages build, tako da radi i kada je sajt objavljen kao project page (`username.github.io/naziv-repozitorijuma/`). Interni linkovi i asset-i koriste Jekyll `relative_url` filter.

## Lokalni pregled

Ako imate Ruby/Bundler:

```bash
bundle install
bundle exec jekyll serve
```

Zatim otvorite `http://127.0.0.1:4000/`.

## Struktura

- `index.md` — početna strana
- `_pages/` — srpske statičke stranice
- `_posts/` — srpske vesti/objave
- `_data/` — navigacija, hero, početne kartice i footer
- `_includes/` — zajedničke komponente
- `_layouts/` — Jekyll layout-i
- `assets/` — CSS, JavaScript, fontovi i slike
