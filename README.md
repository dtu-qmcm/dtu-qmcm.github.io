# QMCM group website

Website of the Quantitative Modelling of Cell Metabolism (QMCM) group at BRIGHT.

**Live site:** https://dtu-qmcm.github.io/

Built with [Jekyll](https://jekyllrb.com) and the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme, hosted on GitHub Pages. Every commit to `main` rebuilds the site automatically (check the **Actions** tab: green = live, red = error).

## How to update the site

All edits can be done directly on github.com with the pencil icon. No installation needed.

### Add a person
1. Upload their photo to `assets/images/` (lowercase, no spaces, e.g. `anna.jpeg`).
2. Add an entry to `_data/people.yml` under the right section:
   ```yaml
       - name: "Anna Hansen"
         role: "PhD Student"
         photo: "anna.jpeg"
         email: "anna@dtu.dk"
   ```
   `photo` and `email` are optional. Without a photo, initials are shown.

### Add a publication
Add an entry to `_data/publications.yml`. Group members in `**bold**`:
```yaml
- title: "Paper title"
  authors: "Surname A, **Groves T**"
  journal: "Journal Name"
  year: 2026
  doi: "10.xxxx/xxxxx"
```

### Add news
Edit `anouncements.md`, and update the "Latest news" list in `index.md`.

## File overview

| File | What it controls |
|---|---|
| `_config.yml` | Site title, theme, skin |
| `index.md` | Home page (banner, boxes, news) |
| `research.md`, `contact.md` | Research and Contact pages |
| `_data/people.yml` | People page content |
| `_data/publications.yml` | Publications page content |
| `_data/navigation.yml` | Top menu |
| `assets/css/main.scss` | Colors, fonts, layout styles |
| `_includes/person.html` | Layout of one person card |
| `assets/images/` | All images |

## Tips
- Indentation matters in `.yml` files: use spaces, never Tab.
- Put quotes around titles that contain a `:`.
- If the site doesn't change after a green build, open it in a private window or use Ctrl+Shift+R to refresh the page. Your browser may be showing an old copy.
- If the build is red, open the failed run in **Actions** and read the line starting with `Error:`.
