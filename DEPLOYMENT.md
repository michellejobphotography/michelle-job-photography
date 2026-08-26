# Deploying Michelle Job Photography

## Recommended: Cloudflare Pages + GitHub

1. Create a GitHub account/repository and upload all files in this folder.
2. In Cloudflare, open Workers & Pages → Create application → Pages → Import an existing Git repository.
3. Select the repository.
4. Production branch: `main`
5. Build command: `exit 0`
6. Build output directory: `/` (or the repository root, depending on the Cloudflare UI).
7. Deploy.
8. Cloudflare gives you a `*.pages.dev` preview URL.
9. In the Pages project choose Custom domains → Set up a domain → enter `michellejobphotography.com`.
10. If Cloudflare asks to add the domain as a zone, follow its nameserver instructions at your domain registrar. For an apex domain, Cloudflare requires the domain to be a Cloudflare zone.
11. Also add `www.michellejobphotography.com` as a custom domain if you want to support it, then choose one canonical version and redirect the other to it.
12. Keep the Squarespace site live until the new domain is confirmed working and redirects are tested.
13. In Google Search Console, verify the domain and submit `https://www.michellejobphotography.com/sitemap.xml`.
14. Only after testing the new site, cancel Squarespace.

## Important before launch

The prototype still references some images through the current Squarespace CDN. Before cancelling Squarespace, download the original owned photographs, optimize them to WebP/AVIF in multiple sizes, put them under `/images/`, and update the HTML to point to the local files.

## SEO migration

Before switching DNS, create 301 redirects from every important existing Squarespace URL to the closest new URL. Do not simply send every old URL to the homepage. Keep Google Search Console active and monitor indexing and 404s after launch.
