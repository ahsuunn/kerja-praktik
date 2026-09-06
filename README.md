# Laporan Kerja Praktik (LaTeX Template)

Repository ini berisi templat dan naskah LaTeX untuk **Laporan Kerja Praktik (KP)**. Dokumen disesuaikan dengan format standar laporan akademik/instansi (ukuran kertas A4, margin 4-3-3-3, penomoran Romawi/Arabik, dan bahasa Indonesia).

---

## 📁 Struktur Direktori

```text
kerja-praktik/
├── main.tex                    # Berkas utama LaTeX (Root Document)
├── main.pdf                    # Berkas PDF hasil kompilasi
├── README.md                   # Panduan penggunaan proyek
├── frontmatter/                # Halaman depan (Cover, Pengesahan, Abstrak, Kata Pengantar)
│   ├── Cover.tex
│   ├── Lembar_Pengesahan_Dosen.tex
│   ├── Lembar_Pengesahan_Perusahaan.tex
│   ├── Abstrak.tex
│   ├── Kata_Pengantar.tex
│   ├── Daftar_Istilah.tex
│   └── Daftar_Lampiran.tex
├── chapters/                   # Bab utama laporan
│   ├── BabI_Pendahuluan.tex
│   ├── BabII_Organisasi_dan_LKP.tex
│   ├── BabIII_Judul_Pekerjaan.tex
│   └── BabIV_Rangkuman.tex
├── backmatter/                 # Daftar pustaka / referensi
│   └── Referensi.tex
├── appendices/                 # Lampiran (misal: TOR / Terms of Reference)
│   └── TOR.tex
├── figures/                    # Gambar dan diagram
├── context/                    # Catatan/konteks proyek (opsional untuk AI assistant)
└── .zed/                       # Konfigurasi tugas otomatis untuk editor Zed
    └── task.json
```

---

## 🛠️ Prasyarat (Prerequisites)

Pastikan sistem Anda telah terpasang paket TeX Live dan alat bantu berikut:

### Arch Linux / Manjaro
```bash
sudo pacman -S texlive-meta texlive-latexextra texlive-fontsrecommended zathura zathura-pdf-mupdf
```

### Ubuntu / Debian
```bash
sudo apt update
sudo apt install texlive-latex-extra texlive-fonts-recommended latexmk zathura
```

---

## 🚀 Cara Menjalankan & Kompilasi (How to Run)

### 1. Kompilasi Sekali (Single Build)
Untuk mengompilasi naskah menjadi `main.pdf`:

```bash
latexmk -pdf -interaction=nonstopmode main.tex
```

### 2. Mode Live Preview / Watch (Rekomendasi saat Menulis)
Untuk memantau perubahan berkas secara otomatis setiap kali disimpan:

```bash
latexmk -pvc -pdf -synctex=1 -interaction=nonstopmode main.tex
```

### 3. Membuka PDF Previewer (Zathura)
Di terminal terpisah, jalankan `zathura` di latar belakang:

```bash
zathura main.pdf &
```
> **Catatan:** `zathura` akan memperbarui tampilan secara otomatis (*auto-refresh*) setiap kali `latexmk` memperbarui `main.pdf`.

### 4. Membersihkan Berkas Aux (Clean Build Files)
Untuk menghapus berkas sementara (`.aux`, `.log`, `.fls`, `.toc`, dll.):

```bash
latexmk -c
```

---

## ⚡ Penggunaan di Zed Editor

Repository ini sudah dilengkapi dengan berkas tugas di `.zed/task.json`. Di dalam **Zed Editor**, Anda dapat menekan `Ctrl+Shift+P` (atau `Cmd+Shift+P`), mengetik `task: spawn`, lalu memilih salah satu opsi:

* **`LaTeX: Build Document`**: Mengompilasi `main.tex` sekali.
* **`LaTeX: Watch & Live Preview`**: Mengaktifkan mode `-pvc` auto-compile saat berkas disimpan.
* **`LaTeX: Clean Auxiliary Files`**: Membersihkan berkas pembantu kompilasi.

---

## 📝 Mengisi Data Laporan

Identitas laporan (Judul, Nama Mahasiswa, NIM, Dosen Pembimbing, Pembimbing Perusahaan) dapat diubah langsung pada berkas **[`main.tex`](file:///home/malik/Work/kerja-praktik/main.tex)** di bagian **Metadata laporan** (baris 30–46).
