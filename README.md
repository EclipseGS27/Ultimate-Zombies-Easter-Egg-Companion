# Kronorium

A zombies easter egg companion for Black Ops 1 to Black Ops 4: step-by-step main quest guides with a video for every quest step, progress tracking, and the story of the Aether.

The whole site is one file. `index.html` and `Main Website` are the same page.

## Videos

Each step has a collapsible video that plays just that step: the stretch of a full walkthrough from where the step starts to where the next one begins. When it ends, one tap plays the next step. Scroll away while one plays and it docks in the corner. Step times come from each video's chapters, either the creator's own or chapters generated from the video's timed captions. YouTube only plays embedded videos on a page opened from a web address, so host the site to get them:

1. On GitHub, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the branch with `index.html` and the `/ (root)` folder, then **Save**.
3. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

Opened as a saved file, the site still works, and its videos open on YouTube instead.

## Changing a video or its times

Open the site with `?edit` at the end of the address, for example `https://<your-username>.github.io/<repository-name>/?edit`. Editing stays on in that browser until you press **Stop editing**. Visitors never see any of it.

- Open any step's video. Under it, paste a different YouTube link, or change **Starts at** and **Ends at**. Type a time like `4:32`, or press **Now** while the video plays to use the moment it is at. A link with `?t=` in it sets the start for you.
- **Save** makes it the step's first video. **Remove this video from the step** drops a video you don't want. **Undo my changes** puts the step back as it was.
- Steps with no video show **Add a video**.
- The banner also shows **Use my image** and **Use my track**, which swap a map's art or music in your browser only. Visitors don't see these buttons, and everyone else always gets the built-in art and music.

Changes show straight away, but only in your browser. To publish them for everyone, press **Download videos.json**. Then, on GitHub, choose **Add file → Upload files**, drop the file in, and press **Commit changes**. It replaces `videos.json` in the repository, and the site picks it up within a few minutes.

