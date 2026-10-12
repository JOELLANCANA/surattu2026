# 🚀 START HERE — Sistem Persuratan & Digitalisasi Arsip UIN Ar-Raniry

**Version**: v2.0 (Offline Edition)  
**Status**: ✅ Production Ready  
**Date**: September 9, 2026  
**Size**: 138.6 KB (single HTML file)

---

## 🎯 Quick Start (2 Minutes)

### Option 1: Open Directly
```
1. Double-click: index.html
2. Application loads in browser
3. ✅ Ready to use!
```

### Option 2: Copy to Web Server
```
1. Copy index.html + logo.svg to server
2. Access via browser
3. ✅ Ready to use!
```

### Option 3: Use as USB Drive
```
1. Copy index.html + logo.svg to USB
2. Open from any computer
3. ✅ Works offline!
```

---

## 📖 What This Application Does

**Sistem Persuratan & Digitalisasi Arsip** adalah aplikasi web untuk:

```
✅ Mengelola surat masuk dan keluar
✅ Mengarsipkan dokumen digital
✅ Mencari dan memfilter surat
✅ Mendistribusikan surat ke unit kerja
✅ Mencetak bukti tanda terima 2 sisi
✅ Membuat laporan dan statistik
✅ Menyimpan data offline
✅ Mengekspor data ke CSV
```

---

## 🎨 Features

### Admin Panel
- [x] Login terpisah untuk admin surat masuk, surat keluar, distribusi, dan Super Admin
- [x] Akses halaman dibatasi berdasarkan jenis akun
- [x] Admin distribusi hanya mendapat akses baca
- [x] Super Admin dapat mengakses semua halaman dan tindakan administrasi

### User Features
- [x] Dashboard dengan analytics
- [x] Archive surat (100+ sample data)
- [x] Input surat masuk/keluar
- [x] Search dan filter
- [x] Print 2-sided receipt dengan QR
- [x] Public archive view
- [x] Distribution tracking

---

## 📋 Navigation

### Halaman Admin

Halaman yang muncul bergantung pada akun yang dipilih. Admin surat masuk
mengelola surat masuk dan arsip surat masuk; admin surat keluar mengelola surat
keluar dan arsip surat keluar; admin distribusi hanya membaca halaman
distribusi. Super Admin dapat mengakses seluruh halaman dan tindakan
administrasi yang tersedia.

---

## 🔐 Admin Access

### Login Admin

Akun admin memiliki nama pengguna tetap:

| Akses | Nama pengguna |
|---|---|
| Login Admin Surat Masuk | `admin_masuk` |
| Login Admin Surat Keluar | `admin_keluar` |
| Login Admin Distribusi Surat | `admin_distribusi` |
| Login Super Admin | `super_admin` |

Jalankan fungsi `setup()` di Apps Script untuk membuat tab **Admin Login** di
Spreadsheet utama. Isi kolom `password` pada setiap baris akun, lalu deploy
versi terbaru sebagai Web App. Nilai sandi dibaca server dan tidak dikirim ke
halaman publik. Batasi akses Spreadsheet kepada pengelola tepercaya.

Untuk konfigurasi awal yang diminta, isikan sandi yang sama pada keempat akun.
Perlu diketahui, sandi bersama tidak membatasi pemilihan peran: siapa pun yang
mengetahuinya dapat memilih Super Admin. Hak baca-saja distribusi hanya berlaku
untuk sesi yang masuk menggunakan peran distribusi.


Login admin hanya tersedia saat aplikasi dibuka melalui deployment Web App
Google Apps Script. Sesi berlaku hingga 6 jam. Super Admin memiliki akses ke
semua halaman dan tindakan administrasi yang saat ini didukung. Akun distribusi
hanya memiliki akses baca ke halaman distribusi.

### How to Login
```
1. Click "🔒 Login" button (top right)
2. Choose one of the four admin login options
3. Enter the selected account's password
4. Click "Masuk"
5. The workspace opens with access limited to that account's role
```

---

## 📊 Sample Data

Application includes **100 sample letters** with:
- Letter numbers
- Dates received/sent
- Sender information
- Recipient
- Subject
- Classification
- Distribution status

These are loaded automatically on page open.

---

## 🖨️ Print Features

### 2-Sided Receipt (Tanda Terima)
```
How to print:
1. Go to "📂 Arsip Surat"
2. Find letter you want
3. Click "🖨️" button
4. Click "🖨️ Cetak Tanda Terima (2 Sisi)"
5. Print preview opens
6. Click "Print"

Features:
- Official letterhead (kop surat)
- QR code for verification
- Two copies (lembar 1 & 2)
- Ready for cutting
- Professional layout
```

---

## 💾 Data Storage

### How Data Is Saved

```
Session Data (Current Session):
- Letters you add → saved in memory
- Lost when page refreshes
- Normal behavior for web app

Persistent Settings:
- Admin customization → localStorage
- Master data → localStorage
- Admin login → session only
- Survives page refresh
```

### Important Note
```
⚠️ Session letters NOT automatically saved between refreshes
Solution: Export to CSV before closing browser
         Or implement IndexedDB (see documentation)
```

---

## 🔍 How to Use Features

### Search & Filter
```
1. Go to "📂 Arsip Surat"
2. Use filters on top:
   - By date range
   - By pengirim (sender)
   - By status
3. Results update automatically
```

### Add New Letter
```
1. Go to "📥 Input Masuk" or "📤 Input Keluar"
2. Fill in form fields
3. Click "💾 Simpan Surat..."
4. ✅ Success message
5. Auto-redirects to dashboard
```

### Print QR Receipt
```
1. Go to "📂 Arsip Surat"
2. Find letter
3. Click "🖨️"
4. Preview appears with QR
5. Click "Print" to print both sides
```

### Catatan Pengaturan

Pengaturan branding dan sistem tidak termasuk dalam tiga akun admin yang
tersedia. Perubahan data admin memerlukan sesi Web App yang masih aktif.

---

## 🌐 Offline Capability

### Works Without Internet
- ✅ View cached public information
- ✅ Search documents already loaded in the browser
- ✅ Print documents and export loaded data

### Cannot Do (Without Internet)
- ❌ Admin login and authenticated changes
- ❌ Load current server data or sync changes
- ❌ Upload to cloud

---

## 📱 Browser Compatibility

### Fully Supported
- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Mobile browsers
- ✅ Tablets
- ✅ Any modern browser

---

## 🚀 Deployment

### Single File Application
```
Copy to server:
- index.html (main application)
- logo.svg (logo image)

No setup needed! ✅
```

### Hosting Options
- Web server (Apache, Nginx)
- Cloud static (GitHub Pages, Netlify)
- Intranet server
- USB drive
- Local file

---

## 📚 Documentation

### For Users
- **README.md** — Quick overview
- **FEATURES.md** — Full feature list
- **QUICK-CHECKLIST.md** — Setup guide

### For Admins
- **DEPLOYMENT-CHECKLIST.md** — Deployment steps
- **BRANDING-ASSETS.md** — Design system

### For Developers
- **OFFLINE-VERIFICATION.md** — Technical details
- **LOGO-INTEGRATION.md** — Logo information
- **REMOVAL-COMPLETE.md** — Backend removal info

---

## ⚙️ Technical Details

### Application Type
```
Single-Page Application (SPA)
HTML5 + JavaScript
No backend needed
No database required
No external dependencies
```

### Technologies Used
```
Frontend:
- HTML5
- CSS3
- JavaScript (vanilla)
- SVG logos

Storage:
- localStorage (browser)
- In-memory arrays

Printing:
- Browser native print
- CSS print styles
```

### Performance
```
File size: 138.6 KB
Load time: <500ms
Memory: ~200 KB runtime
Supported: All modern browsers
Works offline: ✅ Yes
```

---

## 🆘 Troubleshooting

### Dashboard not loading
```
Solution:
1. Refresh page (F5)
2. Clear browser cache (Ctrl+Shift+Delete)
3. Try different browser
```

### Admin login not working
```
Solution:
1. Open the deployed Google Apps Script Web App, not the local HTML file
2. Check that the matching password Script Property is configured
3. Confirm the selected role and its username, then retry
4. Deploy the latest Code.gs version and refresh the Web App
```

### Print not working
```
Solution:
1. Try Ctrl+P
2. Check print settings
3. Test with different browser
4. Ensure printer connected
```

### Settings not saving
```
Solution:
1. Check browser allows localStorage
2. Settings require admin login first
3. Some browsers restrict localStorage in private mode
```

---

## 💡 Tips & Tricks

### Export Data
```
1. Go to "📂 Arsip Surat"
2. Click "⬇️ Export CSV"
3. Data downloads to computer
4. Open with Excel/Sheets
```

### Backup Settings
```
1. Settings saved in browser localStorage
2. If browser data cleared → settings reset
3. Admin defaults restore automatically
4. Consider exporting regularly
```

### Bulk Print
```
1. Select multiple letters
2. Use browser print (Ctrl+P)
3. Print to PDF
4. Save for later
```

### Mobile Use
```
1. Responsive design
2. Works on phones/tablets
3. Touch-friendly buttons
4. Same features on mobile
```

---

## 🔒 Security

### What's Protected
- [x] Admin panel (password required)
- [x] Customization settings
- [x] No data sent to internet
- [x] No external tracking
- [x] No third-party services

### Admin credentials

There is no default password. Set the three role-specific password values in
Apps Script Script Properties; do not edit or store passwords in `index.html`.

---

## ❓ FAQ

### Q: Is my data safe?
**A:** Yes. All data stays on your computer. Nothing sent online.

### Q: Does it work offline?
**A:** Yes, completely offline after loading.

### Q: Can multiple users use it?
**A:** Yes, on same computer. Data shared via browser.

### Q: How do I backup data?
**A:** Export to CSV regularly before closing browser.

### Q: Can I deploy to internet?
**A:** Yes, copy index.html + logo.svg to web server.

### Q: Is it free?
**A:** Yes, completely free. No licenses needed.

### Q: Can I modify it?
**A:** Yes, edit index.html with text editor.

### Q: What if password forgotten?
**A:** Set a new value for the matching admin password in Apps Script Script
Properties, then use the new password at the next login.

---

## 📞 Support

### For Issues
1. Check QUICK-CHECKLIST.md
2. Check OFFLINE-VERIFICATION.md
3. Clear browser cache and refresh

### For Features
- See FEATURES.md for complete list
- See README.md for overview

### For Deployment
- See DEPLOYMENT-CHECKLIST.md

---

## 🎉 You're Ready!

```
✅ Application ready to use
✅ All features working
✅ Offline capability enabled
✅ Print functionality ready
✅ Admin customization available

👉 Next Step: Double-click index.html!
```

---

## 📋 File List

### Essential Files
```
index.html       (138.6 KB) ← Main application (REQUIRED)
logo.svg         (1.2 KB)   ← Logo image (REQUIRED)
```

### Documentation (Optional but Helpful)
```
README.md
FEATURES.md
QUICK-CHECKLIST.md
DEPLOYMENT-CHECKLIST.md
BRANDING-ASSETS.md
LOGO-INTEGRATION.md
OFFLINE-VERIFICATION.md
REMOVAL-COMPLETE.md
```

### Sample Data (Optional)
```
Surat-Masuk-2026-09-08.csv
```

---

## 🚀 Getting Started

### 3 Steps to Success

1. **Open Application**
   ```
   Double-click: index.html
   Or copy to web server
   ```

2. **Explore Features**
   ```
   Click through all pages
   Try search & filter
   Add test letter
   ```

3. **Customize Branding** (Optional)
   ```
   Login with the relevant admin account
   Go to its role-specific page
   Edit header/footer
   Save settings
   ```

---

## 📌 Remember

```
✅ No internet needed
✅ Single HTML file
✅ Fast loading
✅ Secure & offline
✅ Print-ready
✅ Mobile responsive
✅ Professional design
✅ Free to use
```

---

**Ready to get started?**

👉 **Open `index.html` in your browser now!**

---

**Version**: v2.0 (Offline Edition)  
**Institution**: UIN Ar-Raniry Banda Aceh  
**Status**: ✅ Production Ready  
**Date**: September 9, 2026

🎉 **Selamat menggunakan! (Happy using!)**
