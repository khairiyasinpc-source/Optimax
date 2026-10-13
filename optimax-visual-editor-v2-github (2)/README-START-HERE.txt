OPTIMAX VISUAL EDITOR V2
========================

Ini versi upgrade website OPTIMAX yang sedia ada di GitHub.
JANGAN create repository baru. JANGAN upload ZIP sebagai satu fail.

FAKTA PENTING
- Framework: React + Vite. Hosting preview: GitHub Pages.
- Extra cost: RM0 untuk frontend editor + GitHub Pages biasa.
- Editor URL selepas deployment: https://khairiyasinpc-source.github.io/Optimax/?edit=1
- Website URL: https://khairiyasinpc-source.github.io/Optimax/
- Editor menyimpan draft dalam browser, BUKAN terus publish ke GitHub.

CARA UPDATE REPOSITORY LAMA
1. Extract fail optimax-visual-editor-v2.zip.
2. Repository sedia ada: khairiyasinpc-source/Optimax
3. Kekalkan struktur folder seperti berikut (jangan cipta nested folder kedua):
   Optimax/
     .github/workflows/main.yml   (workflow sedia ada, jangan padam)
     optimax-website/
       index.html
       package.json
       vite.config.js
       public/site-content.json
       src/Editor.jsx
       src/main.jsx
       src/editor.css
       src/style.css
       src/siteDefaults.js
       tests/logic.test.mjs
4. Upload fail baharu ke folder/fail path yang SAMA dalam repository.
   Jika upload beberapa folder sukar melalui GitHub web, GitHub Desktop percuma lebih mudah untuk copy projek ke clone repo dan Commit/Push.
5. Semak Actions -> Deploy OPTIMAX Website -> tunggu tanda hijau.
6. Buka link ?edit=1.

CARA PUBLISH PERUBAHAN DESIGN
1. Buat edit dalam browser melalui ?edit=1.
2. Klik Export for GitHub > Download site-content.json.
3. Dalam repository, ke optimax-website/public/site-content.json.
4. Replace fail dengan JSON baharu di lokasi yang sama dan Commit changes.
5. Tunggu Actions hijau, refresh website public.

Nota:
- User lain yang buka ?edit=1 boleh edit draft browser sendiri, tetapi tidak boleh publish tanpa akses tulis repository.
- Tiada password/admin login dan tiada backend. Jangan masukkan data pesakit.
- Gambar yang diupload masuk ke JSON (WebP yang dikecilkan). Pastikan fail tidak terlalu besar.
- Partner logo, gambar stock, link form dan klaim medikal perlu disemak sebelum laman ini digunakan sebagai website rasmi.
