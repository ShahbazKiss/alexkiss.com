# alexkiss.com

A daily page, written by hand, typed up, put online. Nothing else to maintain.

## Every day

1. Open `_new-page-template.md` in Notepad++, change the title, type the page.
2. Save it as a new file in `_posts/`, named with the day's date and a few words:
   `_posts/2026-11-16-on-listening.md`
   (Notepad++: *Encoding → UTF-8* if accents look wrong.)
3. Upload that one file:
   - **in the browser:** on github.com open the repository, click into `_posts`,
     then *Add file → Upload files*, drop the file in, press *Commit changes*; or
   - **with GitHub Desktop:** save straight into the local copy of the repository,
     write a word in the summary box, *Commit*, then *Push origin*.
4. About a minute later the page is live, on the front page, in *All pages*,
   in the feed and in the sitemap.

Writing in Dutch that day? Same steps, in the alexkiss.nl repository.

**Correcting a page:** edit the file and upload it again under the same name.
**Removing a page:** delete the file on github.com.
**An image (e.g. a scan):** upload it to an `images/` folder and write
`![what it shows](/images/2026-11-16.jpg)` where it should appear.

## Once: before the first page

- In `_config.yml`, fill in the three lines at the top: `author` (your name for
  the copyright line), `footer_note` (your line about the other site) and,
  if you like, `description`.

## Once: putting it online (free)

1. Make a free account on github.com.
2. *New repository* → name it `alexkiss.com` → **Public** → *Create*.
3. *uploading an existing file* → drag in **everything in this folder**,
   including the `_layouts`, `_includes`, `_posts` and `assets` folders → *Commit changes*.
4. *Settings → Pages*: Source **Deploy from a branch**, branch **main**, folder **/(root)** → *Save*.
5. Same page, *Custom domain*: `alexkiss.com` → *Save*.
6. At **Vimexx** (DNS settings for alexkiss.com):
   - remove the current forwarding to deluisterij.nl;
   - four **A** records for `@` (the bare domain):
     `185.199.108.153` · `185.199.109.153` · `185.199.110.153` · `185.199.111.153`
   - optional, four **AAAA** records for `@`:
     `2606:50c0:8000::153` · `2606:50c0:8001::153` · `2606:50c0:8002::153` · `2606:50c0:8003::153`
   - one **CNAME** record: `www` → `YOUR-GITHUB-USERNAME.github.io`
7. Wait until *Settings → Pages* shows the domain check as successful (minutes to a
   few hours), then tick **Enforce HTTPS**.
8. Protect the domain: GitHub profile *Settings → Pages → Add a domain* → `alexkiss.com`,
   and add the TXT record GitHub shows you at Vimexx. This stops anyone else's
   GitHub site from claiming your domain.

Moving the domain from Vimexx to Spaceship later changes nothing here:
recreate the same DNS records at Spaceship.

## What is where

| File | What it does |
|---|---|
| `_posts/` | the pages — the only folder you touch day to day |
| `_config.yml` | name, footer line, labels, licence |
| `_layouts/`, `_includes/` | the page templates |
| `assets/style.css` | the look (Paper) |
| `assets/fonts/` | EB Garamond, served from this site so no visitor data goes to Google |
| `index.html` | front page: newest page in full, three earlier ones listed |
| `pages.html` | *All pages*, grouped by month |
| `404.html` | shown at addresses that don't exist |
| `CNAME` | tells GitHub which domain this is |

No analytics, no comments, no counters, no JavaScript.
