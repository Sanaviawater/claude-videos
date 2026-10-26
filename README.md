# Sanavia videos

Sanavia's video projects, built with [Remotion](https://www.remotion.dev) and edited by asking Claude in plain English. This repo holds the project files. Finished videos and raw footage stay on your own computer.

## First-time setup (Mac)

You only do this once. It takes about 15 minutes.

### 1. Get access to this repo

This repo is private.

**Signing in with the Sanavia support GitHub account (`Sanaviawater`)?** It owns this repo, so skip this step. Just sign in to GitHub with it when Claude asks in step 4.

Using your own GitHub account instead:

1. If you don't have a GitHub account, make a free one at [github.com/signup](https://github.com/signup).
2. Send your GitHub username to the Sanavia account owner. They add you under **Settings → Collaborators → Add people**.
3. Accept the invite. It arrives by email, or appears at [github.com/notifications](https://github.com/notifications). **Setup won't work until you accept it.**

### 2. Install Node.js

Node.js is the program that runs the video tool.

1. Check your Mac's chip: click the Apple logo  at the top left, then **About This Mac**.
   - **Apple M1, M2, M3, M4 or M5:** you need the **ARM64** version.
   - **Intel:** you need the **x64** version.
2. Go to [nodejs.org/en/download](https://nodejs.org/en/download). Skip the code box at the top. Under "Or get a prebuilt Node.js", pick **macOS** and your chip, then click **macOS Installer (.pkg)**.
3. Open the downloaded file and click Continue → Continue → Agree → Install. Enter your Mac password, then click Close.

### 3. Install the Claude desktop app

Download it from [claude.ai/download](https://claude.ai/download) and sign in to your Claude account. You need a plan that includes Claude Code.

### 4. Download the project with Claude

1. In the Claude app, open the **Code** tab and click **+ New**.
2. Check that the bottom bar says **This computer**. That makes Claude work on your Mac, not in the cloud.
3. Click **Choose…** next to the folder icon and pick your **Documents** folder.
4. Paste this and press Enter:

   > Clone https://github.com/Sanaviawater/claude-videos into ~/Documents/claude-videos. It's a Remotion video project. Then run npm install and npm run dev to open Remotion Studio in my browser.

5. Approve when Claude asks to run commands. If it asks you to sign in to GitHub, sign in with **Sanaviawater** (the support account), or with the account that accepted the invite.

When it's done, **Remotion Studio** opens in your browser. That's where you watch videos as they're built.

## Making a video

1. **Add your footage.** In Finder, open **Documents → claude-videos → public → clips** (create the `clips` folder if it isn't there) and drag your videos in. To save clips someone texted you, click their name at the top of the Messages conversation, then **Info → Photos**, select the videos and drag them into `clips`.
2. **Describe the video to Claude.** Say what it's for, how long it should be, and the shape (vertical for Reels and TikTok, wide for YouTube and the website). For example:

   > Look at the clips in public/clips and make a 30-second vertical video from the best moments, with captions and our logo. End on "Book your free water test at sanaviawater.com".

   > Make a 20-second vertical product video for the Hydra from public/products/hydra/01-hero.png. Cut the product out of its white background, slow zoom, three feature callouts, and end on "Shop now at sanaviawater.com".

3. **Watch it in Studio.** Click the video in the left-hand list and press **space** to play. Ask for changes in plain words, like "make the text bigger" or "cut the second clip shorter".
4. **Export it.** Say **"render it"**. The finished MP4 lands in `Documents/claude-videos/out/`, ready to upload.

## Every time after that

- In the Claude **Code** tab, click **+ New**, check it says **This computer**, and use **Choose… → Documents → claude-videos**.
- Start with **"Pull the latest from GitHub"** to get anyone else's changes.
- When you're happy with your work, say **"Commit and push my changes"** to back it up and share it with the team.

## What's in here

| Folder | What it's for |
|---|---|
| `public/products/` | Product photos from the Shopify store (Hydra, filters, bundle) |
| `public/clips/` | Your raw footage. **Stays on your computer only** and isn't uploaded to GitHub, because phone videos are often too big. Keep the originals in Photos or Messages. |
| `src/` | The video designs. Claude edits these for you. |
| `out/` | Finished videos. Stays on your computer only. |

## If something goes wrong

- **"Repository not found" when cloning:** you either haven't accepted the GitHub invite yet, or your Mac is signed in to a different GitHub account. Tell Claude: "Sign me in to GitHub with gh auth login", then sign in with **Sanaviawater** or the account that was invited.
- **Studio isn't showing up:** tell Claude "start the preview" (it runs `npm run dev`).
- **A "vulnerabilities" warning during install:** normal for a tool that only runs on your computer. Ignore it.

## Commands

Claude runs these for you, but in case you want them:

| Command | What it does |
|---|---|
| `npm install` | Install the tools the project needs |
| `npm run dev` | Open Remotion Studio |
| `npx remotion render` | Render a video to `out/` |

Remotion is free for teams of up to 3 people. Larger companies need a [company license](https://www.remotion.pro/license).
