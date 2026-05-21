# Jekyll Showcase Site - Documentation

This is the showcase website source code. The site is built with Jekyll and deployed to GitHub Pages.

## Structure

```
docs/
├── _config.yml           # Jekyll configuration
├── _layouts/             # Page templates (default, post, project)
├── _includes/            # Reusable components (navbar, footer)
├── _sass/                # SCSS stylesheets
├── _projects/            # Project collection items
├── _posts/               # Blog posts
├── assets/css/           # Compiled CSS
├── index.md              # Homepage
├── about.md              # About page
├── contact.md            # Contact page
├── projects.md           # Projects listing
└── blog.md               # Blog listing
```

## Setup & Local Development

### Prerequisites

- Ruby 2.7 or higher
- Bundler

### Installation

1. Navigate to the docs folder:
   ```bash
   cd docs
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Start the Jekyll server:
   ```bash
   bundle exec jekyll serve
   ```

4. Open your browser to `http://localhost:4000`

The site will auto-rebuild as you make changes.

## Building

To build the site for production:

```bash
bundle exec jekyll build
```

The compiled site will be in `_site/`.

## Customization

### Adding a New Project

1. Create a new file in `_projects/` with the naming convention `NN-project-name.md`:
   ```yaml
   ---
   title: Project Name
   subtitle: Brief description
   tech:
     - Technology 1
     - Technology 2
   link: https://github.com/...
   ---
   
   ## Project Details
   
   Your content here...
   ```

2. The project will automatically appear on the Projects page and homepage (featured projects).

### Adding a Blog Post

1. Create a new file in `_posts/` with the naming convention `YYYY-MM-DD-slug.md`:
   ```yaml
   ---
   layout: post
   title: "Post Title"
   date: 2024-05-20
   tags:
     - tag1
       - tag2
   excerpt: "Brief excerpt"
   ---
   
   Post content here...
   ```

2. The post will automatically appear on the Blog page and homepage (latest posts).

### Customizing Colors & Styling

Edit `_sass/main.scss`:
- Update color variables at the top (`$primary`, `$secondary`, etc.)
- Modify breakpoints for responsive design
- Adjust spacing and typography

### Updating Navigation & Footer

Edit `_includes/navbar.html` and `_includes/footer.html` to customize navigation links and social media URLs.

## Deployment to GitHub Pages

### Prerequisites

1. Push this repository to GitHub
2. Go to repository Settings → Pages
3. Set source to "Deploy from a branch"
4. Select `main` branch and `/docs` folder
5. Save

The site will automatically build and deploy to `https://yourusername.github.io/`

### Custom Domain (Optional)

1. In repository Settings → Pages, add your custom domain
2. Update `_config.yml` with your domain:
   ```yaml
   url: "https://yourdomain.com"
   baseurl: ""
   ```

## Verification Checklist

Before deploying:

- [ ] All navigation links work
- [ ] Homepage displays all sections (hero, projects, skills, blog, CTA)
- [ ] At least 3 projects are visible
- [ ] Latest blog posts appear on homepage
- [ ] About page has your bio
- [ ] Contact page has working form (requires Formspree or similar)
- [ ] Social links in footer point to correct profiles
- [ ] Mobile responsive (test on phone/tablet)
- [ ] No console errors or warnings
- [ ] Images (if any) load correctly

## Contact Form Setup

The contact page uses [Formspree](https://formspree.io/) for form handling:

1. Go to formspree.io and create an account
2. Create a new form
3. Copy your form ID
4. Update `contact.md` form action:
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```

## Common Issues

**Build fails with "Can't find jekyll"**
- Run `bundle install` first

**Styles not loading**
- Make sure `assets/css/main.css` has front matter (the `---` lines)
- Clear Jekyll cache: `bundle exec jekyll clean && bundle exec jekyll serve`

**Posts/Projects not showing**
- Verify frontmatter is valid YAML
- Check filename follows naming convention (`YYYY-MM-DD-slug.md` for posts)
- Verify collection is configured in `_config.yml`

**Site looks different locally vs. GitHub Pages**
- Check `_config.yml` settings match your deployment URL
- Ensure `baseurl` is correct (empty string for personal site, `/repo-name` for project site)

## License & Attribution

Feel free to use this template as a starting point for your own site!
