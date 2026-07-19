# Wordhoard site

Static GitHub Pages site for Wordhoard's App Store URLs.

- `index.html` — support page (use as the **Support URL** in App Store Connect)
- `privacy.html` — privacy policy (use as the **Privacy Policy URL**)
- `.nojekyll` — tells GitHub Pages to serve the files as-is

## Publishing

```sh
cd ~/wordhoard-site
git init -b main
git add -A
git commit -m "Wordhoard support site and privacy policy"
# create an empty PUBLIC repo named wordhoard-site on github.com, then:
git remote add origin git@github.com:<your-username>/wordhoard-site.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Deploy from a branch**, select `main` / `/ (root)`, save. After a minute or two the site is live at:

- Support URL: `https://<your-username>.github.io/wordhoard-site/`
- Privacy Policy URL: `https://<your-username>.github.io/wordhoard-site/privacy.html`

(If you have the `gh` CLI, the create+push steps collapse to
`gh repo create wordhoard-site --public --source=. --push`.)
