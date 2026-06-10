# campbellsean.github.io

Personal site and blog, built with [Jekyll](https://jekyllrb.com/) and published automatically by GitHub Pages on every push to `master`.

## Writing a new blog post

1. Create a file in `_posts/` named `YYYY-MM-DD-your-title.md`, e.g. `_posts/2026-06-14-churros-at-midnight.md`
2. Start it with this header, then write Markdown below:

   ```markdown
   ---
   layout: post
   title: "Churros at Midnight"
   ---

   Post content goes here.
   ```

3. Push to `master`. GitHub Pages rebuilds in about a minute. The post gets its own
   shareable URL: `/blog/2026/06/14/churros-at-midnight/`

### Images in posts

Put them in `assets/images/posts/` (a folder per post keeps things tidy) and reference them:

```markdown
![Churros](/assets/images/posts/2026-06-14-churros/churros.jpg)
```

Tip: resize photos to ~1600px wide before committing so pages load fast.

## Editing the site

- `index.html` — homepage (bio, photo, recent posts)
- `blog/index.html` — the post list
- `_layouts/` — shared page shell (`default.html`) and post template (`post.html`)
- `assets/css/main.css` — all styling; colors are CSS variables at the top
- `classic/` — the original 2022 site, preserved unchanged

## Running locally

Jekyll is installed in the user gem directory (system Ruby 2.6, matching the
Jekyll 3.9 line GitHub Pages uses):

```sh
~/.gem/ruby/2.6.0/bin/jekyll serve
```

Then open http://localhost:4000. It rebuilds automatically as you edit files.

If Jekyll isn't installed yet:

```sh
gem install --user-install ffi -v 1.15.5 public_suffix -v 4.0.7 --no-document
gem install --user-install jekyll -v 3.9.5 kramdown-parser-gfm --no-document
```

(The pinned `ffi` and `public_suffix` versions are needed because system Ruby is 2.6.)
