# Portofolio

Situs portofolio satu halaman, HTML dan CSS biasa. Tanpa framework, tanpa build
step, tanpa JavaScript.

- `index.html` — seluruh isi
- `style.css` — seluruh tampilan
- `assets/` — tangkapan layar aplikasi, WebP 540 px

Tema gelap sebagai default dan ikut berubah terang bila sistem pengguna memilih
terang. Di layar HP, deretan tangkapan layar digeser mendatar.

Tangkapan layar diambil dari emulator Android, bukan dari HP pribadi. Gambar
dikompres dengan:

```bash
python3 -c "from PIL import Image; im=Image.open('src.png').convert('RGB'); \
im.resize((540, round(im.height*540/im.width))).save('assets/out.webp','WEBP',quality=80)"
```

## Menjalankan lokal

Buka `index.html` langsung di peramban, atau:

```bash
python3 -m http.server 8080
```

Lalu buka <http://localhost:8080>.
