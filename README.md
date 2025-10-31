# VDT Berlin Website

Modern, responsive website for VDT Berlin travel agency.

## Quick Start

### 1. Copy Your Files
Add these folders from the old website:
- `images/` (head.jpg, foot.jpg, download.gif)


### 2. Edit Placeholders
Replace `[PLACEHOLDERS]` in:
- `impressum.html` - company info
- `datenschutz.html` - contact details

### 3. Deploy to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/[USERNAME]/vdt-berlin.git
git push -u origin main
```

### 4. Enable GitHub Pages
1. Go to repository Settings
2. Pages section
3. Source: main branch
4. Save

**Done! Your site is live with SSL at:**
`https://[USERNAME].github.io/vdt-berlin/`

## Custom Domain (Optional)

Create `CNAME` file:
```
www.vdt-berlin.de
```

Configure DNS:
```
Type: CNAME
Name: www
Value: [USERNAME].github.io
```

## File Structure

```
vdt-berlin-website/
├── index.html
├── impressum.html
├── datenschutz.html
├── css/
│   └── style.css
├── images/
│   ├── head1.jpg
│   ├── foot1.jpg
│   └── download.gif
└── download/
    ├── BangGiaVeMayBay.pdf
    ├── DatMuaVeMaybay.pdf
    └── HuongDanLayVeTau.pdf
```

## Support

Questions? Check the deployment guide in the documentation folder.
