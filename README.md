# Nemo’s Eye — Deep & Dark Web Search

**Live:** https://nemocyberworld.github.io/hacktolive-search/  


Client-only meta search that **builds smart links** for clear, deep, and dark web tools. No servers, no tracking, no storage.

## Features
- Clear / Deep / Dark categories loaded from `/tools/*.json`
- Quick + advanced **filetype/dork** filters (incl. custom extensions)
- “**Use Tor — Dive Deeper**” button (copies/opens the last tool link)
- Single-file app (`index.html`), Tailwind via CDN

## Run it
### A) GitHub Pages (clearnet)
Open: **https://nemocyberworld.github.io/hacktolive-search/**

### B) Tor Browser (file://)
1) Download/clone the repo  
2) Keep `index.html` and the `tools/` folder **side by side**  
3) Open `index.html` **in Tor Browser** (drag-drop or Ctrl/Cmd+O)  
> If your system blocks `file://` JSON fetches, use the local server below.

### C) Local server (Chrome/Firefox/Edge or Tor)
**Python**
```bash
python -m http.server 8000
# visit http://localhost:8000
````

**Node**

```bash
npx http-server -p 8000
```

## Structure

```
hacktolive-search/
├─ index.html
└─ tools/
   ├─ clear.json
   ├─ deep.json
   └─ dark.json
```

**Tools JSON:** each file exports `{ "label", "groups": [ { "label", "engines": [ { "name", "url", "desc" } ] } ] }`.
Use **`{q}`** in `url` where the query should go.

## “Use Tor” button (quick note)

* Remembers the **last clicked tool URL**; shows copy/Ahmia options if not already in Tor Browser.


## Credits & License

Built by [Captain Nemo](https://github.com/nemocyberworld) with [HackToLive Academy](https://hacktolive.net). 
MIT Lincence
