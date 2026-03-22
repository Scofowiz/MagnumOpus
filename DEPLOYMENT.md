# Ipso Facto - Deployment Guide for Cloudflare Pages

This repository contains three integrated Ipso Facto products:
- **Magnum Opus** — Flagship heavy-duty writing environment
- **Scriptorium** — Practical writing suite
- **NOTA** — Voice-driven capture application

## Directory Structure

```
/
├── index.html                    # Main hub/portal page
├── _redirects                    # Cloudflare Pages routing
├── magnum-opus/
│   └── index.html               # Magnum Opus product page
├── scriptorium/
│   └── index.html               # Scriptorium product page
└── nota/
    └── index.html               # NOTA product page
```

## Deployment to Cloudflare Pages

1. **Prerequisites**
   - Cloudflare account
   - Git repository connected to Cloudflare Pages

2. **Build Configuration**
   - Framework: None (static site)
   - Build command: (leave empty)
   - Build output directory: `/`

3. **No Build Step Required**
   This is a static site. All files are ready to serve as-is.

4. **Environment**
   - No environment variables required
   - All assets are self-contained

## Navigation Structure

All pages include consistent navigation:
- **Hub (index.html)**: Links to all three products
- **Product Pages**: Include back links to hub via "Ipso Facto" navigation link
- **Cross-Product Links**: Products can reference each other via relative paths

## URL Structure After Deployment

Assuming deployment to `ipso-facto.example.com`:

- `https://ipso-facto.example.com/` — Hub/Portal
- `https://ipso-facto.example.com/magnum-opus/` — Magnum Opus
- `https://ipso-facto.example.com/scriptorium/` — Scriptorium
- `https://ipso-facto.example.com/nota/` — NOTA

## Local Testing

To test locally:

```bash
# Using Python 3
python -m http.server 8000

# Or using Node.js with http-server
npx http-server

# Then visit: http://localhost:8000
```

## File Structure Notes

- All CSS is embedded inline within each HTML file (no external dependencies)
- All images are inline SVG or gradients (no external image files)
- Fonts are loaded from Google Fonts CDN
- Each product page is completely self-contained

## Next Steps

1. Commit and push this structure to your Git repository
2. Connect the repository to Cloudflare Pages
3. Set deployment source to main branch, root directory
4. Cloudflare will automatically deploy on every push

## Support

For questions about individual products, see their respective product pages in the repository.
