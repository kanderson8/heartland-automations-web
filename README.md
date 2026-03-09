# Heartland Automations — Marketing Website

One-page marketing site for Heartland Automations, an AI workflow automation consultancy serving Chicago-area SMBs.

## Deploy to Cloudflare Pages

1. **Push to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   gh repo create heartland-automations-web --public --source=. --push
   ```

2. **Connect to Cloudflare Pages**
   - Go to [Cloudflare Dashboard → Pages](https://dash.cloudflare.com/?to=/:account/pages)
   - Click "Create a project" → "Connect to Git"
   - Select the `heartland-automations-web` repo
   - Build settings: leave blank (static site, no build step)
   - Deploy

3. **Custom Domain**
   - In Cloudflare Pages project settings → Custom domains
   - Add `heartlandautomations.com` and `www.heartlandautomations.com`
   - Cloudflare handles DNS + SSL automatically if the domain is on Cloudflare

4. **Update Calendly Link**
   - Search `index.html` for `https://calendly.com/heartlandautomations`
   - Replace with your real Calendly scheduling URL

## Stack

- Pure HTML + CSS (no build tools, no frameworks)
- Google Fonts (Inter)
- Minimal JS for mobile nav toggle only
