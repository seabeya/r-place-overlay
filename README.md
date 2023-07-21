<h1 align="center">R-Place Overlay</h1>

<p align="center">
  Overlay for Reddit Place event
<p>

<br>

> **Note**:
> Only works on PC.

---

### 🔷 How To Use

1. Install the extension.
   - Chrome: [Tampermonkey - Chrome Web Store](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo).
   - Firefox: [Tampermonkey - Firefox Addons](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/).
2. Install the main script:
   > https://github.com/osuplace/templateManager/raw/main/dist/templateManager.user.js
3. Activate the overlay.

   1. Go to: https://www.reddit.com/r/place (refresh the page).
   2. Click the settings icon (top left):
      > ![settings-icon](https://github.com/shaanaliyev/r-place-overlay/assets/35802638/e0f2aa9a-268d-4933-b49b-670c0ccdc706)
   3. Enter your Template URL here:

      > ![image](https://github.com/shaanaliyev/r-place-overlay/assets/35802638/2f34f7c7-d058-4101-b28b-7b9e9c2c38cb)

      > If you don't have a ready template, please have a look at the ["How To Create A Template"](#-how-to-create-a-template) section.

   4. Click "Always load".

      > If prompted for permission, click "Always allow domain".

      > ![image](https://github.com/shaanaliyev/r-place-overlay/assets/35802638/ed806b67-882e-409d-8e9d-01b2d37c20c4)

   5. Done! You will now see the template overlay on the Reddit Place canvas.

<br>

### 🔷 How To Create A Template

1. You need to prepare an image.
   > The image should be ready (properly resized).
2. Go to https://imgur.com or any other image hosting platform and upload your image.

   > The image URL should end with the correct image format, such as .png, .webp, etc.

   > To get the correct URL after a successful upload, right-click and choose either "Copy image address" or "Open image in a new tab," then copy the URL.

   > The image you are using should be pixel-perfect sized with the canvas. This means, for example, you cannot use a 1600x1200 image to fit a 25x10 space.

3. Preparing the template.

   1. Go to: https://rentry.co
   2. Enter the base template:
      ```json
      {
        "contact": "https://github.com/shaanaliyev",
        "templates": [
          {
            "name": "NAME_YOUR_ART",
            "sources": ["PASTE_IMAGE_URL_HERE"],
            "x": 0,
            "y": 0
          }
        ]
      }
      ```
   3. Replace the data with yours.
      - `name`: Can be anything.
      - `sources`: Paste the image URL that you prepared.
      - `x` and `y`: Top-left starting points for your art on the canvas.
        > The script takes (0, 0) as the starting points. So, you need some calculations here. If you want to go down, add to `y`; if you want to go right, add to `x`.
   4. Click "Go" > "Export" > "Raw" and copy the URL.

      > Done! This is your Template URL. Share this URL with others to collaborate together.

      > They need to follow the ["How to use"](#-how-to-use) section to use the template.

Extra:

> You can update the template on (https://rentry.co) by clicking the edit button anytime you need. The users will get the update automatically just after they refresh the r/place page.

> Also, you can work on multiple images following this syntax:
>
> ```json
> {
>   "contact": "https://github.com/shaanaliyev",
>   "templates": [
>     {
>       "name": "NAME_YOUR_ART_1",
>       "sources": ["PASTE_IMAGE_1_URL_HERE"],
>       "x": 0,
>       "y": 0
>     },
>     {
>       "name": "NAME_YOUR_ART_2",
>       "sources": ["PASTE_IMAGE_2_URL_HERE"],
>       "x": 0,
>       "y": 0
>     }
>   ]
> }
> ```

<br>

---

Looking for R-Placer? (It's a different r/place project.) Have a look: https://shaanaliyev.github.io/r-placer

> Useful for:
>
> - Sharing coordinates with other communities.
> - People who don't want to (or can't) install an overlay.
