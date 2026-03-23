# Nexorie Bytetown

Landing page SvelteKit untuk presentasi visual Nexorie Bytetown berbasis rangkaian screenshot referensi.

## Stack

- SvelteKit 2
- Svelte 5
- TypeScript
- Vite
- PNPM

## Tujuan Proyek

Repo ini menyusun halaman sebagai showcase visual full-page yang menampilkan beberapa section referensi secara berurutan.

Fokus implementasi saat ini:

- render berurutan beberapa screenshot section
- container visual dengan efek mesh background
- layout responsif sederhana untuk desktop dan mobile

Implementasi utama ada di `src/routes/+page.svelte`.

## Struktur Singkat

```text
src/
  app.html
  routes/
    +layout.ts
    +page.svelte
static/
```

## Menjalankan Project

```bash
pnpm install
pnpm dev
```

## Scripts

```bash
pnpm dev
pnpm build
pnpm preview
pnpm check
```

## Catatan

- Package name: `nexorie-bytetown-landing`
- Halaman saat ini adalah showcase berbasis image reference, bukan implementasi komponen konten granular
- Komponen halaman mengimpor asset screenshot lokal; pastikan file referensi tersedia sesuai path yang digunakan sebelum proses build atau deploy
- Validasi lokal pada checkout sekarang menunjukkan `pnpm check` gagal karena binary `svelte-kit` belum tersedia di environment, jadi dependency perlu di-install atau dipulihkan lebih dulu
