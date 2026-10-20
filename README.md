# Omkar & Shreya — Wedding Invitation Website

A responsive, bilingual (English/Marathi) static wedding invitation site.

## Included
- Royal burgundy, ivory and gold design
- Animated hero and scroll reveals
- English/Marathi language toggle
- Countdown to 27 December 2026 (India Standard Time)
- Engagement and wedding event cards with placeholders for unknown details
- Sample wedding gallery images
- Navi Mumbai venue search link
- RSVP form that opens the visitor's email app

## Preview locally
1. Unzip the download.
2. Open `index.html` in a browser. Internet access is needed for Google Fonts and sample Unsplash images.

## Before publishing
1. Open `index.html` in a text editor.
2. Search for `const RSVP_EMAIL = "your-email@example.com";`
3. Replace it with the email address that should receive RSVPs.
4. Replace sample images in the gallery with your own image URLs if desired.
5. Update engagement date/time and the final venue address once confirmed.

**RSVP note:** This is a static website. The form uses a `mailto:` link and does not store submissions in a database. For reliable RSVP collection without requiring guests to have an email app configured, connect a form service (such as Formspree) or add a backend.

## Publish on Vercel (free)
1. Create/sign in to a Vercel account at https://vercel.com/
2. Create a GitHub repository and upload `index.html` (and this README if you want).
3. In Vercel, choose **Add New → Project**, import the repository, and deploy.
4. Framework preset: **Other**. Build command: leave empty. Output directory: `.` (or leave the default if detected).
5. Once deployment finishes, Vercel gives you a public `*.vercel.app` URL you can share on WhatsApp.

### Quick alternative
You can also use Netlify Drop at https://app.netlify.com/drop and drag the unzipped folder into the page for a quick static deployment.

## Customization
All styling and behavior are inside `index.html`, so no build tools or package installation are required.
