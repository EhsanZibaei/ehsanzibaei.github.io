# Ehsan Zibaei's website

This site is built with Jekyll. Edit the source files in the repository; `_site/`
contains generated output.

## Local preview

Install Ruby and Bundler, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open the local address printed by Jekyll. To run the same build check as CI:

```sh
bundle exec jekyll build
```

## Updating the site

- **Career history:** edit `_data/career.yml`. Each entry controls a timeline
  heading and description. Optional `highlights` render as a bullet list.
- **Project cards:** edit the matching file in `_projects/`. Set `listing_title`,
  `listing_image`, `listing_period`, and `listing_order` in its front matter.
  `listing_period` connects the card to an entry in `_data/career.yml`.
- **Pages and layouts:** update `_pages/`, `_layouts/`, and `_includes/`.
- **Styles:** update `assets/css/style.css`.

The site build runs automatically on pushes and pull requests.
