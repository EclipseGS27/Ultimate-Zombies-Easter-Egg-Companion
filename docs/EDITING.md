# Maintaining Kronorium

This page is for the site's owner. Visitors don't need any of it, and nothing here changes the public site unless it is committed to this repository.

The whole site is one file, plus the puzzle screenshots in `img/`. `index.html` and `Main Website` are the same page.

## How the step videos work

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
- **Delete step** under a step, or **Delete section** under a section's title, removes it for visitors once published. You confirm before anything goes. Deleted items stay in your editor greyed out with a **Restore** button, before or after publishing. Progress counts leave them out.
- The banner also shows **Use my image** and **Use my track**, which swap a map's art or music in your browser only. Visitors don't see these buttons, and everyone else always gets the built-in art and music.

Changes show straight away, but only in your browser. To publish them for everyone, press **Download videos.json**. Then, on GitHub, choose **Add file → Upload files**, drop the file in, and press **Commit changes**. It replaces `videos.json` in the repository, and the site picks it up within a few minutes.

## Puzzle screenshots

Black Ops 7 steps with a cipher or puzzle show screenshots under the step text. A tap opens one full screen. The images live in `img/bo7/`. Most are frames from the step's own guide video. The two pigpen sheets for Ashes of the Damned (`aotd-yuri-pigpen.svg` and `aotd-monitor-pigpen.svg`) are drawn for this site.

To swap a picture, upload a new file under the same name in `img/bo7/`. To add, move or re-caption one, edit the `const SHOTS = {...}` line in `index.html`. It maps a step id to a list of pictures:

```js
'aotd-serum-2': [['img/bo7/aotd-yuri-lab.jpg', 'Caption shown under the picture', 'XGc-_4sT9dE', 905]]
```

The last two values are the YouTube video and the second the frame comes from. They make the "From … at 15:05" link under the picture. Use `''` and `0` for a picture that isn't from a video. Step ids are the map id, the section id and the step's number from 0, so `aotd-serum-2` is the third step of the Serum section in Ashes of the Damned. Copy any change to `Main Website` too.

