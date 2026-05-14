# GTI Blog — Global Translations Panama

This is the source code for the blog at [globaltranslationspanama.com](https://www.globaltranslationspanama.com), hosted via Cloudflare Pages from this GitHub repository.

---

## 📁 File Structure

```
/
├── index.html                  ← Blog home page (article listing)
└── articles/
    ├── TEMPLATE-article.html   ← Copy this to create a new article
    ├── what-is-certified-translation.html
    ├── consecutive-vs-simultaneous.html
    ├── translate-documents-for-panama.html
    ├── tips-for-working-with-interpreter.html
    ├── medical-translation-accuracy.html
    └── corporate-translation-panama.html
```

---

## ✍️ How to Add a New Article

### Step 1 — Copy the template
Duplicate `articles/TEMPLATE-article.html` and rename it using a short, descriptive slug:
```
articles/your-article-topic-here.html
```
Use lowercase letters and hyphens only (no spaces or special characters).

### Step 2 — Fill in the article content
Open your new file and replace all placeholder text:

| Placeholder | Replace with |
|---|---|
| `ARTICLE TITLE` | Your full article title |
| `ARTICLE META DESCRIPTION` | 1–2 sentence SEO description |
| `ARTICLE TITLE SHORT` | Short breadcrumb label |
| `CATEGORY` | e.g. Translation, Interpretation, Legal & Certified, Tips & Guides, Panama |
| `Month Year` | e.g. June 2025 |
| `X min read` | Estimated reading time |
| Article body sections | Your actual content |

### Step 3 — Add it to the blog index
Open `index.html` and add a new card inside the `<div id="blog-grid">` section.

Copy an existing `post-card` block and update:
- `href` → path to your new article
- `data-category` → one or more category keywords (used by the filter buttons)
- The emoji icon, category label, title, description, and date

**Example card:**
```html
<a href="articles/your-article-topic-here.html" class="post-card" data-category="translation tips">
  <div class="post-card-img">🌎</div>
  <div class="post-card-body">
    <span class="post-category">Translation</span>
    <h3>Your Article Title Here</h3>
    <p>A 1–2 sentence summary of the article for the card preview.</p>
    <div class="post-meta">
      <span>📅 June 2025</span>
      <span>⏱ 4 min read</span>
    </div>
    <span class="read-more">Read Article →</span>
  </div>
</a>
```

### Step 4 — Commit and push
```bash
git add .
git commit -m "Add new article: your article title"
git push
```
Cloudflare Pages will automatically deploy your changes within seconds.

---

## 🏷️ Available Category Tags

Use these in `data-category` attributes on cards and filter buttons:

| Tag | Label shown |
|---|---|
| `translation` | Translation |
| `interpretation` | Interpretation |
| `legal` | Legal & Certified |
| `tips` | Tips & Guides |
| `panama` | Panama |

Multiple tags are space-separated: `data-category="legal translation panama"`

---

## 🔗 Deployment

This blog is deployed via **Cloudflare Pages** connected to this GitHub repository.

- Every push to `main` triggers an automatic deployment.
- The blog is linked from the main site at [globaltranslationspanama.com](https://www.globaltranslationspanama.com).
- No build step required — this is plain HTML/CSS/JS.

---

## 🎨 Design Notes

The blog uses the same design tokens as the main site:
- **Navy:** `#0d2b4e`
- **Gold:** `#c9933a`
- **Fonts:** Playfair Display (headings) + Inter (body) via Google Fonts

---

© 2025 Global Translations Panama, Inc.
