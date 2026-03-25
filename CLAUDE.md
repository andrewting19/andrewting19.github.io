# CLAUDE.md

Personal website and blog for Andrew Ting. Static HTML site hosted on GitHub Pages.

## Blog Posts

### Structure
- Blog index: `blog/index.html` — lists all posts as cards
- Post template: `blog/posts/template.html` — copy this for new posts
- Each post lives in its own directory: `blog/posts/<slug>/index.html`

### Creating a new post
1. Create directory: `blog/posts/<slug>/`
2. Copy `blog/posts/template.html` to `blog/posts/<slug>/index.html`
3. Update the content, title, meta tags, date, read time, and tags
4. **Add a card entry to `blog/index.html`** in the `.blog-list` div (newest posts first). Don't forget this step!
5. Asset paths from posts use `../../../assets/` (three levels up)

### Conventions
- All styling is inline (no shared CSS file) — each page has its own `<style>` block
- Design: dark terminal aesthetic, JetBrains Mono + Instrument Sans, cyan accent (#22d3ee)
- Nav bar links use relative paths back to root (`../../../` from post, `../` from blog index)
- Footnotes: use `<a href="#fnN" id="fnrefN" class="footnote-ref">[N]</a>` in text, `<div class="footnotes"><ol><li id="fnN">...</li></ol></div>` before `</article>` — see `fundamental-principles-llms` post for footnote CSS
- Some posts have an unhinged/normal mode toggle with `#hash` URL routing — see `tools-i-actually-use` for the pattern
- Footer has ASCII art logo, consistent across all pages
- Date format: YYYY-MM-DD
