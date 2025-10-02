## ethanriver.page

Static landing page with social links for `ethanriver.page`.

### Update your links

- Edit `index.html` and replace `your_handle` in the link `href`s.
- Update email address and any networks you want to add or remove.

### Local preview

Any static file server works. With Python 3:

```bash
cd /Users/ethan/ethanriver.page
python3 -m http.server 8787
```

Open `http://localhost:8787`.

### Deploy on Cloudflare Pages

You already have DNS with Cloudflare. Deploy with Pages:

1. Commit this folder to a new Git repository (GitHub/GitLab/Bitbucket).
2. In Cloudflare Dashboard → Pages → Create project → Connect to your repo.
3. Build settings:
   - Framework preset: None
   - Build command: (leave empty)
   - Build output directory: `/`
4. After first deploy, add a custom domain:
   - Pages project → Custom domains → `ethanriver.page`
   - Approve/verify DNS. Cloudflare will handle the `CNAME` automatically.
5. Set redirects (optional): Pages → Routing → Add rule → `/*` → `index.html` (Serve Single Page App) to ensure deep links resolve.

### Optional enhancements

- Replace `assets/favicon.svg` with your own.
- Add analytics (Cloudflare Web Analytics is easy and free).
- Add `security.txt` at `/.well-known/security.txt`.
- Add `humans.txt` with credits or contact.



