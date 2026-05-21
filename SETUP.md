# 🚀 Quick Start Guide

Your showcase website is ready! Here's how to get it running locally and deploy to GitHub Pages.

## ⚡ Local Testing (5 minutes)

### 1. Install Dependencies
```bash
cd Documents/welcome
bundle install
```

### 2. Run Development Server
```bash
bundle exec jekyll serve
```

You'll see output like:
```
Server address: http://127.0.0.1:4000/
Server running... press ctrl-c to stop.
```

### 3. View Your Site
Open your browser to **http://localhost:4000**

The site auto-rebuilds as you make changes. Perfect for testing!

## 🌐 Deploy to GitHub Pages

### 1. Push to GitHub
If you haven't already:
```bash
git init
git add .
git commit -m "Initial commit: Jekyll showcase site"
git branch -M main
git remote add origin https://github.com/yourusername/welcome.git
git push -u origin main
```

### 2. Enable GitHub Pages
1. Go to your repository on GitHub
2. Settings → Pages
3. Source: `Deploy from a branch`
4. Branch: `main` / Folder: `/docs`
5. Save

Your site will deploy to: **https://yourusername.github.io/welcome/**

### 3. Update Configuration (if using different URL)
If your repository is at a different URL or you have a custom domain, update `docs/_config.yml`:

```yaml
# For project site: https://yourusername.github.io/welcome/
url: "https://yourusername.github.io"
baseurl: "/welcome"

# OR for personal site: https://yourusername.github.io/
url: "https://yourusername.github.io"
baseurl: ""
```

Then commit and push.

## ✏️ Customization Checklist

- [ ] Update social links in `docs/_includes/footer.html`
- [ ] Replace placeholder links (GitHub, LinkedIn, Twitter)
- [ ] Set up contact form on [Formspree](https://formspree.io/) and update `docs/contact.md`
- [ ] Replace `about.md` with your actual bio
- [ ] Add your own projects to `docs/_projects/` (remove sample projects when ready)
- [ ] Publish your first blog post in `docs/_posts/`
- [ ] Test on mobile device
- [ ] Update `_config.yml` with your domain (if using custom domain)

## 📝 Add Your Own Content

### New Project
Create `docs/_projects/04-my-project.md`:
```yaml
---
title: My Amazing Project
subtitle: One-line description
tech:
  - Technology1
  - Technology2
link: https://github.com/...
---

## Project Description
Your content here...
```

### New Blog Post
Create `docs/_posts/2024-05-21-my-post.md`:
```yaml
---
layout: post
title: "My First Post"
date: 2024-05-21
tags:
  - tag1
  - tag2
excerpt: "Brief summary"
---

Your blog content here...
```

## 🎨 Styling Tweaks

Edit `docs/_sass/main.scss` to:
- Change colors (update `$primary`, `$secondary`, etc.)
- Adjust spacing and fonts
- Modify component styles

Then rebuild:
```bash
bundle exec jekyll build
```

## ❓ Troubleshooting

**Port 4000 already in use?**
```bash
bundle exec jekyll serve --port 4001
```

**Styles not updating?**
```bash
bundle exec jekyll clean
bundle exec jekyll serve
```

**Posts/projects not showing?**
- Check filename format: `YYYY-MM-DD-slug.md` for posts, `NN-name.md` for projects
- Verify frontmatter YAML is valid (check indentation)
- Files in `_posts/` and `_projects/` auto-generate permalinks

**Build errors?**
```bash
bundle update
bundle exec jekyll serve
```

## 📚 Next Steps

1. ✅ Test locally
2. ✅ Deploy to GitHub Pages
3. ✅ Customize with your info
4. ✅ Add your real projects and posts
5. ✅ Share your new site!

## 📖 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Docs](https://pages.github.com/)
- [Markdown Guide](https://www.markdownguide.org/)
- [YAML Syntax](https://learn.getgrav.org/16/advanced/yaml)

---

**Need help?** Check `docs/README.md` for detailed documentation.

Happy building! 🎉
