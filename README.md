# SprayTrace landing page

Static site for GitHub Pages. No build step: `index.html` plus the `assets/` folder.

## Publish on GitHub Pages (about 5 minutes)

1. Create a public repository named `spraytrace-site` under your GitHub account.
2. Upload everything in this folder (including the hidden `.nojekyll` file) to the repository root.
3. In the repository: Settings → Pages → Build and deployment → Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`. Save.
4. The site appears at `https://siddharthabora.github.io/spraytrace-site/` within a few minutes.

If you use a different repository name, change the two `og:` URLs near the top of `index.html` so link previews show the right image.

## Connect the contact form (Formspree)

1. In Formspree, create a new form (for example "SprayTrace pilot enquiries") with the inbox that should receive enquiries.
2. Copy its form ID (the part after `/f/` in the endpoint, such as `xrejqzlj`).
3. In `index.html`, replace `REPLACE_WITH_FORM_ID` with that ID. It appears once, in the form's `action`.
4. Submit a test enquiry from the live site and confirm it in Formspree. The first submission may ask you to verify the address.

Until the ID is set, the form shows "This form is not connected yet" instead of failing silently.

## Add the Gemini images

Save the images with these exact names in `assets/img/`:

- `hero-tag-on-sprayer.jpg` (16:9, the large one)
- `field-worker-spraying.jpg`
- `tag-closeup-studio.jpg`
- `mixing-point.jpg`
- `division-hub.jpg`
- `supervisor-alert.jpg`

The "Built for the tea garden" section stays hidden until at least one of these files exists, and each picture appears only if its file loads. Keep images under about 400 KB each (JPEG, 1600 px wide is plenty).

## Files

- `assets/logo/`: logo in SVG and PNG for dark and light backgrounds, the droplet mark, favicons
- `assets/video/spraytrace-demo.mp4`: 65 s demo with voice-over and burned-in subtitles
- `assets/og-image.png`: link preview image (1200×630)
