# Portfolio

Situs portfolio satu halaman, HTML dan CSS biasa. Tanpa framework, tanpa build
step, tanpa JavaScript.

- `index.html` — seluruh isi
- `style.css` — seluruh tampilan
- `assets/` — tangkapan layar aplikasi (WebP), ilustrasi, dan font

## Desain

Tata letak, warna, dan ukuran diambil dari file desain FigCraft
(`portfolio-zierch.figcraft`). Palet:

| Token | Nilai |
|---|---|
| Latar | `#000000` |
| Kartu | `#121212` |
| Garis | `#1F1F1F` |
| Teks | `#F3F3F3` / `#949494` |
| Aksen | `#9072D4` |
| Aksen gelap | `#6D46C7` |

Font di-host sendiri, bukan dari CDN:

- **Inter** (variabel 100–900) — teks dan judul
- **Dancing Script 700** — wordmark "zierch"

Keduanya berlisensi SIL Open Font License. Wordmark di desain memakai Segoe
Script, tapi font itu milik Microsoft dan tidak boleh di-embed di web publik,
jadi Dancing Script dipakai sebagai pengganti terdekat.

## Tangkapan layar

Diambil dari emulator Android, bukan dari HP pribadi. Dikompres dengan:

```bash
python3 -c "from PIL import Image; im=Image.open('src.png').convert('RGB'); \
im.resize((540, round(im.height*540/im.width))).save('assets/out.webp','WEBP',quality=80)"
```

Di layar lebar ketiganya tampil berjajar dengan rasio 9:20; di layar sempit
jadi strip geser mendatar.

## Menjalankan lokal

Buka `index.html` langsung di peramban, atau:

```bash
python3 -m http.server 8080
```

Lalu buka <http://localhost:8080>.
