# nmimpactlab.github.io

Source for the public New Mexico Impact Lab website — an independent, public-interest
data project that makes New Mexico government records usable.

**Live site:** https://nmimpactlab.org

## What this is
A dependency-free static site (plain HTML/CSS, no build step). GitHub Pages serves it
directly. The `.nojekyll` file tells Pages to skip Jekyll processing and serve the files
as-is.

## Structure
```
/                      index.html         Home
/investigations/       index + one page per investigation
/data/                 Datasets hub
/methodology.html      How we collect, verify, and publish
/about.html            About the project
/contact.html          Contact (research@nmimpactlab.org)
/assets/css/style.css  Styles (light + dark)
/404.html              Not-found page
/CNAME                 Custom domain (nmimpactlab.org)
/sitemap.xml, robots.txt
```

## Local preview
It's static — open `index.html` in a browser, or run a simple server from this folder:
```
python -m http.server 8080
# then visit http://localhost:8080/
```

## Custom domain
`CNAME` is set to `nmimpactlab.org`. In **Settings → Pages**, confirm the custom domain
and enable **Enforce HTTPS** once DNS validates. `nmimpactlab.com` is handled as a
registrar-level 301 redirect to the `.org`.

## Editing
Each page is standalone HTML that shares `/assets/css/style.css`. The header and footer
are duplicated per page (no template engine). When adding a nav link or footer item,
update it across pages.

## Contributing data
Datasets are published only after they clear an internal sourcing/access/privacy review.
Everything published is drawn from public records, with sources preserved. See
[methodology](https://nmimpactlab.org/methodology.html).
