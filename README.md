# Accurate OpenAPI

Dokumentasi dan spesifikasi OpenAPI untuk integrasi dengan Accurate Cloud API.

## Struktur Project

- `openapi.yaml`  
  Spesifikasi utama OpenAPI dalam format YAML.
- `openapi.json`  
  Spesifikasi utama OpenAPI dalam format JSON.
- `llms.txt`  
  Dokumentasi tambahan, contoh penggunaan, dan penjelasan parameter API.

## Fitur

- Mendukung berbagai endpoint Accurate Cloud API, seperti:
  - Manajemen Proyek (`/api/project`)
  - Manajemen Cabang (`/api/branch`)
  - Manajemen Vendor, Customer, Barang, dan lainnya
- Spesifikasi lengkap untuk request, response, parameter, dan security scopes.
- Contoh penggunaan dan penjelasan parameter dalam Bahasa Indonesia.

## Cara Menggunakan

1. **Lihat Spesifikasi API**
   - Buka file [`openapi.yaml`](openapi.yaml) atau [`openapi.json`](openapi.json) menggunakan editor atau tool visualisasi OpenAPI (misal: [Swagger Editor](https://editor.swagger.io/)).
2. **Baca Dokumentasi**
   - Lihat file [`llms.txt`](llms.txt) untuk penjelasan tambahan, contoh request/response, dan deskripsi parameter.
3. **Integrasi**
   - Gunakan spesifikasi ini untuk membangun integrasi dengan Accurate Cloud API menggunakan bahasa pemrograman atau tools pilihan Anda.

## Tools yang Direkomendasikan

- [Swagger Editor](https://editor.swagger.io/)  
  Untuk melihat dan menguji spesifikasi OpenAPI.
- [Postman](https://www.postman.com/)  
  Untuk mencoba request ke endpoint API.

## Catatan

- Pastikan Anda memiliki akses dan kredensial ke Accurate Cloud API.
- Beberapa endpoint membutuhkan header `X-Session-ID` yang didapat dari endpoint `/api/open-db.do`.
- Contoh nilai parameter dapat dilihat pada bagian `Cth:` di setiap deskripsi field.

## Kontribusi

Silakan buat pull request atau issue jika menemukan kekurangan atau ingin menambahkan dokumentasi.

---

**Hak Cipta © Accurate OpenAPI**