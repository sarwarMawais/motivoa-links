# Motivoa — public pages

The privacy policy, terms and support page for the **Motivoa** Android app
(`com.affirmdaily.motivation`), published via GitHub Pages so Google Play and AdMob
have public URLs to point at.

These files are the **source of truth** and live in the app repository under `website/`.
Edit them there and copy them here — never the other way round, or the app's in-app legal
text and the hosted pages will drift apart.

## Files

| File | Purpose |
|---|---|
| `index.html` | Landing page. Use as the **developer website** in the Play listing |
| `privacy.html` | **Privacy Policy.** Required by Play, by AdMob's consent messages, and by the Data Safety form |
| `privacy.html#delete` | The **data deletion** anchor. This is the URL the Data Safety form asks for |
| `terms.html` | Terms of Service |
| `app-ads.txt` | Authorised sellers for AdMob. See the note below — it only works at a domain root |

## Enabling GitHub Pages

1. Create a public repository named `motivoa-links`.
2. Commit these files to the root of the `main` branch.
3. **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save.**
4. Wait a minute, then confirm each page loads in a private window with no login:
   - `https://sarwarmawais.github.io/motivoa-links/`
   - `https://sarwarmawais.github.io/motivoa-links/privacy.html`
   - `https://sarwarmawais.github.io/motivoa-links/terms.html`

Use those `github.io` URLs in Play Console and AdMob — **not** `github.com/.../blob/...` links,
which render GitHub's code viewer rather than the page itself.

## The app-ads.txt caveat

AdMob does not look for `app-ads.txt` next to your pages. It reads the **developer website**
from your Play listing, then fetches `app-ads.txt` from the **root of that domain**.

With a project page at `sarwarmawais.github.io/motivoa-links/`, the root is
`sarwarmawais.github.io/`, so the file has to live in a repository named
**`sarwarMawais.github.io`** — not in this one. Two ways to make it work:

- create that user-site repository and put `app-ads.txt` in it, or
- point a custom domain at this repository and serve `app-ads.txt` from its root.

Until one of those is done, `app-ads.txt` here is inert. It is not a launch blocker — it
protects ad revenue from spoofed inventory, which matters once there is revenue to protect.
