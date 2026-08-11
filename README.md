# Fivefold — installing on your iPhone (free)

This folder is a complete, installable web app (PWA). No build step, no cost.
Files: index.html, manifest.webmanifest, sw.js, icon-180/192/512.png

## 1. Put it online (pick ONE, both free, no card)

### Option A — Netlify Drop (fastest)
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page.
3. You get a public https link like https://something.netlify.app — that's your app.
   (Make a free account if you want the link to stay permanent.)

### Option B — GitHub Pages
1. Create a free GitHub account, make a new public repository.
2. Upload all the files in this folder to it.
3. Repo → Settings → Pages → Source: "Deploy from branch", pick main / root, Save.
4. After a minute your app is at https://<you>.github.io/<repo>/

> It must be served over https (both options are). Opening index.html directly
> from your files won't work — the service worker and AI calls need a real https URL.

## 2. Add it to your iPhone home screen
1. Open the https link in **Safari** (not Chrome — only Safari can install PWAs on iOS).
2. Tap the **Share** button → **Add to Home Screen** → Add.
3. It now has its own icon and opens fullscreen, like a normal app.

## 3. Turn on the AI features (optional, free)
The planner, streak, food log, weigh-ins and reading all work with no key.
The **generate / suggest** buttons need a free Gemini key:
1. Go to https://aistudio.google.com → sign in with a Google account.
2. Create an API key (no credit card, no billing setup).
3. In the app: tap the **gear (Settings)** → "AI key" → paste it → Save.

That's it. Your data stays on your phone; the only thing that leaves the device
is the text you send to Gemini when you tap a generate button.

## Known limits of this first version
- **Events search** is off for now (it needed a live web search). The Socialising
  planner falls back to generated "things to do with people" ideas instead.
- **Reminders / the interrupter** (notifications) aren't in yet — that's the next step.
- Free Gemini tier: generous daily limits (fine for one person), and Google may use
  free-tier inputs to improve their models.
