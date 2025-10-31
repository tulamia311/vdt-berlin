# VDT Berlin - Deployment Guide

## Step-by-Step Deployment to GitHub Pages

### Prerequisites
- GitHub account (free)
- Git installed on your computer
- The old website files (images and PDFs)

---

## Step 1: Prepare Your Files

### 1.1 Copy Images
From the old website, copy these files to `images/` folder:
- `head1.jpg`
- `foot1.jpg`
- `download.gif`

### 1.2 Copy PDFs
From the old website, copy these files to `download/` folder:
- `BangGiaVeMayBay.pdf`
- `DatMuaVeMaybay.pdf`
- `HuongDanLayVeTau.pdf`

### 1.3 Fill in Legal Information

**Edit `impressum.html`** - Replace these placeholders:
```
[FIRMENNAME] → Your company name
[RECHTSFORM] → e.g., "Einzelunternehmen"
[STRASSE UND HAUSNUMMER] → Your street address
[PLZ] → Postal code
[+49 XXX XXXXXXXX] → Your phone number
[info@vdt-berlin.de] → Your email
[NAME DER GESCHÄFTSFÜHRUNG] → Owner name
```

**Edit `datenschutz.html`** - Replace the same placeholders

---

## Step 2: Create GitHub Repository

### 2.1 Create New Repository
1. Go to https://github.com
2. Click "New repository"
3. Name: `vdt-berlin`
4. Description: "VDT Berlin Travel Agency Website"
5. Public repository
6. **Don't** initialize with README
7. Click "Create repository"

---

## Step 3: Upload Files to GitHub

### Option A: Using Git Command Line

```bash
# Navigate to your website folder
cd /path/to/vdt-berlin-website

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - VDT Berlin website"

# Add remote (replace USERNAME with your GitHub username)
git remote add origin https://github.com/USERNAME/vdt-berlin.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Option B: Using GitHub Desktop (Easier)
1. Download GitHub Desktop: https://desktop.github.com
2. Install and sign in
3. File → Add Local Repository
4. Choose your `vdt-berlin-website` folder
5. Click "Publish repository"

---

## Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Scroll to "Pages" section (left sidebar)
4. Under "Source":
   - Branch: `main`
   - Folder: `/ (root)`
5. Click "Save"

**Wait 2-3 minutes**, then your site will be live at:
```
https://USERNAME.github.io/vdt-berlin/
```

**SSL/HTTPS is automatic!** ✅

---

## Step 5: Custom Domain (Optional)

If you want to use `www.vdt-berlin.de`:

### 5.1 Add CNAME File
Create a file named `CNAME` (no extension) in the root folder with content:
```
www.vdt-berlin.de
```

Push to GitHub:
```bash
git add CNAME
git commit -m "Add custom domain"
git push
```

### 5.2 Configure DNS
At your domain registrar (where you bought vdt-berlin.de):

**Add CNAME Record:**
```
Type: CNAME
Name: www
Value: USERNAME.github.io
TTL: 3600
```

**For root domain (optional):**
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

### 5.3 Enable HTTPS
1. Wait 24 hours for DNS propagation
2. Go to GitHub repository Settings → Pages
3. Check "Enforce HTTPS"
4. Done! ✅

---

## Step 6: Test Your Website

### Test Checklist:
- [ ] Homepage loads correctly
- [ ] Images display properly
- [ ] PDF downloads work
- [ ] Links to Vietnamese embassy work
- [ ] Impressum page accessible
- [ ] Datenschutz page accessible
- [ ] Mobile responsive (test on phone)
- [ ] HTTPS/SSL working (green padlock)

### Test on Multiple Devices:
- Desktop browser
- Mobile phone
- Tablet
- Different browsers (Chrome, Firefox, Safari)

---

## Updating Your Website

To make changes:

```bash
# Edit files locally
# Then:
git add .
git commit -m "Update content"
git push

# Changes live in 1-2 minutes!
```

---

## Troubleshooting

### Images not showing?
- Check file names match exactly (case-sensitive)
- Ensure images are in `images/` folder
- Clear browser cache

### PDFs not downloading?
- Check files are in `download/` folder
- Check file names in `index.html` match exactly

### Custom domain not working?
- Wait 24-48 hours for DNS propagation
- Check DNS settings at registrar
- Verify CNAME file exists in repository

### Page not updating?
- Wait 2-3 minutes after push
- Clear browser cache (Ctrl+F5)
- Check GitHub Actions for build errors

---

## Cost Summary

| Item | Cost |
|------|------|
| GitHub Pages Hosting | **FREE** |
| SSL Certificate | **FREE** |
| Bandwidth | **FREE** (unlimited) |
| Domain (optional) | ~€10/year |

---

## Support

Need help? Contact:
- GitHub Pages Docs: https://docs.github.com/pages
- GitHub Support: https://support.github.com

---

**Congratulations! Your website is now modern, secure, and free to host!** 🎉
