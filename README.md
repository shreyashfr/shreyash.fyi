# fyi by shreyash

Personal website and mentorship hub for Shreyash Chavan.

## Website Structure

- **[/](https://shreyash.fyi)** - Homepage with intro and Cal.com booking integration
- **[/suchi](https://shreyash.fyi/suchi)** - Mentorship plan page

## Domain

This site is hosted on GitHub Pages and accessible at [shreyash.fyi](https://shreyash.fyi)

## Tech Stack

- Pure HTML/CSS/JavaScript
- GitHub Pages for hosting
- Cal.com for booking integration
- Custom domain via Namecheap DNS

## Setup Domain (Namecheap)

To connect your Namecheap domain to GitHub Pages:

1. Go to Namecheap Dashboard → Domain List → Manage
2. Navigate to "Advanced DNS"
3. Add these DNS records:

```
Type: A Record
Host: @
Value: 185.199.108.153
TTL: Automatic

Type: A Record
Host: @
Value: 185.199.109.153
TTL: Automatic

Type: A Record
Host: @
Value: 185.199.110.153
TTL: Automatic

Type: A Record
Host: @
Value: 185.199.111.153
TTL: Automatic

Type: CNAME Record
Host: www
Value: shreyashfr.github.io
TTL: Automatic
```

4. Wait 30 minutes to a few hours for DNS propagation
5. GitHub Pages will automatically detect your custom domain from the CNAME file

## Local Development

Simply open `index.html` or `suchi.html` in your browser.

## Deploy

Push to main branch - GitHub Pages will automatically deploy.

```bash
git add .
git commit -m "Update website"
git push origin main
```
