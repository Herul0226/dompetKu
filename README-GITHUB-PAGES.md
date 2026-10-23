# Deploy DompetKu ke GitHub Pages

## Opsi cepat

Gunakan `dompetku-static.zip` jika repository GitHub Pages menggunakan domain root, misalnya `username.github.io`.

1. Ekstrak `dompetku-static.zip`.
2. Upload isi folder tersebut ke repository.
3. Aktifkan **Settings > Pages > Deploy from a branch**.
4. Pilih branch `main` dan folder `/ (root)`.

## Opsi source

Gunakan `dompetku-source.zip` jika ingin melakukan build melalui GitHub Actions atau mengembangkan aplikasinya.

```bash
pnpm install
pnpm build
```

Hasil deployment berada di folder `dist/`. Untuk repository project page seperti `username.github.io/dompetku`, ubah `base` di `vite.config.ts` menjadi:

```ts
base: '/dompetku/',
```

Ganti `dompetku` dengan nama repository Anda, lalu jalankan ulang `pnpm build`.

Data transaksi disimpan di IndexedDB browser. Data tersebut terikat pada domain/browser dan tidak ikut tersimpan di GitHub. Buat backup JSON melalui menu Pengaturan sebelum mengganti browser atau menghapus data situs.
