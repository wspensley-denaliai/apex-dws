# Publishing the APEX DWS Sales Pack to GitHub Pages

This folder contains everything you need. **`index.html`** is the whole
interactive sales pack in one file (3D configurator, fonts, logos, video —
all self-contained). Publishing it gives you one public link you can send
to anyone, in or outside your organisation. It's **free**.

---

## Part 1 — Get it live (about 5 minutes, no coding)

### 1. Create a repository
1. Go to **https://github.com/new** (sign in first).
2. **Repository name:** `apex-dws` (or anything you like).
3. Set it to **Public**.
   *(Private repos can also publish Pages, but only on a paid GitHub plan.
   Public is simplest and the code here is just a demo page.)*
4. Leave everything else default → **Create repository**.

### 2. Upload the file
1. On the new repo page, click **Add file → Upload files**.
2. Drag **`index.html`** (from this folder) into the upload area.
   > The file MUST be named `index.html` — that's what makes it open at the
   > clean root URL. If it's named anything else, rename it before uploading.
3. Scroll down → **Commit changes**.

### 3. Turn on GitHub Pages
1. In the repo, open **Settings** (top menu) → **Pages** (left sidebar).
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. **Branch:** `main`  ·  **Folder:** `/ (root)` → **Save**.
4. Wait ~1 minute, then refresh the Pages screen.

### 4. Share the link
At the top of the Pages screen you'll see:

```
https://<your-username>.github.io/apex-dws/
```

That is your public link. Send it to anyone — it opens in any modern
browser (Chrome, Edge, Safari), on desktop or mobile, no download needed.
HTTPS is automatic.

---

## Part 2 — Use your own domain (optional)

Hosting stays free; you only pay for the domain name (~£8–12 / year).

1. **Buy a domain** from any registrar — Cloudflare, Namecheap, GoDaddy, etc.
   (e.g. `apexdws.com`).
2. In your repo: **Settings → Pages → Custom domain**, type the domain →
   **Save**. This adds a `CNAME` file to the repo automatically.
3. At your **registrar's DNS settings**, add records:
   - For a root domain (`apexdws.com`): four **A records** pointing to
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
     `185.199.111.153`.
   - For a subdomain (`apex.apexdws.com`): one **CNAME** record pointing to
     `<your-username>.github.io`.
4. Back on the Pages screen, tick **Enforce HTTPS** once it becomes available
   (GitHub issues the SSL certificate for free — can take up to an hour).

Your link becomes `https://apexdws.com`.

---

## Updating it later
Re-upload a new `index.html` (**Add file → Upload files**, same name,
Commit). The link stays identical; changes appear within a minute or two.

## Good to know
- **File size:** ~23 MB (mostly the embedded demo video). Well within
  GitHub's limits (100 MB per file, 100 GB bandwidth / month). First load
  takes a few seconds while the video downloads; after that it's instant.
- **Want it to load faster?** The video can be split into a separate file so
  the page itself is ~1 MB and the video streams. Ask and I'll prepare that
  two-file version (`index.html` + `dws-demo.mp4`).
- **Access:** a GitHub Pages site is public to anyone with the link. If you
  need it gated (password / org-only), tell me and I'll suggest a host that
  supports that.
