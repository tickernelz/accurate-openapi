## Penggunaan API Accurate Online

![API Example](https://accurate.id/wp-content/uploads/2024/02/artificial-intelligence-illustration-04@2x.png)

#### Contoh Langkah Penggunaan API Accurate Online

Setiap HTTP request yang dikirimkan untuk mengakses API Accurate Online (AOL) harus menyertakan HTTP Header (Bearer) yang berisi Access Token yang sudah didapatkan pada tahap sebelumnya. Pada saat melakukan integrasi pertama kali dengan AOL, aplikasi pihak ke-3 harus mengetahui terlebih dahulu akan terhubung dengan database AOL yang mana. Oleh karena itu apabila sudah memperoleh Access Token pertama kali, aplikasi pihak ke-3 harus melakukan 2 tahap berikut ini:

1.  1.  Menampilkan Daftar Database AOL yang dapat diakses oleh Access Token terkait
    2.  Menyimpan informasi Database AOL yang dipilih oleh pengguna (id dan alias database) dan melakukan Open Database untuk mendapatkan informasi host dan session untuk disimpan dan digunakan untuk mengakses data didalam database tersebut

Ke-2 tahap diatas hanya perlu dilakukan 1x saja saat aplikasi pihak ke-3 belum mengetahui akan terhubung ke database AOL yang mana.

Sebagai contoh, berikut adalah informasi aplikasi yang akan digunakan:

**Nama Aplikasi**  
Demo Example  
**Platform**  
Website  
**URL Website**  
https://example.com  
**URL OAuth Callback**  
https://example.com/aol-oauth-callback  
**Client ID**  
42f12a10-08df-4b91-b1e4-c4465d686072  
**Client Secret**  
e133410eb632596255adfbe5a49990fe

Pastikan Anda telah memiliki Akses Token yang bisa didapatkan lewat proses OAuth. Sebagai contoh, berikut adalah Akses Token yang sudah didapatkan:

<table><tbody><tr><td>Pengguna</td><td>john@example.com</td></tr><tr><td>Akses Token</td><td>e8446369-bd56-4731-acea-c0a9e0cc46fa</td></tr><tr><td><strong><a href="https://accurate.id/api-integration/scope">scope</a></strong></td><td>item_view item_save sales_invoice_view</td></tr></tbody></table>

#### Cara membaca dokumentasi Daftar API AOL

Setelah terdaftar sebagai pengembang AOL, Anda dapat melihat daftar dan dokumentasi API AOL di:  
[https://account.accurate.id/developer/api-docs.do](https://account.accurate.id/developer/api-docs.do)

API AOL terbagi menjadi 2 jenis yaitu:

1.  1.  **API Dasar**  
        Berisi API untuk operasi diluar data pengguna, misalnya: melihat daftar database, membuka database, dll
    2.  **API Accurate**  
        Berisi API untuk membaca, menulis, merubah ataupun menghapus data pada database pengguna AOL, misalnya: menambahkan barang/jasa baru, membuat faktur penjualan, dll. Untuk mengakses API Accurate, perlu ditambahkan header **X-Session-ID** yang berisi kode session database yang berhasil didapatkan dari pemanggilan API /api/open-db.do

Pada dokumentasi, Anda dapat mengetahui URL Endpoint untuk mengakses API AOL beserta dengan parameter yang dapat digunakan

###### Cara mengetahui URL Endpoint API AOL

Contoh pada API Dasar berikut ini:

![api-dasar](https://accurate.id/wp-content/uploads/2024/02/api-dasar.png)

Untuk mendapatkan URL API, Anda dapat menggabungkan informasi yang di beri kotak diatas. Misalnya untuk mengakses API Db List (daftar database), berarti URL Endpoint API nya yaitu:  
**https://account.accurate.id/api/db-list.do**

Sekarang kita coba mendapatkan URL Endpoint untuk menyimpan/mengedit data Cabang di database AOL:

![api-accurate](https://accurate.id/wp-content/uploads/2024/02/api-accurate.png)

Dari gambar diatas, kita bisa mendapatkan URL Endpoint untuk API Cabang yaitu:  
**https://xyz.accurate.id/accurate/api/branch/save.do**

Namun untuk jenis API Accurate, prefix URL yang diberi tanda merah diatas perlu diganti dengan response parameter **host** yang didapatkan saat mengakses API Open DB. Contoh apabila response parameter host yang didapat dari API Open DB adalah: https://public.accurate.id, maka URL Endpoint yang digunakan untuk mengakases API Cabang untuk database tersebut adalah:  
**https://public.accurate.id/accurate/api/branch/save.do**

###### Cara mengetahui parameter yang dapat digunakan pada API AOL

Pada dokumentasi Daftar API, dapat dilihat parameter yang dapat digunakan saat mengakses API terkait, lengkap dengan tipe data, contoh dan keterangannya, seperti berikut ini:

![api-branch-param](https://accurate.id/wp-content/uploads/2024/02/api-branch-param.png)

Parameter yang digunakan yaitu HTTP Parameter biasa (disarankan menggunakan HTTP POST method). Kolom Nama Parameter pada dokumentasi merupakan nama HTTP parameter yang dapat digunakan. Untuk mengubah/edit data yang sudah ada di AOL, harus menyertakan parameter id yang berisi **id** record yang ingin dirubah.

Untuk API yang memiliki tipe data yang kompleks, misalnya faktur penjualan, dimana 1 faktur penjualan bisa memiliki beberapa item, pada dokumentasi nama parameter diberi tambahan \[n\] dimana n adalah index angka urut mulai dari 0 (nol). Contoh sbb:

![api-n-detail](https://accurate.id/wp-content/uploads/2024/02/api-n-detail.png)

Misalnya:  
detailItem\[0\].itemNo=ITM0001  
detailItem\[1\].itemNo=ITM0002

#### Mendapatkan daftar database Accurate Online

Untuk mendapatkan daftar database yang dapat dibuka oleh pengguna john@example.com, gunakan API Db List seperti berikut:

<table><tbody><tr><td>URL</td><td>https://account.accurate.id/api/db-list.do</td></tr><tr><td>Method</td><td>HTTP GET</td></tr><tr><td><strong>Header</strong></td><td>&nbsp;</td></tr><tr><td>Authorization</td><td>Bearer e8446369-bd56-4731-acea-c0a9e0cc46fa</td></tr></tbody></table>

Hasil dari request tersebut adalah daftar database seperti berikut:

```

{
  "d": [
    {
      "id": 1156,
      "alias": "PT Demo Example"
    },
    {
      "id": 1253,
      "alias": "PT Contoh"
    }
  ],
  "s": true
}
```

Jika Anda tidak mendapatkan hasil seperti di atas, silakan melihat [halaman Penjelasan Informasi Kesalahan pada API](https://accurate.id/api-integration/error-info/).

#### Mendapatkan session dan host dari Database

Untuk dapat membaca dan menulis ke database diperlukan informasi session dan host untuk database tersebut. Misalkan Anda ingin menggunakan database PT Demo Example maka session dan host dapat didapatkan menggunakan API Open Db dengan mengirimkan id dari database tersebut sebagai parameter sbb:

<table><tbody><tr><td>URL</td><td>https://account.accurate.id/api/open-db.do</td></tr><tr><td>Method</td><td>HTTP GET</td></tr><tr><td><strong>Header</strong></td><td>&nbsp;</td></tr><tr><td>Authorization</td><td>Bearer e8446369-bd56-4731-acea-c0a9e0cc46fa</td></tr><tr><td><strong>Request Parameter</strong></td><td>&nbsp;</td></tr><tr><td>id<strong><br></strong></td><td>1156</td></tr></tbody></table>

Hasil dari request tersebut adalah sebagai berikut:

```

{
  "d": [
    "Proses Berhasil Dilakukan"
  ],
  "host": "https://public.accurate.id",
  "session": "7ff842b6-53e2-4d7b-8038-09e3f8318f1b",
  "s": true
}
```

Dari hasil berikut didapatkan session **7ff842b6-53e2-4d7b-8038- 09e3f8318f1b** dan host **https://public.accurate.id** yang dapat digunakan untuk mengakses data pada database terkait sesuai dengan scope yang diminta. Informasi host ini akan menentukan prefix URL untuk mengakses API Accurate

#### Menulis data kedalam Database AOL

Berikutnya kita sudah dapat menulis ke database. Misalkan kita ingin menyimpan data barang baru, maka kita bisa lihat dari Daftar API, dan maka bisa menggunakan API /api/item seperti berikut:

<table><tbody><tr><td>URL</td><td>https://public.accurate.id/accurate/api/item/save.do</td></tr><tr><td>Method</td><td><a href="https://accurate.id/api-integration/http-post-method">HTTP POST</a></td></tr><tr><td><strong>Header</strong></td><td>&nbsp;</td></tr><tr><td>Authorization</td><td>Bearer e8446369-bd56-4731-acea-c0a9e0cc46fa</td></tr><tr><td>X-Session-ID</td><td>7ff842b6-53e2-4d7b-8038-09e3f8318f1b</td></tr><tr><td><strong>Request Body</strong></td><td>&nbsp;</td></tr><tr><td>name</td><td>Test Item</td></tr><tr><td>itemType</td><td>INVENTORY</td></tr></tbody></table>

Hasil dari request tersebut adalah sebagai berikut:

```

{
  "r": {
    "id": 1250,
    "no": "100027",
    "name": "Test Item",
    "upcNo": null,
    "itemType": "INVENTORY",
    "notes": null,
    "detailOpenBalance": [],
     ....
  },
  "s": true,
  "d": [
    "Barang & Jasa "Test Item" berhasil disimpan"
  ]
}
```

#### Membaca daftar data dari Database

Untuk melihat daftar barang yang ada, bisa menggunakan API /item/list seperti berikut:

<table><tbody><tr><td>URL</td><td>https://public.accurate.id/accurate/api/item/list.do</td></tr><tr><td>Method</td><td>HTTP GET</td></tr><tr><td><strong>Header</strong></td><td>&nbsp;</td></tr><tr><td>Authorization</td><td>Bearer e8446369-bd56-4731-acea-c0a9e0cc46fa</td></tr><tr><td>X-Session-ID</td><td>7ff842b6-53e2-4d7b-8038-09e3f8318f1b</td></tr><tr><td><strong>Request Parameter</strong></td><td>&nbsp;</td></tr><tr><td>fields</td><td>id,name,no</td></tr><tr><td>filter.itemType</td><td>INVENTORY</td></tr></tbody></table>

Hasil dari request tersebut adalah sebagai berikut :

```

{
  "s": true,
  "d": [
    {
      "no": "100027",
      "name": "Test Item",
      "id": 1250
    },
    {
      "no": "100016",
      "name": "Chipset 6293LW",
      "id": 984
    },
    {
      "no": "100012",
      "name": "289TD Docking Station 43 mm",
      "id": 728
    }
    ...
  ],
  "sp": {
    "page": 1,
    "sort": null,
    "pageSize": 20,
    "pageCount": 2,
    "rowCount": 22,
    "start": 0,
    "limit": null
  }
}
```

#### Membaca rincian data dari Database

Untuk mendapatkan data barang yang lebih rinci bisa menggunakan API /item/detail seperti berikut:

<table><tbody><tr><td>URL</td><td>https://public.accurate.id/accurate/api/item/detail.do</td></tr><tr><td>Method</td><td>HTTP GET</td></tr><tr><td><strong>Header</strong></td><td>&nbsp;</td></tr><tr><td>Authorization</td><td>Bearer e8446369-bd56-4731-acea-c0a9e0cc46fa</td></tr><tr><td>X-Session-ID</td><td>7ff842b6-53e2-4d7b-8038-09e3f8318f1b</td></tr><tr><td><strong>Request Parameter</strong></td><td>&nbsp;</td></tr><tr><td>id</td><td>1250</td></tr></tbody></table>

Hasil dari request tersebut adalah informasi data barang yang rinci seperti berikut:

```

{
  "s": true,
  "d": {
    "id": 1250,
    "no": "100027",
    "name": "Test Item",
    "upcNo": null,
    "itemType": "INVENTORY",
    "notes": null,
    "detailOpenBalance": [],
     ....
  }
}
```

Daftar API yang dapat digunakan dapat dilhat pada halaman developer [https://account.accurate.id/developer](https://account.accurate.id/developer) pada bagian [Daftar API](https://account.accurate.id/developer/api-docs.do). Anda juga dapat mencoba mencoba Public API Accurate Online secara interaktif tanpa harus membuat code terlebih dahulu melalui Swagger Hub berikut ini:

[https://app.swaggerhub.com/apis/cpssoft/accurate-online\_public\_api/](https://app.swaggerhub.com/apis/cpssoft/accurate-online_public_api/)

Jika Anda mengalami kendala dalam penggunaan silakan lihat halaman [Penjelasan Informasi Kesalahan pada API](https://accurate.id/api-integration/error-info).