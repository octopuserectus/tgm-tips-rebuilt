# TGM Guide

A Japanese strategy guide to Arika's *Tetris: The Grand Master* series (TGM, TAP, Ti), rebuilt as a
Jekyll site with English translations.

Live site: https://octopuserectus.github.io/tgm-tips-rebuilt/

- The original is no longer online; it can be found on the Web Archive: http://www13.plala.or.jp/TETRiS_TGM/kouza/
- Villadelfia's translation source can be found here: https://tgm.tips/
- English terminology follows https://tetris.wiki/

## Layout

| Path | Contents |
|---|---|
| `en/` | English translation, plus `glossary.html` |
| `en-vd/` | Villadelfia's English translation (incomplete) |
| `jp/` | Japanese original |
| `_data/chapters.yml` | Chapter order, slugs and titles for every language. The sidebar, index pages and previous/next links are generated from it |
| `_data/locales.yml` | One entry per language section: labels and UI strings |
| `_data/glossary.yml` | Japanese → English terminology, rendered by `en/glossary.html` |
| `_layouts/`, `_includes/` | `tip` (chapter page), `home` (section index), `landing` (language chooser) |
| `assets/images/NNpics/` | Diagrams for chapter NN |

Every language section has the same 19 files under `tips/`, named after the slugs in `chapters.yml`.
A chapter file holds only its front matter (`title`, `guide`, `order`, `layout: tip`) and content;
the heading and navigation come from the layout.

To add a language, create a directory with `index.html` and `tips/`, add an entry to `locales.yml`
and a title per chapter in `chapters.yml`.

## Running locally

```
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000/tgm-tips-rebuilt/.
