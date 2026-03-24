# Deployment Guide

This guide will help you deploy the Reasoning From Scratch learning website to GitHub Pages.

## Prerequisites

- GitHub repository with the website code in the `docs/` folder
- GitHub account with repository access

## Deployment Steps

### 1. Enable GitHub Pages

1. Navigate to your repository on GitHub
2. Click on **Settings**
3. In the left sidebar, click on **Pages**
4. Under **Source**, select:
   - **Branch**: `main` (or your current branch name)
   - **Folder**: `/docs`
5. Click **Save**

### 2. Wait for Deployment

GitHub will automatically build and deploy your site. This usually takes 1-2 minutes.

You can check the deployment status:
- Go to the **Actions** tab in your repository
- Look for the "pages build and deployment" workflow

### 3. Access Your Site

Once deployed, your site will be available at:
```
https://<username>.github.io/<repository-name>/
```

For this repository:
```
https://kodecraze.github.io/reasoning-from-scratch/
```

## Customization

### Update Site URL

If your repository name or GitHub username is different, update the `_config.yml` file:

```yaml
baseurl: "/<your-repository-name>"
url: "https://<your-username>.github.io"
repository: "<your-username>/<your-repository-name>"
```

### Custom Domain (Optional)

To use a custom domain:

1. Add a `CNAME` file to the `docs/` directory with your domain name
2. Configure DNS settings with your domain provider
3. In GitHub Pages settings, enter your custom domain

## Local Testing

Before deploying, test your website locally:

```bash
# Navigate to docs directory
cd docs

# Start a local server
python -m http.server 8000

# Open browser to http://localhost:8000
```

## Troubleshooting

### Site Not Loading

- **Check GitHub Actions**: Ensure the deployment workflow completed successfully
- **Verify Branch**: Make sure you selected the correct branch in GitHub Pages settings
- **Clear Cache**: Try clearing your browser cache or use incognito mode
- **Check URL**: Ensure you're using the correct URL format

### Styling Issues

- **Relative Paths**: Make sure all CSS/JS links use relative paths
- **.nojekyll File**: Ensure the `.nojekyll` file exists in the docs/ folder
- **Browser Cache**: Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)

### 404 Errors

- **Case Sensitivity**: GitHub Pages is case-sensitive; check file names
- **File Paths**: Verify all internal links use correct relative paths
- **Index File**: Ensure `index.html` exists in the docs/ directory

## Updating the Site

After making changes:

1. Commit your changes
   ```bash
   git add docs/
   git commit -m "Update website content"
   ```

2. Push to GitHub
   ```bash
   git push origin main
   ```

3. GitHub Pages will automatically rebuild and deploy (1-2 minutes)

## Advanced Configuration

### Custom 404 Page

Create `docs/404.html` for a custom not-found page.

### SEO Optimization

- Add meta tags to each page
- Include `sitemap.xml`
- Configure Open Graph tags for social sharing
- Use the `jekyll-seo-tag` plugin (already configured)

### Analytics (Optional)

Add Google Analytics or similar tracking:

1. Get your tracking ID
2. Add the tracking script to each HTML file (before `</head>`)

## Maintenance

- **Update Content**: Regularly update chapter content and resources
- **Monitor Issues**: Check GitHub Issues for reported bugs
- **Test Links**: Periodically verify all external links work
- **Update Dependencies**: Keep CDN links (Font Awesome, Prism.js) current

## Support

For issues with:
- **Website Content**: Open an issue in the repository
- **GitHub Pages**: Check [GitHub Pages documentation](https://docs.github.com/en/pages)
- **Jekyll**: See [Jekyll documentation](https://jekyllrb.com/docs/)

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Documentation](https://jekyllrb.com/)
- [Custom Domain Setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
