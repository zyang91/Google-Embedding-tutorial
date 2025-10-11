# GitHub Workflows

## Deploy Slides to GitHub Pages

The `deploy-slides.yml` workflow automatically deploys the presentation slides to GitHub Pages.

### How it works

- **Trigger**: Automatically runs when changes are pushed to the `main` branch that affect files in the `slides/` directory
- **Manual trigger**: Can also be triggered manually via the Actions tab
- **Deployment**: Deploys all contents of the `slides/` directory to GitHub Pages
- **URL**: Once deployed, slides will be available at `https://zyang91.github.io/Google-Embedding-tutorial/`

### Setup Requirements

To enable this workflow, you need to:

1. Go to repository Settings → Pages
2. Under "Build and deployment", select "Source: GitHub Actions"
3. The workflow will automatically deploy on the next push to main

### Files Deployed

The workflow deploys the entire `slides/` directory, including:
- `slides.html` - Main presentation file
- `slides_files/` - Supporting libraries and assets
- `images/` - Image assets
- Other supporting files

### Permissions

The workflow requires the following permissions:
- `contents: read` - To read repository contents
- `pages: write` - To deploy to GitHub Pages
- `id-token: write` - For OIDC authentication
