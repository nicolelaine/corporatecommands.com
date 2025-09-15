# corporatecommands.com

This is the source code for [corporatecommands.com](https://www.corporatecommands.com), a website built with [Hugo](https://gohugo.io/) and the [Blowfish theme](https://github.com/nunocoracao/blowfish), using Hugo Modules and deployed via GitHub Actions to GitHub Pages.

## Local Development

Make sure you have [Hugo Extended](https://gohugo.io/getting-started/installing/) installed.

This site is built with Hugo version:

```bash
hugo v0.148.2+extended+withdeploy darwin/amd64 BuildDate=2025-07-27T12:43:24Z VendorInfo=brew
```

To preview the site locally:

### Clone the repo
```bash
git clone https://github.com/nicolelaine/corporatecommands.com.git
cd corporatecommands.com
```

### Fetch Hugo module dependencies
```bash
hugo mod tidy
```

### Start the local server
```bash
./serve.sh
```

### Or manually run 
```bash
hugo server --baseURL http://localhost:1313/
```

## Deployment 

This site is automatically deployed to GitHub Pages using a GitHub Actions workflow.

Deployment steps:

Push to the main branch.

GitHub Actions runs hugo and deploys the output in the /public/ folder to the gh-pages branch.

The live site is available at:
https://www.corporatecommands.com 

# Repository Structure

| Folder/File          | Description                                               |
| -------------------- | --------------------------------------------------------- |
| `config/_default/`   | Hugo site configuration files (`config.toml`, etc.)       |
| `content/`           | Website's markdown content                                |
| `layouts/`           | Custom templates and overrides                            |
| `static/`            | Static assets (files, etc)                                |
| `assets/`            | Processed assets                                          |
| `archetypes/`        | Contains content templates for new pages or posts         |
| `serve.sh`           | Helper script to run the site locally                     |
| `CNAME`              | Stores the custom domain                                  |
| `.gitignore`         | Everything not pushed to Git/Github                       |
| `go.mod`, `go.sum`   | Hugo Modules configuration                                |
| `.github/workflows/` | GitHub Actions deployment setup                           |

# Housekeeping

The public/ and resources folders are not committed — they are regenerated automatically.
Unused folders like data/, i18n, and themes/ were removed for clarity.

# Credits

Theme: Blowfish by @nunocoracao 
Built with Hugo
