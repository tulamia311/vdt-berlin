# VDT Berlin - Minimal Website Relaunch (Low Budget)

**Goal**: Quick, minimal improvements with zero hosting costs  
**Budget**: €0 - €500  
**Timeline**: 1-2 weeks  
**Hosting**: GitHub Pages (free, includes SSL)

---

## What We'll Do

✅ Add SSL/HTTPS (automatic with GitHub Pages)  
✅ Make site responsive (mobile-friendly)  
✅ Add Impressum & Datenschutz pages  
✅ Keep all existing content  
✅ Fast deployment via GitHub  

---

## Implementation Plan

### Step 1: Convert to Modern HTML5 (Keep Content)

**File Structure:**
```
vdt-berlin/
├── index.html          # Main page (converted from table layout)
├── impressum.html      # Legal notice
├── datenschutz.html    # Privacy policy
├── css/
│   └── style.css       # Responsive styles
├── images/             # Existing images
│   ├── head1.jpg
│   ├── foot1.jpg
│   └── download.gif
└── download/           # Existing PDFs
    ├── BangGiaVeMayBay.pdf
    ├── DatMuaVeMaybay.pdf
    └── HuongDanLayVeTau.pdf
```

---

### Step 2: Modern HTML5 Code

**index.html** (Responsive version):
```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VDT Berlin - Flugtickets & Visa Service für Vietnam</title>
    <meta name="description" content="VDT Berlin - Ihr Reisebüro für Flugtickets nach Vietnam und Visa-Service. Chuyên vé máy bay đi Việt Nam.">
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <img src="images/head1.jpg" alt="VDT Berlin Header" class="header-image">
    </header>

    <main class="container">
        <section class="business-hours">
            <div class="hours-block">
                <h2>Geschäftszeiten</h2>
                <p>Mo. - Fr.: 9.00 - 17.00 Uhr<br>
                Sa. u. So. geschlossen</p>
            </div>
            <div class="hours-block">
                <h2>Giờ mở cửa</h2>
                <p>Thứ 2 - Thứ 6: 9.00 - 17.00 giờ<br>
                Thứ 7 và CN đóng cửa</p>
            </div>
        </section>

        <section class="services">
            <h2>Vé Máy Bay / Flugtickets</h2>
            <ul class="download-list">
                <li>
                    <a href="download/BangGiaVeMayBay.pdf" download>
                        📄 Bảng giá vé máy bay / Preisliste
                    </a>
                </li>
                <li>
                    <a href="download/DatMuaVeMaybay.pdf" download>
                        📄 Thông tin đặt mua vé máy bay
                    </a>
                </li>
                <li>
                    <a href="download/HuongDanLayVeTau.pdf" download>
                        📄 Hướng dẫn lấy vé tàu
                    </a>
                </li>
                <li>
                    <a href="http://www.vietnambotschaft.org" target="_blank" rel="noopener">
                        🔗 Các thủ tục lãnh sự
                    </a>
                </li>
            </ul>
        </section>
    </main>

    <footer>
        <img src="images/foot1.jpg" alt="VDT Berlin Footer" class="footer-image">
        <nav class="footer-nav">
            <a href="impressum.html">Impressum</a> | 
            <a href="datenschutz.html">Datenschutz</a>
        </nav>
        <p class="copyright">© 2025 VDT Berlin. Alle Rechte vorbehalten.</p>
    </footer>
</body>
</html>
```

---

### Step 3: Responsive CSS

**css/style.css**:
```css
/* Reset & Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f5f5f5;
}

/* Container */
.container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    background-color: white;
}

/* Header */
header {
    max-width: 800px;
    margin: 0 auto;
}

.header-image {
    width: 100%;
    height: auto;
    display: block;
}

/* Business Hours */
.business-hours {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin: 30px 0;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 8px;
}

.hours-block h2 {
    font-size: 1.2em;
    margin-bottom: 10px;
    color: #2c5aa0;
}

.hours-block p {
    font-size: 1em;
    line-height: 1.8;
}

/* Services Section */
.services {
    margin: 30px 0;
}

.services h2 {
    font-size: 1.5em;
    margin-bottom: 20px;
    color: #2c5aa0;
    border-bottom: 2px solid #2c5aa0;
    padding-bottom: 10px;
}

.download-list {
    list-style: none;
    padding: 0;
}

.download-list li {
    margin: 15px 0;
}

.download-list a {
    display: inline-block;
    padding: 10px 15px;
    color: #2c5aa0;
    text-decoration: none;
    border: 1px solid #2c5aa0;
    border-radius: 5px;
    transition: all 0.3s ease;
}

.download-list a:hover {
    background-color: #2c5aa0;
    color: white;
}

/* Footer */
footer {
    max-width: 800px;
    margin: 0 auto;
    text-align: center;
}

.footer-image {
    width: 100%;
    height: auto;
    display: block;
}

.footer-nav {
    padding: 20px;
    background-color: #2c5aa0;
    color: white;
}

.footer-nav a {
    color: white;
    text-decoration: none;
    padding: 0 10px;
}

.footer-nav a:hover {
    text-decoration: underline;
}

.copyright {
    padding: 10px;
    font-size: 0.9em;
    color: #666;
}

/* Mobile Responsive */
@media (max-width: 768px) {
    .container {
        padding: 15px;
    }
    
    .business-hours {
        grid-template-columns: 1fr;
        gap: 15px;
    }
    
    .hours-block h2 {
        font-size: 1.1em;
    }
    
    .services h2 {
        font-size: 1.3em;
    }
    
    .download-list a {
        display: block;
        margin: 10px 0;
    }
}

@media (max-width: 480px) {
    .container {
        padding: 10px;
    }
    
    .hours-block h2 {
        font-size: 1em;
    }
    
    .hours-block p {
        font-size: 0.9em;
    }
}
```

---

### Step 4: Impressum Page

**impressum.html**:
```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Impressum - VDT Berlin</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <img src="images/head1.jpg" alt="VDT Berlin Header" class="header-image">
    </header>

    <main class="container">
        <h1>Impressum</h1>
        
        <h2>Angaben gemäß § 5 TMG</h2>
        <p>
            <strong>[FIRMENNAME]</strong><br>
            [RECHTSFORM]<br>
            [STRASSE UND HAUSNUMMER]<br>
            [PLZ] Berlin<br>
            Deutschland
        </p>

        <h2>Kontakt</h2>
        <p>
            Telefon: [+49 XXX XXXXXXXX]<br>
            E-Mail: [info@vdt-berlin.de]
        </p>

        <h2>Vertreten durch</h2>
        <p>[NAME DER GESCHÄFTSFÜHRUNG]</p>

        <h2>Umsatzsteuer-ID</h2>
        <p>
            Umsatzsteuer-Identifikationsnummer gemäß §27a Umsatzsteuergesetz:<br>
            [DE XXXXXXXXX]
        </p>

        <h2>Verantwortlich für den Inhalt nach § 55 Abs. 2 RStV</h2>
        <p>
            [NAME]<br>
            [ADRESSE]
        </p>

        <h2>Haftungsausschluss</h2>
        
        <h3>Haftung für Inhalte</h3>
        <p>
            Die Inhalte unserer Seiten wurden mit größter Sorgfalt erstellt. 
            Für die Richtigkeit, Vollständigkeit und Aktualität der Inhalte 
            können wir jedoch keine Gewähr übernehmen.
        </p>

        <h3>Haftung für Links</h3>
        <p>
            Unser Angebot enthält Links zu externen Webseiten Dritter, auf deren 
            Inhalte wir keinen Einfluss haben. Deshalb können wir für diese 
            fremden Inhalte auch keine Gewähr übernehmen.
        </p>

        <h3>Urheberrecht</h3>
        <p>
            Die durch die Seitenbetreiber erstellten Inhalte und Werke auf diesen 
            Seiten unterliegen dem deutschen Urheberrecht.
        </p>

        <p><a href="index.html">← Zurück zur Startseite</a></p>
    </main>

    <footer>
        <img src="images/foot1.jpg" alt="VDT Berlin Footer" class="footer-image">
        <nav class="footer-nav">
            <a href="impressum.html">Impressum</a> | 
            <a href="datenschutz.html">Datenschutz</a>
        </nav>
    </footer>
</body>
</html>
```

---

### Step 5: Datenschutz Page

**datenschutz.html**:
```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Datenschutzerklärung - VDT Berlin</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <img src="images/head1.jpg" alt="VDT Berlin Header" class="header-image">
    </header>

    <main class="container">
        <h1>Datenschutzerklärung</h1>

        <h2>1. Datenschutz auf einen Blick</h2>
        
        <h3>Allgemeine Hinweise</h3>
        <p>
            Die folgenden Hinweise geben einen einfachen Überblick darüber, was mit 
            Ihren personenbezogenen Daten passiert, wenn Sie diese Website besuchen.
        </p>

        <h3>Datenerfassung auf dieser Website</h3>
        <p>
            <strong>Wer ist verantwortlich für die Datenerfassung auf dieser Website?</strong><br>
            Die Datenverarbeitung auf dieser Website erfolgt durch den Websitebetreiber. 
            Dessen Kontaktdaten können Sie dem Impressum dieser Website entnehmen.
        </p>

        <h2>2. Hosting</h2>
        <p>
            Diese Website wird auf GitHub Pages gehostet. Der Anbieter ist:<br>
            GitHub Inc., 88 Colin P Kelly Jr St, San Francisco, CA 94107, USA
        </p>
        <p>
            GitHub kann beim Aufruf dieser Website technische Informationen 
            erfassen, einschließlich Ihrer IP-Adresse.
        </p>

        <h2>3. Allgemeine Hinweise und Pflichtinformationen</h2>
        
        <h3>Datenschutz</h3>
        <p>
            Wir nehmen den Schutz Ihrer persönlichen Daten sehr ernst. Wir behandeln 
            Ihre personenbezogenen Daten vertraulich und entsprechend der gesetzlichen 
            Datenschutzvorschriften sowie dieser Datenschutzerklärung.
        </p>

        <h3>Hinweis zur verantwortlichen Stelle</h3>
        <p>
            Die verantwortliche Stelle für die Datenverarbeitung auf dieser Website ist:<br><br>
            [FIRMENNAME]<br>
            [STRASSE UND HAUSNUMMER]<br>
            [PLZ] Berlin<br>
            Telefon: [TELEFON]<br>
            E-Mail: [E-MAIL]
        </p>

        <h2>4. Datenerfassung auf dieser Website</h2>
        
        <h3>Server-Log-Dateien</h3>
        <p>
            Der Provider der Seiten (GitHub Pages) erhebt und speichert automatisch 
            Informationen in so genannten Server-Log-Dateien, die Ihr Browser automatisch 
            an uns übermittelt. Dies sind:
        </p>
        <ul>
            <li>Browsertyp und Browserversion</li>
            <li>Verwendetes Betriebssystem</li>
            <li>Referrer URL</li>
            <li>Hostname des zugreifenden Rechners</li>
            <li>Uhrzeit der Serveranfrage</li>
            <li>IP-Adresse</li>
        </ul>
        <p>
            Eine Zusammenführung dieser Daten mit anderen Datenquellen wird nicht vorgenommen.
        </p>

        <h2>5. Ihre Rechte</h2>
        <p>Sie haben folgende Rechte:</p>
        <ul>
            <li>Recht auf Auskunft über Ihre gespeicherten Daten</li>
            <li>Recht auf Berichtigung unrichtiger Daten</li>
            <li>Recht auf Löschung Ihrer Daten</li>
            <li>Recht auf Einschränkung der Datenverarbeitung</li>
            <li>Recht auf Datenübertragbarkeit</li>
            <li>Widerspruchsrecht gegen die Datenverarbeitung</li>
            <li>Beschwerderecht bei einer Aufsichtsbehörde</li>
        </ul>

        <h2>6. Kontakt</h2>
        <p>
            Bei Fragen zum Datenschutz wenden Sie sich bitte an:<br>
            E-Mail: [DATENSCHUTZ@VDT-BERLIN.DE]
        </p>

        <p><em>Stand: Oktober 2025</em></p>

        <p><a href="index.html">← Zurück zur Startseite</a></p>
    </main>

    <footer>
        <img src="images/foot1.jpg" alt="VDT Berlin Footer" class="footer-image">
        <nav class="footer-nav">
            <a href="impressum.html">Impressum</a> | 
            <a href="datenschutz.html">Datenschutz</a>
        </nav>
    </footer>
</body>
</html>
```

---

## GitHub Pages Deployment Steps

### 1. Create GitHub Repository
```bash
# On your local machine
mkdir vdt-berlin
cd vdt-berlin

# Copy all files (HTML, CSS, images, PDFs)
# Then initialize git
git init
git add .
git commit -m "Initial commit - VDT Berlin website"
```

### 2. Push to GitHub
```bash
# Create repository on GitHub: vdt-berlin
git remote add origin https://github.com/[USERNAME]/vdt-berlin.git
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages
1. Go to repository Settings
2. Navigate to "Pages" section
3. Source: Deploy from branch "main"
4. Folder: / (root)
5. Click Save

**Your site will be live at:**
`https://[USERNAME].github.io/vdt-berlin/`

### 4. Custom Domain (Optional)
If you want to keep `www.vdt-berlin.de`:

1. Add file `CNAME` in repository root:
```
www.vdt-berlin.de
```

2. Configure DNS at domain registrar:
```
Type: CNAME
Name: www
Value: [USERNAME].github.io
```

3. Enable "Enforce HTTPS" in GitHub Pages settings

**SSL is automatic and free with GitHub Pages!**

---

## Cost Breakdown

| Item | Cost |
|------|------|
| GitHub Pages Hosting | **€0** (free) |
| SSL Certificate | **€0** (included) |
| Development Time (4-8 hours) | €0 - €400 |
| Domain (if needed) | €10/year |
| **TOTAL** | **€0 - €410** |

---

## Timeline

- **Day 1**: Convert HTML, create CSS (2-3 hours)
- **Day 2**: Create Impressum & Datenschutz pages (1-2 hours)
- **Day 3**: Test on mobile devices (1 hour)
- **Day 4**: Deploy to GitHub Pages (30 minutes)
- **Day 5**: Configure custom domain (if needed) (30 minutes)

**Total: 1 week maximum**

---

## What You Get

✅ **SSL/HTTPS** - Automatic with GitHub Pages  
✅ **Responsive Design** - Works on all devices  
✅ **Legal Compliance** - Impressum & Datenschutz  
✅ **Same Content** - All existing PDFs and links preserved  
✅ **Fast Loading** - GitHub's CDN worldwide  
✅ **Free Hosting** - No monthly costs  
✅ **Easy Updates** - Edit files and push to GitHub  

---

## Maintenance

**To update content:**
```bash
# Edit files locally
git add .
git commit -m "Update content"
git push

# Changes live in 1-2 minutes!
```

---

## Next Steps

1. ✅ I can create the complete code files for you
2. ✅ You copy existing images and PDFs
3. ✅ Fill in placeholders in Impressum/Datenschutz
4. ✅ Create GitHub account (if needed)
5. ✅ Deploy in 30 minutes

**Want me to create the complete file structure ready to deploy?**
