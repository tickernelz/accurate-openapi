# Accurate Online Public API

Public API Accurate Online. For further information visit: https:/accurate.id/api-integration

## 🌍 Base URL


| URL | Description |
|-----|-------------|
| https://account.accurate.id | API Dasar |
| https://{cloudServerCode}.accurate.id/accurate | API Accurate |


## 🔐 Authentication



## Security Schemes

| Name              | Type              | Description              | Scheme              | Bearer Format             |
|-------------------|-------------------|--------------------------|---------------------|---------------------------|
| default | oauth2 |  |  |  |

# 🛠️ APIs

## GET `/api/approved-scope.do`

> **/api/approved-scope.do**

Daftar scope OAuth2 yang telah disetujui oleh pengguna untuk token yang sedang digunakan





### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/auth-info.do`

> **/api/auth-info.do**

Informasi pengguna dari token yang sedang digunakan





### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/db-check-session.do`

> **/api/db-check-session.do**

Memeriksa apakah Data Usaha session masih dapat digunakan



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| session | string | True | Data Usaha session yang didapatkan dari hasil API /open-db.do 

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/db-detail.do`

> **/api/db-detail.do**

Detil informasi database



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| id | integer | True | ID data usaha yang ingin diakses

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/db-list.do`

> **/api/db-list.do**

Daftar data usaha yang dapat diakses





### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/db-refresh-session.do`

> **/api/db-refresh-session.do**

Memeriksa dan mengganti Data Usaha session jika sudah tidak dapat digunakan



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| id | integer | True | db_id_desc

Cth: 1, 2, 3 (Angka non desimal) |
| session | string | True | Data Usaha session yang didapatkan dari hasil API /open-db.do 

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/db-status.do`

> **/api/db-status.do**

Memeriksa status database



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| id | integer | True | ID data usaha yang ingin diakses

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/open-db.do`

> **/api/open-db.do**

Mengakses database



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| id | integer | True | ID data usaha yang ingin diakses

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/userinfo.do`

> **/api/userinfo.do**

Informasi OAuth2 Claim dari pengguna yang digunakan





### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/webhook-history.do`

> **/api/webhook-history.do**

Menampilkan daftar data pengiriman webhook yang sudah terjadi dalam 1 bulan terakhir dan API ini hanya dapat diakses oleh token dari pengguna yang merupakan developer dari aplikasi



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| from | string | True | Filter tanggal mulai createDate dengan format dd/MM/yyyy HH:mm:ss

Cth: Halo Semua 123 |
| to | string | True | Filter tanggal akhir createDate dengan format dd/MM/yyyy HH:mm:ss (rentang maksimal from-to adalah 24 jam)

Cth: Halo Semua 123 |
| databaseId | integer | False | Filter data yang ingin ditampilkan berdasarkan nilai ID data usaha

Cth: 1, 2, 3 (Angka non desimal) |
| type | string | False | Filter webhook yang ingin ditampilkan berdasarkan tipe webhook, yaitu: ITEM_QUANTITY, SALES_INVOICE_OWING, ITEM, SALES_ORDER, CUSTOMER, STOCK_MUTATION, GLACCOUNT, SALES_QUOTATION, DELIVERY_ORDER, SALES_INVOICE, SALES_RETURN, SALES_RECEIPT, ITEM_ADJUSTMENT, JOB_ORDER, ROLL_OVER, MATERIAL_ADJUSTMENT, WAREHOUSE, ITEM_TRANSFER, PURCHASE_ORDER, PURCHASE_REQUISITION, PURCHASE_INVOICE, PURCHASE_RETURN, RECEIVE_ITEM, PURCHASE_PAYMENT

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/webhook-renew.do`

> **/api/webhook-renew.do**

Memperpanjang lama aktif webhook





### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/access-privilege/detail.do`

> **/api/access-privilege/detail.do**

Melihat detil data Akses Grup berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/access-privilege/list.do`

> **/api/access-privilege/list.do**

Melihat daftar data Akses Grup, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/auto-number/list.do`

> **/api/auto-number/list.do**

Melihat daftar data Penomoran, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.transactionType.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transactionType.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/bank-transfer/bulk-save.do`

> **/api/bank-transfer/bulk-save.do**

Membuat mengedit beberapa data Transfer Bank sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/bank-transfer/delete.do`

> **/api/bank-transfer/delete.do**

Menghapus data Transfer Bank berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/bank-transfer/detail.do`

> **/api/bank-transfer/detail.do**

Melihat detil data Transfer Bank berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/bank-transfer/list.do`

> **/api/bank-transfer/list.do**

Melihat daftar data Transfer Bank, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/bank-transfer/save.do`

> **/api/bank-transfer/save.do**

Membuat data Transfer Bank baru atau mengedit data Transfer Bank yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| fromBankAmount | number | Jumlah nilai transaksi transfer terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| fromBankNo | string | Nomor akun perkiraan bank yang menjadi sumber untuk transaksi transfer terkait

Cth: Halo Semua 123 |
| toBankNo | string | Nomor akun perkiraan bank yang menjadi tujuan untuk transaksi transfer terkait

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailBankTransfer | array |  |
| differenceAccountNo | string | Nomor akun perkiraan bank yang digunakan untuk mencatat selisih nilai tukar mata uang (jika mata uang sumber dan tujuan berbeda)

Cth: Halo Semua 123 |
| fromBankRate | number | Nilai tukar mata uang untuk bank sumber (jika mata uang bank sumber berbeda dengan mata uang default yang digunakan di database)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| toBankRate | number | Nilai tukar mata uang untuk bank tujuan (jika mata uang bank tujuan berbeda dengan mata uang default yang digunakan di database)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/branch/bulk-save.do`

> **/api/branch/bulk-save.do**

Membuat mengedit beberapa data Cabang sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/branch/delete.do`

> **/api/branch/delete.do**

Menghapus data Cabang berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | False | Menghapus daftar data sesuai dengan Nama Cabang (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/branch/detail.do`

> **/api/branch/detail.do**

Melihat detil data Cabang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | False | Melihat daftar data sesuai dengan Nama Cabang (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/branch/list.do`

> **/api/branch/list.do**

Melihat daftar data Cabang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.suspended | boolean | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/branch/save.do`

> **/api/branch/save.do**

Membuat data Cabang baru atau mengedit data Cabang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Cabang

Cth: Halo Semua 123 |
| city | string | Kota

Cth: Halo Semua 123 |
| country | string | Negara

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| province | string | Provinsi

Cth: Halo Semua 123 |
| street | string | Jalan

Cth: Halo Semua 123 |
| zipCode | string | K.Pos

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/currency/bulk-save.do`

> **/api/currency/bulk-save.do**

Membuat mengedit beberapa data Mata Uang sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/currency/detail.do`

> **/api/currency/detail.do**

Melihat detil data Mata Uang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/currency/exchange-rate.do`

> **/api/currency/exchange-rate.do**

Melihat detil data Histori Kurs mata uang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| code | string | True | Kode

Cth: Halo Semua 123 |
| id | integer | False | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/currency/fiscal-rate.do`

> **/api/currency/fiscal-rate.do**

Melihat detil data Histori Kurs Pajak mata uang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| code | string | True | Kode

Cth: Halo Semua 123 |
| id | integer | False | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/currency/list.do`

> **/api/currency/list.do**

Melihat daftar data Mata Uang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/currency/save.do`

> **/api/currency/save.do**

Membuat data Mata Uang baru atau mengedit data Mata Uang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| code | string | Kode

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/customer/bulk-save.do`

> **/api/customer/bulk-save.do**

Membuat mengedit beberapa data Pelanggan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/customer/delete.do`

> **/api/customer/delete.do**

Melihat detil data Pelanggan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| customerNo | string | False | Menghapus daftar data sesuai dengan Nomor Identitas Pelanggan (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/customer/detail.do`

> **/api/customer/detail.do**

Melihat detil data Pelanggan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| customerNo | string | False | Melihat detil daftar sesuai dengan Nomor Identitas Pelanggan (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/customer/list.do`

> **/api/customer/list.do**

Melihat daftar data Pelanggan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.customerCategoryId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.customerCategoryId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.no.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.no.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.npwpNo.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.npwpNo.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.suspended | boolean | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| npwpNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor NPWP pelanggan

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| suspendedFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true, false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/customer/save.do`

> **/api/customer/save.do**

Membuat data Pelanggan baru atau mengedit data Pelanggan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama entitas. Cth: PT. XYZ, John Doe, dll)

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| billCity | string | Nama kota alamat penagihan

Cth: Halo Semua 123 |
| billCountry | string | Nama negara alamat pengiriman

Cth: Halo Semua 123 |
| billProvince | string | Nama provinsi alamat penagihan

Cth: Halo Semua 123 |
| billStreet | string | Nama jalan alamat penagihan

Cth: Halo Semua 123 |
| billZipCode | string | Kode pos alamat penagihan

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| categoryName | string | Nama record kategori pelanggan. Cth: Grosir, Ritel, dll

Cth: Halo Semua 123 |
| consignmentStore | boolean | Apakah perusahaan menitipkan barang untuk dijual (konsinyasi) kepada pelanggan terkait

Cth: true / false |
| currencyCode | string | Kode record mata uang default yang ingin digunakan pada saat bertransaksi dengan perusahaan terkait (Cth: IDR, USD, dll)

Cth: Halo Semua 123 |
| customerDownPaymentAccountListNo | array | Kode Akun Uang Muka

Cth: Halo Semua 123 |
| customerLimitAge | boolean | Apakah ingin membatasi umur piutang maksimum yang diperbolehkan untuk pelanggan terkait. Nilai umur piutang maksimum ditentukan pada field: customerLimitAgeValue

Cth: true / false |
| customerLimitAgeValue | integer | Jumlah hari maksimum umur piutang yang diperbolehkan untuk pelanggan terkait

Cth: 1, 2, 3 (Angka non desimal) |
| customerLimitAmount | boolean | Apakah ingin membatasi maksimum total piutang yang diperbolehkan untuk pelanggan terkait. Nilai jumlah piutang maksimum ditentukan pada field:customerLimitAmountValue

Cth: true / false |
| customerLimitAmountValue | number | Jumlah maksimum total piutang (dalam satuan mata uang default perusahaan) yang diperbolehkan untuk pelanggan terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| customerReceivableAccountListNo | array | Kode Akun Piutang

Cth: Halo Semua 123 |
| customerTaxType | string |  |
| defaultIncTax | boolean | Apakah secara default transaksi dengan perushaan terkait akan dikenakan pajak

Cth: true / false |
| defaultSalesDisc | string | Formula diskon default. Cth: 2+5 (Artinya: diskon 2% + 5%)

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailContact | array |  |
| detailOpenBalance | array |  |
| detailShipAddress | array |  |
| discountCategoryName | string | Nama Kategori Diskon yang ingin digunakan untuk pelanggan. Kategori diskon akan memberikan diskon barang kepada pelanggan 

Cth: Halo Semua 123 |
| email | string | Alamat Email (Cth: johndoe@example.com)

Cth: Halo Semua 123 |
| fax | string | Nomor faximili

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| mobilePhone | string | Nomor handphone

Cth: Halo Semua 123 |
| notes | string | Catatan tambahan untuk data perusahaan terkait

Cth: Halo Semua 123 |
| npwpNo | string | Nomor NPWP (Nomor Pokok Wajib Pajak)

Cth: Halo Semua 123 |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| pkpNo | string | Nomor PKP (Pengusaha Kena Pajak)

Cth: Halo Semua 123 |
| priceCategoryName | string | Nama Kategori Harga yang ingin digunakan untuk pelanggan. Kategori harga akan mempengaruhi harga jual barang kepada pelanggan

Cth: Halo Semua 123 |
| salesmanListNumber | array | Daftar Nomor identitas tenaga penjual yang melayani pelanggan terkait

Cth: Halo Semua 123 |
| salesmanNumber | string | Nomor identitas tenaga penjual yang melayani pelanggan terkait

Cth: Halo Semua 123 |
| shipCity | string | Nama kota alamat pengiriman

Cth: Halo Semua 123 |
| shipCountry | string | Nama negara alamat pengiriman

Cth: Halo Semua 123 |
| shipProvince | string | Nama provinsi alamat pengiriman

Cth: Halo Semua 123 |
| shipSameAsBill | boolean | Apakah alamat pengiriman sama dengan alamat penagihan

Cth: true / false |
| shipStreet | string | Nama jalan alamat pengiriman

Cth: Halo Semua 123 |
| shipZipCode | string | Kode pos alamat pengiriman

Cth: Halo Semua 123 |
| taxCity | string | Nama kota alamat pajak

Cth: Halo Semua 123 |
| taxCountry | string | Nama negara alamat pajak

Cth: Halo Semua 123 |
| taxProvince | string | Nama provinsi alamat pajak

Cth: Halo Semua 123 |
| taxSameAsBill | boolean | Apakah alamat pajak sama dengan alamat penagihan

Cth: true / false |
| taxStreet | string | Nama jalan alamat pajak

Cth: Halo Semua 123 |
| taxZipCode | string | Kode pos alamat pajak

Cth: Halo Semua 123 |
| termName | string | Nama record termin pembayaran default yang ingin digunakan pada saat bertransaksi dengan perusahaan terkait

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| website | string | Alamat Website (Cth: http://cpssoft.com)

Cth: Halo Semua 123 |
| workPhone | string | Nomor telepon kantor

Cth: Halo Semua 123 |
| wpName | string | company.api_wp_name_desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/customer-category/bulk-save.do`

> **/api/customer-category/bulk-save.do**

Membuat mengedit beberapa data Kategori Pelanggan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/customer-category/delete.do`

> **/api/customer-category/delete.do**

Menghapus data Kategori Pelanggan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/customer-category/detail.do`

> **/api/customer-category/detail.do**

Melihat detil data Akun Perkiraan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/customer-category/list.do`

> **/api/customer-category/list.do**

Melihat daftar data Akun Perkiraan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.leafOnly | boolean | False | Filter data agar tidak menampilkan data induk

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| leafOnly | boolean | False | Filter data agar tidak menampilkan Akun Induk

Cth: true / false |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/customer-category/save.do`

> **/api/customer-category/save.do**

Membuat data Kategori Pelanggan baru atau mengedit data Kategori Pelanggan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Kategori Pelanggan

Cth: Halo Semua 123 |
| defaultCategory | boolean | Default Kategori Pelanggan

Cth: true / false |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| parentName | string | Nama Induk Kategori Pelanggan

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/customer-claim/bulk-save.do`

> **/api/customer-claim/bulk-save.do**

Membuat mengedit beberapa data Klaim Pelanggan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/customer-claim/delete.do`

> **/api/customer-claim/delete.do**

Menghapus data Klaim Pelanggan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/customer-claim/detail.do`

> **/api/customer-claim/detail.do**

Melihat detil data Klaim Pelanggan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/customer-claim/list.do`

> **/api/customer-claim/list.do**

Melihat daftar data Klaim Pelanggan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.customerNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pelanggan

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.type | string | False | Filter berdasarkan tipe Klaim Pelanggan. Nilai yang dapat dikirimkan adalah CUSTOMER_CLAIM_OUT atau CUSTOMER_CLAIM_IN |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/customer-claim/save.do`

> **/api/customer-claim/save.do**

Membuat data Klaim Pelanggan baru atau mengedit data Klaim Pelanggan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| customerClaimType | string |  |
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| detailItem | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| fromCustomerClaimNo | string | Nomor Klaim Pelanggan (Terima Barang)

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| saveAsStatusType | string |  |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/data-classification/bulk-save.do`

> **/api/data-classification/bulk-save.do**

Membuat mengedit beberapa data Kategori Keuangan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/data-classification/delete.do`

> **/api/data-classification/delete.do**

Menghapus data Kategori Keuangan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/data-classification/list.do`

> **/api/data-classification/list.do**

Melihat daftar data Kategori Keuangan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| index | string | False | Index Kategori Keuangan, sesuai urutan kategori keuangan yang diset di Menu Preferensi | Atribut Tambahan (Cth: 1 - 10)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/data-classification/save.do`

> **/api/data-classification/save.do**

Membuat data Kategori Keuangan baru atau mengedit data Kategori Keuangan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| index | integer | Index Kategori Keuangan, sesuai urutan kategori keuangan yang diset di Menu Preferensi | Atribut Tambahan (Cth: 1 - 10)

Cth: 1, 2, 3 (Angka non desimal) |
| name | string | Nama Kategori Keuangan

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| suspended | boolean | Kategori Keuangan Non-aktif

Cth: true / false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/delivery-order/bulk-save.do`

> **/api/delivery-order/bulk-save.do**

Membuat mengedit beberapa data Pengiriman Pesanan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/delivery-order/delete.do`

> **/api/delivery-order/delete.do**

Menghapus data Pengiriman Pesanan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/delivery-order/detail.do`

> **/api/delivery-order/detail.do**

Melihat detil data Pengiriman Pesanan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/delivery-order/list.do`

> **/api/delivery-order/list.do**

Melihat daftar data Pengiriman Pesanan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| customerFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pelanggan

Cth: [{"id":50}, {"id":120}] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: Halo Semua 123 |
| filter.customerId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.customerId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerNo | string | False | Filter data yang ingin ditampilkan berdasarkan Pelanggan

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.shipDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.shipDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.shipmentId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.shipmentId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45)

Cth: Halo Semua 123 |
| shipDateFilter | string | False | Filter berdasarkan apakah Tanggal Pengiriman Faktur |
| shipmentFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pengiriman

Cth: [{"id":50}, {"id":120}] |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/delivery-order/save.do`

> **/api/delivery-order/save.do**

Membuat data Pengiriman Pesanan baru atau mengedit data Pengiriman Pesanan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailItem | array |  |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| poNumber | string | Nomor referensi pesanan pembelian yang terkait dengan transaksi pengiriman persanan terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/department/bulk-save.do`

> **/api/department/bulk-save.do**

Membuat mengedit beberapa data Departemen sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/department/delete.do`

> **/api/department/delete.do**

Menghapus data Departemen berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| departmentName | string | False | Menghapus daftar data sesuai dengan Nama Departemen (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/department/detail.do`

> **/api/department/detail.do**

Melihat detil data Departemen berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| departmentName | string | False | Melihat daftar data sesuai dengan Nama Departemen (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/department/list.do`

> **/api/department/list.do**

Melihat daftar data Departemen, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.suspended | boolean | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| suspendedFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true, false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/department/save.do`

> **/api/department/save.do**

Membuat data Departemen baru atau mengedit data Departemen yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| description | string | Keterangan Departemen

Cth: Halo Semua 123 |
| name | string | Nama Departemen

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/employee/delete.do`

> **/api/employee/delete.do**

Menghapus data Karyawan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/employee/detail.do`

> **/api/employee/detail.do**

Melihat detil data Karyawan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/employee/list.do`

> **/api/employee/list.do**

Melihat daftar data Karyawan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.salesman | boolean | False | Filter data berdasarkan status karyawan sebagai Tenaga Penjual

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| salesmanFilter | string | False | Filter data berdasarkan status karyawan sebagai Tenaga Penjual

Cth: true, false |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/employee/save.do`

> **/api/employee/save.do**

Membuat data Karyawan baru atau mengedit data Karyawan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Karyawan

Cth: Halo Semua 123 |
| salutation | string |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| bankAccount | string | No Rekening

Cth: Halo Semua 123 |
| bankAccountName | string | Atas Nama Rekening

Cth: Halo Semua 123 |
| bankCode | string | Kode Bank

Cth: Halo Semua 123 |
| bankName | string | Nama Bank

Cth: Halo Semua 123 |
| bbmPin | string | No. WhatsApp

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| calculatePtkp | boolean | Dikenakan PTKP

Cth: true / false |
| city | string | Nama kota alamat pajak

Cth: Halo Semua 123 |
| country | string | Nama negara alamat pajak

Cth: Halo Semua 123 |
| departmentName | string | Departemen

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| domisiliType | string |  |
| email | string | Alamat Email (Cth: johndoe@example.com)

Cth: Halo Semua 123 |
| employeeTaxStatus | string |  |
| employeeWorkStatus | string |  |
| homePhone | string | Nomor telepon rumah

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| joinDate | string | Tgl Masuk

Cth: 31/03/2016 |
| mobilePhone | string | Nomor handphone

Cth: Halo Semua 123 |
| nettoIncomeBefore | number | Penghasilan Sebelumnya

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| nikNo | string | No. KTP

Cth: Halo Semua 123 |
| notes | string | Catatan

Cth: Halo Semua 123 |
| npwpNo | string | No. NPWP

Cth: Halo Semua 123 |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| position | string | Posisi Jabatan

Cth: Halo Semua 123 |
| pph | boolean | Dikenakan PPh 21

Cth: true / false |
| pphBefore | number | Penghasilan dan PPh sebelumnya HANYA PERLU diisikan jika PPh sudah dihitung dan dibayarkan dari januari, namun Pencatatan gaji di Accurate hanya di isi mulai bulan 

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| province | string | Nama provinsi alamat pajak

Cth: Halo Semua 123 |
| salesman | boolean | Penjual

Cth: true / false |
| startMonthPayment | integer | Bulan Mulai Gajian

Cth: 1, 2, 3 (Angka non desimal) |
| startYearPayment | integer | Tahun Mulai Gajian

Cth: 1, 2, 3 (Angka non desimal) |
| street | string | Nama jalan alamat pajak

Cth: Halo Semua 123 |
| suspended | boolean | Non Aktif

Cth: true / false |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| website | string | Alamat Website (Cth: http://cpssoft.com)

Cth: Halo Semua 123 |
| workPhone | string | Nomor telepon kantor

Cth: Halo Semua 123 |
| zipCode | string | Kode pos alamat pajak

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/exchange-invoice/bulk-save.do`

> **/api/exchange-invoice/bulk-save.do**

Membuat mengedit beberapa data Tukar Faktur sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/exchange-invoice/delete.do`

> **/api/exchange-invoice/delete.do**

Menghapus data Tukar Faktur berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/exchange-invoice/detail.do`

> **/api/exchange-invoice/detail.do**

Melihat detil data Tukar Faktur berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/exchange-invoice/list.do`

> **/api/exchange-invoice/list.do**

Melihat daftar data Tukar Faktur, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/exchange-invoice/save.do`

> **/api/exchange-invoice/save.do**

Membuat data Tukar Faktur baru atau mengedit data Tukar Faktur yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| collectDate | string | Tanggal Proses Tukar

Cth: 31/03/2016 |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| detailInvoice | array |  |
| dueDate | string | Tanggal Jatuh Tempo

Cth: 31/03/2016 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| saveAsStatusType | string |  |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/expense/bulk-save.do`

> **/api/expense/bulk-save.do**

Membuat mengedit beberapa data Pencatatan Beban sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/expense/delete.do`

> **/api/expense/delete.do**

Menghapus data Pencatatan Beban berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/expense/detail.do`

> **/api/expense/detail.do**

Melihat detil data Pencatatan Beban berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/expense/list.do`

> **/api/expense/list.do**

Melihat daftar data Pencatatan Beban, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/expense/save.do`

> **/api/expense/save.do**

Membuat data Pencatatan Beban baru atau mengedit data Pencatatan Beban yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailAccount | array |  |
| dueDate | string | Tanggal jatuh tempo pembayaran beban terkait

Cth: 31/03/2016 |
| expensePayableNo | string | Nomor Akun Perkiraan untuk pencatatan Utang Beban. Diisi dengan Akun tipe Liabilitas Jangka Pendek

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| rate | number | Nilai tukar mata uang yang digunakan pada akun perkiraan dengan mata uang dasar yang digunakan perusahaan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| saveAsStatusType | string |  |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/fixed-asset/delete.do`

> **/api/fixed-asset/delete.do**

Menghapus data Aset Tetap berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/fixed-asset/detail.do`

> **/api/fixed-asset/detail.do**

Melihat detil data Aset Tetap berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/fixed-asset/list.do`

> **/api/fixed-asset/list.do**

Melihat daftar data Aset Tetap, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/fob/bulk-save.do`

> **/api/fob/bulk-save.do**

Membuat mengedit beberapa data FOB sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/fob/delete.do`

> **/api/fob/delete.do**

Menghapus data FOB berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/fob/detail.do`

> **/api/fob/detail.do**

Melihat detil data FOB berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/fob/list.do`

> **/api/fob/list.do**

Melihat daftar data FOB, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/fob/save.do`

> **/api/fob/save.do**

Membuat data FOB baru atau mengedit data FOB yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama FOB

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/freeonboard/bulk-save.do`

> **/api/freeonboard/bulk-save.do**

Membuat mengedit beberapa data FOB sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/freeonboard/delete.do`

> **/api/freeonboard/delete.do**

Menghapus data FOB berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/freeonboard/detail.do`

> **/api/freeonboard/detail.do**

Melihat detil data FOB berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/freeonboard/list.do`

> **/api/freeonboard/list.do**

Melihat daftar data FOB, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/freeonboard/save.do`

> **/api/freeonboard/save.do**

Membuat data FOB baru atau mengedit data FOB yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama FOB

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/glaccount/bulk-save.do`

> **/api/glaccount/bulk-save.do**

Membuat mengedit beberapa data Akun Perkiraan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/glaccount/delete.do`

> **/api/glaccount/delete.do**

Menghapus data Akun Perkiraan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | False | Menghapus daftar data sesuai dengan Nomor/Kode Perkiraan (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/glaccount/detail.do`

> **/api/glaccount/detail.do**

Melihat detil data Akun Perkiraan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | False | Melihat daftar data sesuai dengan Nomor/Kode Perkiraan (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/glaccount/get-balance.do`

> **/api/glaccount/get-balance.do**

Melihat nilai saldo Akun Perkiraan berdasarkan per Tgl



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| no | string | True | Kode Perkiraan

Cth: Halo Semua 123 |
| asOfDate | string | False | per Tgl

Cth: 31/03/2016 |
| fromDate | string | False | Dari Tanggal

Cth: 31/03/2016 |
| id | integer | False | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data. 

Cth: 1, 2, 3 (Angka non desimal) |
| toDate | string | False | S/d Tanggal

Cth: 31/03/2016 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/glaccount/get-bs-account-amount.do`

> **/api/glaccount/get-bs-account-amount.do**

Melihat saldo akun Neraca per tanggal tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| asOfDate | string | True | Data per tanggal 

Cth: 31/03/2016 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/glaccount/get-pl-account-amount.do`

> **/api/glaccount/get-pl-account-amount.do**

Melihat saldo akun Laba Rugi dalam periode tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fromDate | string | True | Tanggal mulai data

Cth: 31/03/2016 |
| toDate | string | True | Tanggal akhir data

Cth: 31/03/2016 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/glaccount/list.do`

> **/api/glaccount/list.do**

Melihat daftar data Akun Perkiraan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| accountType | string | False | Filter data yang ingin ditampilkan berdasarkan Jenis Akun

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.accountType.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.accountType.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.leafOnly | boolean | False | Filter data agar tidak menampilkan Akun Induk

Cth: true / false |
| filter.suspended | boolean | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| leafOnly | boolean | False | Filter data agar tidak menampilkan Akun Induk

Cth: true / false |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/glaccount/save.do`

> **/api/glaccount/save.do**

Membuat data Akun Perkiraan baru atau mengedit data Akun Perkiraan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| accountType | string |  |
| asOf | string | Tanggal pengakuan saldo awal akun perkiraan

Cth: 31/03/2016 |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk akun terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| name | string | Nama akun perkiraan

Cth: Halo Semua 123 |
| no | string | Nomor akun perkiraan

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| memo | string | Deskripsi akun perkiraan

Cth: Halo Semua 123 |
| openBalance | number | Saldo awal akun perkiraan dalam satuan mata uang yang ditentukan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| parentNo | string | Jika ingin membuat sub-akun, masukkan nomor akun perkiraan yang akan menjadi induk dari akun terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| useUserRoleAccessListId | array | ID dari grup pengguna yang akan diberi akses ke akun

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item/bulk-save.do`

> **/api/item/bulk-save.do**

Membuat mengedit beberapa data Barang & Jasa sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/item/delete.do`

> **/api/item/delete.do**

Menghapus data Barang & Jasa berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | False | Menghapus daftar data sesuai dengan Nomor/Kode Barang (dapat digunakan untuk menggantikan parameter id)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/detail.do`

> **/api/item/detail.do**

Melihat detil data Barang & Jasa berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | False | Melihat daftar data sesuai dengan Nomor/Kode Barang (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/get-nearest-cost.do`

> **/api/item/get-nearest-cost.do**

Melihat HPP barang pada tanggal tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| itemNo | string | True | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| transDate | string | False | Tanggal transaksi

Cth: 31/03/2016 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/get-stock.do`

> **/api/item/get-stock.do**

Mengambil Jumlah barang yang tersedia



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| no | string | True | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| warehouseName | string | False | Nama record gudang (jika dikosongkan maka diambil nilai total seluruh gudang)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/list.do`

> **/api/item/list.do**

Melihat daftar data Barang & Jasa, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.itemCategoryId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.itemCategoryId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.itemType.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.itemType.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.no.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.no.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.preferedVendorId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.preferedVendorId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.suspended | boolean | False | Filter data berdasarkan status barang

Cth: true / false |
| itemCategoryFilter | string | False | Filter data berdasarkan kategori barang. Gunakan ID record kategori barang sebagai value dari parameter ini

Cth: [{"id":50}, {"id":120}] |
| itemTypeFilter | string | False | Filter data berdasarkan jenis barang. Gunakan nilai pada parameter "itemType" dari API "/save.do" sebagai value dari parameter ini

Cth: ["XXX", "YYY", "ZZZ"] |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| preferedVendorFilter | string | False | Filter data berdasarkan pemasok. Gunakan ID record pemasok sebagai value dari parameter ini

Cth: [{"id":50}, {"id":120}] |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| suspendedFilter | string | False | Filter data berdasarkan status barang

Cth: true, false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/list-stock.do`

> **/api/item/list-stock.do**

Melihat daftar Jumlah barang yang tersedia 



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| asOfDate | string | False | Tanggal transaksi saldo awal persediaan untuk barang/jasa terkait

Cth: 31/03/2016 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| warehouseId | integer | False | Nama record gudang yang akan digunakan untuk mencatat stok pada transaksi saldo awal persediaan terkait (ini adalah alternatif dari parameter warehouseName)

Cth: 1, 2, 3 (Angka non desimal) |
| warehouseName | string | False | Nama record gudang yang akan digunakan untuk mencatat stok pada transaksi saldo awal persediaan terkait

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item/save.do`

> **/api/item/save.do**

Membuat data Barang & Jasa baru atau mengedit data Barang & Jasa yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| itemType | string |  |
| name | string | Nama barang/jasa

Cth: Halo Semua 123 |
| calculateGroupPrice | boolean | Apakah harga jual barang/jasa jenis grup ingin ditentukan secara otomatis dari harga jual detail barang/jasa pada grup tersebut

Cth: true / false |
| cogsGlAccountNo | string | Nomor akun perkiraan untuk mencatat nilai harga pokok untuk barang terkait

Cth: Halo Semua 123 |
| controlQuantity | boolean | Apakah barang/jasa terkait perlu mencatat histori persediaan/stok kontrol

Cth: true / false |
| defaultDiscount | string | Format diskon default untuk barang/jasa terkait (dalam persen). Cth: 2+3 (artinya 2% + 3%)

Cth: Halo Semua 123 |
| detailGroup | array |  |
| detailOpenBalance | array |  |
| dimDepth | number | Panjang (cm)	

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| dimHeight | number | Tinggi (cm)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| dimWidth | number | Lebar (cm)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| goodTransitGlAccountNo | string | Nomor akun untuk mencatat nilai barang/jasa yang sudah dikirim ke pelanggan namun belum ditagih

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inventoryGlAccountNo | string | Nomor akun perkiraan untuk mencatat nilai persediaan untuk barang terkait

Cth: Halo Semua 123 |
| itemCategoryName | string | Nama record kategori barang untuk barang terkait. Cth: Mobil, Motor, dll

Cth: Halo Semua 123 |
| manageExpired | boolean | Apakah nomor seri menggunakan tanggal kadaluarsa

Cth: true / false |
| manageSN | boolean | Apakah barang terkait menggunakan nomor seri

Cth: true / false |
| minimumQuantity | number | Jumlah pembelian minimum untuk barang/jasa terkait pada saat melakukan transaksi pembelian (Dalam satuan yang disebutkan pada parameter "vendorUnitName")

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| minimumQuantityReorder | number | item.api_minimum_quantity_reorder_desc

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| no | string | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| notes | string | Catatan tambahan untuk barang/jasa terkait

Cth: Halo Semua 123 |
| percentTaxable | number | Persentase dasar pengenaan pajak untuk barang/jasa terkait (Default: 100)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| preferedVendorName | string | Nama pemasok barang. Cth: PT. XYZ, dll

Cth: Halo Semua 123 |
| printDetailGroup | boolean | Apakah detail dari grup barang/jasa ingin ditampilkan pada saat transaksi dicetak

Cth: true / false |
| purchaseRetGlAccountNo | string | Nomor akun perkiraan untuk mencatat nilai retur (pengembalian) pembelian untuk barang/jasa terkait

Cth: Halo Semua 123 |
| ratio2 | number | Nilai rasio untuk satuan 2 terhadap satuan 1

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| ratio3 | number | Nilai rasio untuk satuan 3 terhadap satuan 1

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| ratio4 | number | Nilai rasio untuk satuan 4 terhadap satuan 1

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| ratio5 | number | Nilai rasio untuk satuan 5 terhadap satuan 1

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| salesDiscountGlAccountNo | string | Nomor akun untuk mencatat nilai diskon penjualan untuk barang/jasa terkait

Cth: Halo Semua 123 |
| salesGlAccountNo | string | Nomor akun perkiraan untuk mencatat nilai penjualan untuk barang/jasa terkait

Cth: Halo Semua 123 |
| salesRetGlAccountNo | string | Nomor akun perkiraan untuk mencatat nilai retur (pengembalian) penjualan untuk barang/jasa terkait

Cth: Halo Semua 123 |
| serialNumberType | string |  |
| substituted | boolean | Apakah barang/jasa terkait mempunyai barang/jasa alternatif (pengganti) jika stok tidak tersedia ketika bertransaksi

Cth: true / false |
| substitutedItemNo | string | Nomor/Kode unik barang/jasa substitusi (pengganti) untuk barang/jasa terkait jika stok tidak tersedia ketika bertransaksi

Cth: Halo Semua 123 |
| tax1Name | string | Nama record pajak PPN yang ingin dikenakan pada barang terkait

Cth: Halo Semua 123 |
| tax2Name | string | Nama record pajak PPNBM yang ingin dikenakan pada barang terkait

Cth: Halo Semua 123 |
| tax3Name | string | Nama record pajak PPh yang ingin dikenakan pada barang terkait

Cth: Halo Semua 123 |
| tax4Name | string | Nama record pajak PPh 22 yang ingin dikenakan pada barang terkait

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran otomatis yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| unBilledGlAccountNo | string | Nomor akun untuk mencatat nilai barang/jasa yang sudah diterima dari pemasok namun belum ditagih

Cth: Halo Semua 123 |
| unit1Name | string | Nama record satuan 1 yang dapat digunakan pada barang terkait. Cth: Pcs, Lusin, Dus

Cth: Halo Semua 123 |
| unit2Name | string | Nama record satuan 2 yang dapat digunakan pada barang terkait. Cth: Pcs, Lusin, Dus

Cth: Halo Semua 123 |
| unit2Price | number | Harga Jual default satuan 2 barang terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| unit3Name | string | Nama record satuan 3 yang dapat digunakan pada barang terkait. Cth: Pcs, Lusin, Dus

Cth: Halo Semua 123 |
| unit3Price | number | Harga Jual default satuan 3 barang terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| unit4Name | string | Nama record satuan 4 yang dapat digunakan pada barang terkait. Cth: Pcs, Lusin, Dus

Cth: Halo Semua 123 |
| unit4Price | number | Harga Jual default satuan 4 barang terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| unit5Name | string | Nama record satuan 5 yang dapat digunakan pada barang terkait. Cth: Pcs, Lusin, Dus

Cth: Halo Semua 123 |
| unit5Price | number | Harga Jual default satuan 5 barang terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| unitPrice | number | Harga Jual default satuan 1 untuk barang terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| upcNo | string | UPC/Barcode barang

Cth: Halo Semua 123 |
| usePpn | boolean | Barang kena PPn

Cth: true / false |
| useWholesalePrice | boolean | Menerapkan Harga / Diskon Grosir

Cth: true / false |
| vendorPrice | number | Harga pembelian default yang akan digunakan jika belum ada record Harga Pemasok untuk barang/jasa terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| vendorUnitName | string | Nama record satuan barang default yang akan digunakan pada saat melakukan pembelian barang/jasa terkait (Cth: Pcs, Dus, Lusin, dll)

Cth: Halo Semua 123 |
| weight | number | Berat (gr)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/search-by-item-or-sn.do`

> **/api/item/search-by-item-or-sn.do**

Melihat daftar data Barang & Jasa, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| keywords | string | True | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/search-by-no-upc.do`

> **/api/item/search-by-no-upc.do**

Mencari data master barang/jasa berdasarkan Kode atau UPC/Barcode



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/stock-mutation-history.do`

> **/api/item/stock-mutation-history.do**

Melihat histori mutasi stok (hanya menampilkan data 7 hari terakhir)



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.createDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.createDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.transactionType.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transactionType.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item/vendor-price.do`

> **/api/item/vendor-price.do**

Melihat harga beli terakhir dari suatu pemasok



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| itemNo | string | True | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| vendorNo | string | True | ID Pemasok

Cth: Halo Semua 123 |
| currencyCode | string | False | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| currencyId | integer | False | ID mata uang 

Cth: 1, 2, 3 (Angka non desimal) |
| itemId | integer | False | ID dari barang/jasa

Cth: 1, 2, 3 (Angka non desimal) |
| transDate | string | False | Tanggal beli terakhir

Cth: Halo Semua 123 |
| unitId | integer | False | ID dari satuan barang

Cth: 1, 2, 3 (Angka non desimal) |
| unitName | string | False | Nama record satuan barang default yang akan digunakan pada saat melakukan pembelian barang/jasa terkait (Cth: Pcs, Dus, Lusin, dll)

Cth: Halo Semua 123 |
| vendorId | integer | False | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data. 

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item-adjustment/bulk-save.do`

> **/api/item-adjustment/bulk-save.do**

Membuat mengedit beberapa data Penyesuaian Persediaan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/item-adjustment/delete.do`

> **/api/item-adjustment/delete.do**

Menghapus data Penyesuaian Persediaan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item-adjustment/detail.do`

> **/api/item-adjustment/detail.do**

Melihat detil data Penyesuaian Persediaan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item-adjustment/list.do`

> **/api/item-adjustment/list.do**

Melihat daftar data Penyesuaian Persediaan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item-adjustment/save.do`

> **/api/item-adjustment/save.do**

Membuat data Penyesuaian Persediaan baru atau mengedit data Penyesuaian Persediaan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| adjustmentAccountNo | string | Nomor akun penyesuaian persediaan. Jika tidak diisi akan mengambil default di preferensi

Cth: Halo Semua 123 |
| detailItem | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item-adjustment/save-target-quantity.do`

> **/api/item-adjustment/save-target-quantity.do**

Membuat data Penyesuaian Persediaan baru atau mengedit data Penyesuaian Persediaan yang sudah ada, dengan kuantitas yang diinput adalah kuantitas akhir yang diinginkan



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detail | array |  |
| adjustmentAccountNo | string | Nomor akun penyesuaian persediaan. Jika tidak diisi akan mengambil default di preferensi

Cth: Halo Semua 123 |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| transDate | string | Tanggal transaksi

Cth: 31/03/2016 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item-category/bulk-save.do`

> **/api/item-category/bulk-save.do**

Membuat mengedit beberapa data Kategori Barang sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/item-category/delete.do`

> **/api/item-category/delete.do**

Menghapus data Kategori Barang berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | False | Menghapus daftar data sesuai dengan Nomor/Kode Barang (dapat digunakan untuk menggantikan parameter id) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item-category/detail.do`

> **/api/item-category/detail.do**

Melihat detil data Kategori Barang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item-category/list.do`

> **/api/item-category/list.do**

Melihat daftar data Kategori Barang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.leafOnly | boolean | False | Filter data agar tidak menampilkan data induk

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| leafOnly | boolean | False | Filter data agar tidak menampilkan data induk

Cth: true / false |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item-category/save.do`

> **/api/item-category/save.do**

Membuat data Kategori Barang baru atau mengedit data Kategori Barang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Kategori Barang

Cth: Halo Semua 123 |
| defaultCategory | boolean | Kategori Barang Default

Cth: true / false |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| parentName | string | Nama Kategori Barang

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item-transfer/bulk-save.do`

> **/api/item-transfer/bulk-save.do**

Membuat mengedit beberapa data Pemindahan Barang sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/item-transfer/delete.do`

> **/api/item-transfer/delete.do**

Menghapus data Pemindahan Barang berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item-transfer/detail.do`

> **/api/item-transfer/detail.do**

Melihat detil data Pemindahan Barang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/item-transfer/list.do`

> **/api/item-transfer/list.do**

Melihat daftar data Pemindahan Barang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.itemTransferOutStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.itemTransferOutStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.itemTransferType.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.itemTransferType.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.referenceWarehouseId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.referenceWarehouseId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.warehouseId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.warehouseId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/item-transfer/save.do`

> **/api/item-transfer/save.do**

Membuat data Pemindahan Barang baru atau mengedit data Pemindahan Barang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailItem | array |  |
| itemTransferType | string |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| differenceItemTransferAccountNo | string | Nomor record akun perkiraan untuk mencatat apabila terdapat selisih nilai barang saat pemindahan

Cth: Halo Semua 123 |
| fromItemTransferNo | string | Nomor transaksi record pemindahan barang asal yang ingin digunakan (untuk Terima Barang)

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| referenceWarehouseName | string | Nama record gudang tempat tujuan barang dikeluarkan / sumber barang diterima

Cth: Halo Semua 123 |
| saveAsStatusType | string |  |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| warehouseName | string | Nama record gudang tempat sumber barang dikeluarkan / tujuan barang diterima

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/job-order/bulk-save.do`

> **/api/job-order/bulk-save.do**

Membuat mengedit beberapa data Pekerjaan Pesanan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/job-order/delete.do`

> **/api/job-order/delete.do**

Menghapus data Pekerjaan Pesanan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/job-order/detail.do`

> **/api/job-order/detail.do**

Melihat detil data Pekerjaan Pesanan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/job-order/list.do`

> **/api/job-order/list.do**

Melihat daftar data Pekerjaan Pesanan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/job-order/save.do`

> **/api/job-order/save.do**

Membuat data Pekerjaan Pesanan baru atau mengedit data Pekerjaan Pesanan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailExpense | array |  |
| detailItem | array |  |
| differenceAccountNo | string | Akun selisih biaya yang digunakan di pekerjaan pesanan

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| jobAccountNo | string | Akun pekerjaan yang digunakan di pekerjaan pesanan

Cth: Halo Semua 123 |
| manualClosed | boolean | Tutup Pekerjaan

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/journal-voucher/bulk-save.do`

> **/api/journal-voucher/bulk-save.do**

Membuat mengedit beberapa data Jurnal Umum sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/journal-voucher/delete.do`

> **/api/journal-voucher/delete.do**

Menghapus data Jurnal Umum berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/journal-voucher/detail.do`

> **/api/journal-voucher/detail.do**

Melihat detil data Jurnal Umum berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/journal-voucher/list.do`

> **/api/journal-voucher/list.do**

Melihat daftar data Jurnal Umum, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/journal-voucher/save.do`

> **/api/journal-voucher/save.do**

Membuat data Jurnal Umum baru atau mengedit data Jurnal Umum yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailJournalVoucher | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/material-adjustment/bulk-save.do`

> **/api/material-adjustment/bulk-save.do**

Membuat mengedit beberapa data Penambahan Bahan Baku sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/material-adjustment/delete.do`

> **/api/material-adjustment/delete.do**

Menghapus data Penambahan Bahan Baku berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/material-adjustment/detail.do`

> **/api/material-adjustment/detail.do**

Melihat detil data Penambahan Bahan Baku berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/material-adjustment/list.do`

> **/api/material-adjustment/list.do**

Melihat daftar data Penambahan Bahan Baku, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.jobOrderNumber | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Pekerjaan Pesanan

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/material-adjustment/save.do`

> **/api/material-adjustment/save.do**

Membuat data Penambahan Bahan Baku baru atau mengedit data Penambahan Bahan Baku yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailItem | array |  |
| jobOrderNumber | string | material_adjustment.api_job_order_number_desc

Cth: Halo Semua 123 |
| materialAdjustmentAccountNo | string | material_adjustment.api_adjustment_account_no_desc

Cth: Halo Semua 123 |
| materialAdjustmentType | string |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/other-deposit/bulk-save.do`

> **/api/other-deposit/bulk-save.do**

Melihat daftar data Penerimaan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/other-deposit/delete.do`

> **/api/other-deposit/delete.do**

Menghapus data Penerimaan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/other-deposit/detail.do`

> **/api/other-deposit/detail.do**

Melihat detil data Penerimaan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/other-deposit/list.do`

> **/api/other-deposit/list.do**

Melihat daftar data Penerimaan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/other-deposit/save.do`

> **/api/other-deposit/save.do**

Membuat data Penerimaan baru atau mengedit data Penerimaan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| bankNo | string | Nomor akun perkiraan bank yang digunakan untuk tujuan penerimaan pembayaran

Cth: Halo Semua 123 |
| detailAccount | array |  |
| payee | string | Informasi Penerima / Penerima dari transaksi

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| chequeDate | string | Tanggal cek untuk transaksi terkait, jika tidak diisi akan menggunakan tanggal transaksi

Cth: 31/03/2016 |
| chequeNo | string | Nomor cek untuk transaksi terkait

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/other-payment/bulk-save.do`

> **/api/other-payment/bulk-save.do**

Membuat mengedit beberapa data Pembayaran sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/other-payment/delete.do`

> **/api/other-payment/delete.do**

Menghapus data Pembayaran berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/other-payment/detail.do`

> **/api/other-payment/detail.do**

Melihat detil data Pembayaran berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/other-payment/list.do`

> **/api/other-payment/list.do**

Melihat daftar data Pembayaran, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/other-payment/save.do`

> **/api/other-payment/save.do**

Membuat data Pembayaran baru atau mengedit data Pembayaran yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| bankNo | string | Nomor akun perkiraan bank yang digunakan untuk tujuan penerimaan pembayaran

Cth: Halo Semua 123 |
| detailAccount | array |  |
| payee | string | Informasi Penerima / Penerima dari transaksi

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| chequeDate | string | Tanggal cek untuk transaksi terkait, jika tidak diisi akan menggunakan tanggal transaksi

Cth: 31/03/2016 |
| chequeNo | string | Nomor cek untuk transaksi terkait

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/payment-term/bulk-save.do`

> **/api/payment-term/bulk-save.do**

Membuat mengedit beberapa data Syarat Pembayaran sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/payment-term/delete.do`

> **/api/payment-term/delete.do**

Menghapus data Syarat Pembayaran berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/payment-term/detail.do`

> **/api/payment-term/detail.do**

Melihat detil data Syarat Pembayaran berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/payment-term/list.do`

> **/api/payment-term/list.do**

Melihat daftar data Syarat Pembayaran, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/payment-term/save.do`

> **/api/payment-term/save.do**

Membuat data Syarat Pembayaran baru atau mengedit data Syarat Pembayaran yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| discDays | integer | Masa Mendapatkan Diskon

Cth: 1, 2, 3 (Angka non desimal) |
| discPC | number | Besar Diskon (%)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| name | string | Nama Syarat Pembayaran

Cth: Halo Semua 123 |
| netDays | integer | Masa Jatuh Tempo

Cth: 1, 2, 3 (Angka non desimal) |
| defaultTerm | boolean | Default Syarat Pembayaran

Cth: true / false |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| memo | string | Keterangan Syarat Pembayaran

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/pos/customer/save.do`

> **/api/pos/customer/save.do**

API untuk mempermudah integrasi dengan sistem POS untuk melakukan import/update data master Pelanggan ke Accurate Online. Jika customer terkait sudah ada di Accurate Online, maka akan dilakukan update data. Jika belum ada akan disimpan sebagai data baru.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/pos/item/save.do`

> **/api/pos/item/save.do**

API untuk mempermudah integrasi dengan sistem POS untuk melakukan import/update data master Barang & Jasa ke Accurate Online. Jika customer terkait sudah ada di Accurate Online, maka akan dilakukan update data. Jika belum ada akan disimpan sebagai data baru.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/pos/transaction/save.do`

> **/api/pos/transaction/save.do**

API untuk mempermudah integrasi dengan sistem POS untuk melakukan import data Faktur Penjualan, Pembayaran Pelanggan dan Retur Penjualan ke Accurate Online. Jika data terkait sudah ada di Accurate Online maka akan diabaikan.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| invoices | array |  |
| payments | array |  |
| returns | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/price-category/detail.do`

> **/api/price-category/detail.do**

Melihat detil data Kategori Penjualan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/price-category/list.do`

> **/api/price-category/list.do**

Melihat daftar data Kategori Penjualan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45)

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/price-category/save.do`

> **/api/price-category/save.do**

Membuat data Kategori Penjualan baru atau mengedit data Kategori Penjualan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Kategori

Cth: Halo Semua 123 |
| description | string | Keterangan

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/project/bulk-save.do`

> **/api/project/bulk-save.do**

Membuat mengedit beberapa data Proyek sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/project/delete.do`

> **/api/project/delete.do**

Menghapus data Proyek berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| projectNo | string | False | Menghapus daftar data sesuai dengan Nomor Proyek (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/project/detail.do`

> **/api/project/detail.do**

Melihat detil data Proyek berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| projectNo | string | False | Melihat daftar data sesuai dengan Nomor Proyek (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/project/list.do`

> **/api/project/list.do**

Melihat daftar data Proyek, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.suspended | boolean | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/project/save.do`

> **/api/project/save.do**

Membuat data Proyek baru atau mengedit data Proyek yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Proyek

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| description | string | Keterangan Proyek

Cth: Halo Semua 123 |
| finishDate | string | Tgl Selesai

Cth: 31/03/2016 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | Nomor Proyek

Cth: Halo Semua 123 |
| startDate | string | Tgl Mulai

Cth: 31/03/2016 |
| suspended | boolean | Non Aktif

Cth: true / false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-invoice/bulk-save.do`

> **/api/purchase-invoice/bulk-save.do**

Membuat mengedit beberapa data Faktur Pembelian sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-invoice/create-down-payment.do`

> **/api/purchase-invoice/create-down-payment.do**

Membuat data Uang Muka Pembelian baru atau mengedit data Uang Muka Pembelian yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| billNumber | string | Nomor referensi tagihan dari pemasok yang terkait dengan transaksi faktur pembelian terkait

Cth: Halo Semua 123 |
| dpAmount | number | Nilai uang muka penjualan untuk faktur uang muka penjualan terkait dalam satuan mata uang yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| documentCode | string |  |
| fiscalRate | number | Kurs pajak (fiskal) yang digunakan untuk transaksi terkait. Isi jika transaksi menggunakan mata uang yang berbeda dari mata uang dasar yang digunakan perusahaan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| isTaxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| poNumber | string | Nomor referensi pesanan pembelian yang terkait dengan transaksi faktur penjualan terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| tax1Name | string | Nama pajak PPN yang ingin dikenakan pada faktur uang muka

Cth: Halo Semua 123 |
| taxDate | string | Untuk menentukan tanggal pencatatatn pajak untuk transaksi terkait (gunakan jika transaksi terkait ingin dicatat pada periode pajak yang berbeda dengan tanggal transaksi)

Cth: 31/03/2016 |
| taxNumber | string | Nomor faktur pajak. Jika dikosongkan otomatis akan menggunakan pernomoran faktur pajak yang sudah di-setting

Cth: Halo Semua 123 |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| transDate | string | Tanggal transaksi

Cth: 31/03/2016 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| vendorTaxType | string |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/purchase-invoice/delete.do`

> **/api/purchase-invoice/delete.do**

Menghapus data Faktur Pembelian berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-invoice/detail.do`

> **/api/purchase-invoice/detail.do**

Melihat detil data Faktur Pembelian berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-invoice/list.do`

> **/api/purchase-invoice/list.do**

Melihat daftar data Faktur Pembelian, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| currencyFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Mata Uang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.dueDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.dueDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.invoiceDp | boolean | False | Filter berdasarkan apakah Faktur adalah Uang Muka Pembelian

Cth: true / false |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.noneInvoiceReturn | boolean | False | Filter berdasarkan apakah Faktur adalah Faktur hasil Retur tanpa Faktur

Cth: true / false |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.openingBalance | boolean | False | Filter berdasarkan apakah Faktur adalah Saldo Awal Pemasok

Cth: true / false |
| filter.outstanding | boolean | False | Filter berdasarkan apakah Faktur sudah lunas

Cth: true / false |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.vendorId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.vendorId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.vendorNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pemasok

Cth: Halo Semua 123 |
| id | integer | False | Filter data yang ingin ditampilkan berdasarkan id

Cth: 1, 2, 3 (Angka non desimal) |
| invoiceDpFilter | string | False | Filter berdasarkan apakah Faktur adalah Uang Muka Pembelian

Cth: true, false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| noneInvoiceReturn | string | False | Filter berdasarkan apakah Faktur adalah Faktur hasil Retur tanpa Faktur |
| openingBalanceFilter | string | False | Filter berdasarkan apakah Faktur adalah Saldo Awal Pemasok

Cth: true, false |
| outstandingFilter | string | False | Filter berdasarkan apakah Faktur sudah lunas

Cth: true, false |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |
| vendorFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pemasok

Cth: [{"id":50}, {"id":120}] |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-invoice/save.do`

> **/api/purchase-invoice/save.do**

Membuat data Faktur Pembelian baru atau mengedit data Faktur Pembelian yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| billNumber | string | Nomor referensi tagihan dari pemasok yang terkait dengan transaksi faktur pembelian terkait

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailDownPayment | array |  |
| detailExpense | array |  |
| detailItem | array |  |
| fillPriceByVendorPrice | boolean | Harga satuan ditentukan dari harga pemasok

Cth: true / false |
| fiscalRate | number | Kurs pajak (fiskal) yang digunakan untuk transaksi terkait. Isi jika transaksi menggunakan mata uang yang berbeda dari mata uang dasar yang digunakan perusahaan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| inputDownPayment | number | purchase_invoice.api_dp_amount_desc

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| invoiceDp | boolean | Apakah transaksi faktur pembelian ini ini merupakan uang muka pembelian

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| orderDownPaymentNumber | string | Nomor transaksi pesanan pembelian untuk uang muka yang digunakan

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| reverseInvoice | boolean | Apakah transaksi faktur pembelian ini ingin disimpan sebagai "Tagihan dimuka" (mendahului penerimaan barang)

Cth: true / false |
| shipDate | string | Tanggal pengiriman

Cth: 31/03/2016 |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| tax1Name | string | Nama pajak PPN yang ingin dikenakan pada faktur uang muka

Cth: Halo Semua 123 |
| taxDate | string | Untuk menentukan tanggal pencatatatn pajak untuk transaksi terkait (gunakan jika transaksi terkait ingin dicatat pada periode pajak yang berbeda dengan tanggal transaksi)

Cth: 31/03/2016 |
| taxNumber | string | Nomor faktur pajak. Jika dikosongkan otomatis akan menggunakan pernomoran faktur pajak yang sudah di-setting

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-order/bulk-save.do`

> **/api/purchase-order/bulk-save.do**

Membuat mengedit beberapa data Pesanan Pembelian sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/purchase-order/delete.do`

> **/api/purchase-order/delete.do**

Menghapus data Pesanan Pembelian berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-order/detail.do`

> **/api/purchase-order/detail.do**

Melihat detil data Pesanan Pembelian berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-order/list.do`

> **/api/purchase-order/list.do**

Melihat daftar data Pesanan Pembelian, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.vendorId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.vendorId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.vendorNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pemasok

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |
| vendorFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pemasok

Cth: [{"id":50}, {"id":120}] |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-order/save.do`

> **/api/purchase-order/save.do**

Membuat data Pesanan Pembelian baru atau mengedit data Pesanan Pembelian yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailExpense | array |  |
| detailItem | array |  |
| fillPriceByVendorPrice | boolean | Harga satuan ditentukan dari harga pemasok

Cth: true / false |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| shipDate | string | Tanggal pengiriman

Cth: 31/03/2016 |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-payment/bulk-save.do`

> **/api/purchase-payment/bulk-save.do**

Membuat mengedit beberapa data Pembayaran Pembelian sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/purchase-payment/delete.do`

> **/api/purchase-payment/delete.do**

Menghapus data Pembayaran Pembelian berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-payment/detail.do`

> **/api/purchase-payment/detail.do**

Melihat detil data Pembayaran Pembelian berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-payment/list.do`

> **/api/purchase-payment/list.do**

Melihat daftar data Pembayaran Pembelian, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.vendorId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.vendorId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.vendorNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pemasok

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |
| vendorFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pemasok

Cth: [{"id":50}, {"id":120}] |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-payment/save.do`

> **/api/purchase-payment/save.do**

Membuat data Pembayaran Pembelian baru atau mengedit data Pembayaran Pembelian yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| bankNo | string | Nomor akun perkiraan bank yang digunakan untuk tujuan penerimaan pembayaran

Cth: Halo Semua 123 |
| chequeAmount | number | Jumlah cek untuk transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| detailInvoice | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| chequeDate | string | Tanggal cek untuk transaksi terkait, jika tidak diisi akan menggunakan tanggal transaksi

Cth: 31/03/2016 |
| chequeNo | string | Nomor cek untuk transaksi terkait

Cth: Halo Semua 123 |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentMethod | string |  |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-requisition/bulk-save.do`

> **/api/purchase-requisition/bulk-save.do**

Membuat mengedit beberapa data Permintaan Barang sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/purchase-requisition/delete.do`

> **/api/purchase-requisition/delete.do**

Menghapus data Permintaan Barang berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-requisition/detail.do`

> **/api/purchase-requisition/detail.do**

Melihat detil data Permintaan Barang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-requisition/list.do`

> **/api/purchase-requisition/list.do**

Melihat daftar data Permintaan Barang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-requisition/save.do`

> **/api/purchase-requisition/save.do**

Membuat data Permintaan Barang baru atau mengedit data Permintaan Barang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailItem | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| requisitionType | string |  |
| saveAsStatusType | string |  |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| warehouseName | string | Nama record gudang tujuan barang diterima.

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-return/bulk-save.do`

> **/api/purchase-return/bulk-save.do**

Membuat mengedit beberapa data Retur Pembelian sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/purchase-return/delete.do`

> **/api/purchase-return/delete.do**

Menghapus data Retur Pembelian berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-return/detail.do`

> **/api/purchase-return/detail.do**

Melihat detil data Retur Pembelian berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/purchase-return/list.do`

> **/api/purchase-return/list.do**

Melihat daftar data Retur Pembelian, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.vendorNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pemasok

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/purchase-return/save.do`

> **/api/purchase-return/save.do**

Membuat data Retur Pembelian baru atau mengedit data Retur Pembelian yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailExpense | array |  |
| detailItem | array |  |
| returnType | string |  |
| taxDate | string | Untuk menentukan tanggal pencatatatn pajak untuk transaksi terkait (gunakan jika transaksi terkait ingin dicatat pada periode pajak yang berbeda dengan tanggal transaksi)

Cth: 31/03/2016 |
| taxNumber | string | Nomor faktur pajak. Jika dikosongkan otomatis akan menggunakan pernomoran faktur pajak yang sudah di-setting

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| fiscalRate | number | Kurs pajak (fiskal) yang digunakan untuk transaksi terkait. Isi jika transaksi menggunakan mata uang yang berbeda dari mata uang dasar yang digunakan perusahaan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| invoiceNumber | string | No Faktur

Cth: Halo Semua 123 |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| receiveItemNumber | string | No Penerimaan Barang

Cth: Halo Semua 123 |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/receive-item/bulk-save.do`

> **/api/receive-item/bulk-save.do**

Membuat mengedit beberapa data Penerimaan Barang sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/receive-item/delete.do`

> **/api/receive-item/delete.do**

Menghapus data Penerimaan Barang berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/receive-item/detail.do`

> **/api/receive-item/detail.do**

Melihat detil data Penerimaan Barang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/receive-item/list.do`

> **/api/receive-item/list.do**

Melihat daftar data Penerimaan Barang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.vendorId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.vendorId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.vendorNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pemasok

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |
| vendorFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pemasok

Cth: [{"id":50}, {"id":120}] |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/receive-item/save.do`

> **/api/receive-item/save.do**

Membuat data Penerimaan Barang baru atau mengedit data Penerimaan Barang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailItem | array |  |
| receiveNumber | string | Nomor transaksi pengiriman barang dari pengirim

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| shipDate | string | Tanggal pengiriman

Cth: 31/03/2016 |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/report/serial-number-mutation.do`

> **/api/report/serial-number-mutation.do**

Melihat daftar data No. Seri/Produksi, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| itemNo | string | True | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| fromDate | string | False | Filter tanggal mulai data yang ingin ditampilkan

Cth: 31/03/2016 |
| serialNumber | string | False | Nomor Seri / Produksi barang

Cth: Halo Semua 123 |
| toDate | string | False | Filter tanggal akhir data yang ingin ditampilkan

Cth: 31/03/2016 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/report/serial-number-per-warehouse.do`

> **/api/report/serial-number-per-warehouse.do**

Melihat daftar data No. Seri/Produksi, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| itemNo | string | True | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/report/stock-mutation-summary.do`

> **/api/report/stock-mutation-summary.do**

Melihat daftar data Ringkasan mutasi stok barang/jasa, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fromDate | string | True | Filter tanggal mulai data yang ingin ditampilkan

Cth: 31/03/2016 |
| itemNo | string | True | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| toDate | string | True | Filter tanggal akhir data yang ingin ditampilkan

Cth: 31/03/2016 |
| itemId | integer | False | ID dari barang/jasa

Cth: 1, 2, 3 (Angka non desimal) |
| warehouseName | string | False | Nama gudang

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/report/work-order-detail.do`

> **/api/report/work-order-detail.do**

Melihat daftar data Perintah Kerja, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| workOrderNo | string | True | No Perintah Kerja

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/roll-over/bulk-save.do`

> **/api/roll-over/bulk-save.do**

Membuat mengedit beberapa data Penyelesaian Pesanan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/roll-over/delete.do`

> **/api/roll-over/delete.do**

Menghapus data Penyelesaian Pesanan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/roll-over/detail.do`

> **/api/roll-over/detail.do**

Melihat detil data Penyelesaian Pesanan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/roll-over/list.do`

> **/api/roll-over/list.do**

Melihat daftar data Penyelesaian Pesanan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| filter.approvalStatus | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.jobOrderNumber | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Pekerjaan Pesanan

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/roll-over/save.do`

> **/api/roll-over/save.do**

Membuat data Penyelesaian Pesanan baru atau mengedit data Penyelesaian Pesanan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailExpense | array |  |
| detailItem | array |  |
| jobOrderNumber | string | No Pekerjaan #

Cth: Halo Semua 123 |
| rollOverType | string |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-invoice/bulk-save.do`

> **/api/sales-invoice/bulk-save.do**

Membuat mengedit beberapa data Faktur Penjualan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-invoice/create-down-payment.do`

> **/api/sales-invoice/create-down-payment.do**

Membuat data Uang Muka Penjualan baru atau mengedit data Uang Muka Penjualan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| dpAmount | number | Nilai uang muka penjualan untuk faktur uang muka penjualan terkait dalam satuan mata uang yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| documentCode | string |  |
| fiscalRate | number | Kurs pajak (fiskal) yang digunakan untuk transaksi terkait. Isi jika transaksi menggunakan mata uang yang berbeda dari mata uang dasar yang digunakan perusahaan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| isTaxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| poNumber | string | Nomor referensi pesanan pembelian yang terkait dengan transaksi faktur penjualan terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| retailIdCard | string | NIK dari Pelanggan

Cth: Halo Semua 123 |
| soNumber | string | Nomor transaksi pesanan penjualan untuk uang muka yang digunakan

Cth: Halo Semua 123 |
| tax1Name | string | Nama pajak PPN yang ingin dikenakan pada faktur uang muka

Cth: Halo Semua 123 |
| taxDate | string | Untuk menentukan tanggal pencatatatn pajak untuk transaksi terkait (gunakan jika transaksi terkait ingin dicatat pada periode pajak yang berbeda dengan tanggal transaksi)

Cth: 31/03/2016 |
| taxNumber | string | Nomor faktur pajak. Jika dikosongkan otomatis akan menggunakan pernomoran faktur pajak yang sudah di-setting

Cth: Halo Semua 123 |
| taxType | string |  |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| transDate | string | Tanggal transaksi

Cth: 31/03/2016 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/sales-invoice/delete.do`

> **/api/sales-invoice/delete.do**

Menghapus data Faktur Penjualan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-invoice/detail.do`

> **/api/sales-invoice/detail.do**

Melihat detil data Faktur Penjualan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-invoice/detail-invoice.do`

> **/api/sales-invoice/detail-invoice.do**

Menampilkan faktur penjualan berdasarkan filter tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| customerNo | string | True | ID Pelanggan

Cth: Halo Semua 123 |
| fromDate | string | False | Dari tanggal

Cth: 31/03/2016 |
| itemNo | string | False | Nomor/Kode unik barang/jasa

Cth: Halo Semua 123 |
| salesmanName | string | False | Nama Penjual

Cth: Halo Semua 123 |
| serialNumber | string | False | Daftar nomor seri / nomor produksi untuk detail transaksi terkait

Cth: Halo Semua 123 |
| toDate | string | False | Hingga tanggal

Cth: 31/03/2016 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-invoice/list.do`

> **/api/sales-invoice/list.do**

Melihat daftar data Faktur Penjualan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| currencyFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Mata Uang

Cth: [50, 120, 150] |
| customerFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pelanggan

Cth: [{"id":50}, {"id":120}] |
| dueDateFilter | string | False | Filter berdasarkan apakah Tanggal Jatuh Tempo Faktur |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.customerId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pelanggan

Cth: Halo Semua 123 |
| filter.dueDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.dueDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.invoiceDp | boolean | False | Filter berdasarkan apakah Faktur adalah Uang Muka Penjualan

Cth: true / false |
| filter.isAccuratePos | boolean | False | Filter berdasarkan apakah Faktur merupakan transaksi dari ACCURATE POS

Cth: true / false |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastPaymentDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastPaymentDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.noneInvoiceReturn | boolean | False | Filter berdasarkan apakah Faktur adalah Faktur hasil Retur tanpa Faktur

Cth: true / false |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.openingBalance | boolean | False | Filter berdasarkan apakah Faktur adalah Saldo Awal Pelanggan

Cth: true / false |
| filter.outstanding | boolean | False | Filter berdasarkan apakah Faktur sudah lunas

Cth: true / false |
| filter.overdue | boolean | False | Filter berdasarkan apakah Faktur sudah jatuh tempo

Cth: true / false |
| filter.paymentTermId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.paymentTermId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.reverseInvoice | boolean | False | Filter berdasarkan apakah Faktur adalah Faktur Dimuka

Cth: true / false |
| filter.reverseInvoiceStatus | string | False | Filter berdasarkan status Faktur Di Muka |
| filter.shipDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.shipDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| invoiceDpFilter | string | False | Filter berdasarkan apakah Faktur adalah Uang Muka Penjualan

Cth: true, false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45)

Cth: Halo Semua 123 |
| noneInvoiceReturnFilter | string | False | Filter berdasarkan apakah Faktur adalah Faktur hasil Retur tanpa Faktur

Cth: true, false |
| openingBalanceFilter | string | False | Filter berdasarkan apakah Faktur adalah Saldo Awal Pelanggan

Cth: true, false |
| outstandingFilter | string | False | Filter berdasarkan apakah Faktur sudah lunas

Cth: true, false |
| paymentTermFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Syarat Pembayaran

Cth: [50, 120, 150] |
| reverseInvoiceFilter | string | False | Filter berdasarkan apakah Faktur adalah Faktur Dimuka

Cth: true, false |
| shipDateFilter | string | False | Filter berdasarkan apakah Tanggal Pengiriman Faktur |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-invoice/save.do`

> **/api/sales-invoice/save.do**

Membuat data Faktur Penjualan baru atau mengedit data Faktur Penjualan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| detailDownPayment | array |  |
| detailExpense | array |  |
| detailItem | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| documentCode | string |  |
| fiscalRate | number | Kurs pajak (fiskal) yang digunakan untuk transaksi terkait. Isi jika transaksi menggunakan mata uang yang berbeda dari mata uang dasar yang digunakan perusahaan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| inputDownPayment | number | Nilai uang muka penjualan untuk faktur uang muka penjualan terkait dalam satuan mata uang yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| invoiceDp | boolean | Apakah transaksi faktur penjualan ini merupakan uang muka penjualan

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| orderDownPaymentNumber | string | Nomor transaksi pesanan penjualan untuk uang muka yang digunakan

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| poNumber | string | Nomor referensi pesanan pembelian yang terkait dengan transaksi faktur penjualan terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| retailIdCard | string | NIK dari Pelanggan

Cth: Halo Semua 123 |
| retailWpName | string | Nama Wajib Pajak

Cth: Halo Semua 123 |
| reverseInvoice | boolean | Apakah transaksi faktur penjualan ini ingin disimpan sebagai "Faktur dimuka" (mendahului pengiriman)

Cth: true / false |
| shipDate | string | Tanggal pengiriman

Cth: 31/03/2016 |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| tax1Name | string | Nama pajak PPN yang ingin dikenakan pada faktur uang muka

Cth: Halo Semua 123 |
| taxDate | string | Untuk menentukan tanggal pencatatatn pajak untuk transaksi terkait (gunakan jika transaksi terkait ingin dicatat pada periode pajak yang berbeda dengan tanggal transaksi)

Cth: 31/03/2016 |
| taxNumber | string | Nomor faktur pajak. Jika dikosongkan otomatis akan menggunakan pernomoran faktur pajak yang sudah di-setting

Cth: Halo Semua 123 |
| taxType | string |  |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-order/bulk-save.do`

> **/api/sales-order/bulk-save.do**

Membuat mengedit beberapa data Pesanan Penjualan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/sales-order/delete.do`

> **/api/sales-order/delete.do**

Menghapus data Pesanan Penjualan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-order/detail.do`

> **/api/sales-order/detail.do**

Melihat detil data Pesanan Penjualan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-order/list.do`

> **/api/sales-order/list.do**

Melihat daftar data Pesanan Penjualan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| currencyFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Mata Uang

Cth: [50, 120, 150] |
| customerFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pelanggan

Cth: [{"id":50}, {"id":120}] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.customerId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pelanggan

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.status.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.status.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45)

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| statusFilter | string | False | Filter berdasarkan Status Pesanan. Nilai yang dapat dikirimkan adalah QUEUE, WAITING, PROCEED, atau CLOSED

Cth: ["XXX", "YYY", "ZZZ"] |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-order/manual-close-order.do`

> **/api/sales-order/manual-close-order.do**

Menutup Pesanan Penjualan secara manual (berdasarkan nomor SO)



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| number | string | Nomor Pesanan Penjualan

Cth: Halo Semua 123 |
| orderClosed | boolean | Tutup pesanan

Cth: true / false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-order/save.do`

> **/api/sales-order/save.do**

Membuat data Pesanan Penjualan baru atau mengedit data Pesanan Penjualan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| detailExpense | array |  |
| detailItem | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| poNumber | string | Nomor referensi pesanan pembelian yang terkait dengan transaksi pesanan penjualan terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| shipDate | string | Tanggal pengiriman

Cth: 31/03/2016 |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-quotation/bulk-save.do`

> **/api/sales-quotation/bulk-save.do**

Membuat mengedit beberapa data Penawaran Penjualan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/sales-quotation/delete.do`

> **/api/sales-quotation/delete.do**

Menghapus data Penawaran Penjualan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-quotation/detail.do`

> **/api/sales-quotation/detail.do**

Melihat detil data Penawaran Penjualan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-quotation/list.do`

> **/api/sales-quotation/list.do**

Melihat daftar data Penawaran Penjualan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pelanggan

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.status | string | False | Filter berdasarkan Status Penawaran. Nilai yang dapat dikirimkan adalah QUEUE, WAITING, PROCEED, atau CLOSED |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45)

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-quotation/save.do`

> **/api/sales-quotation/save.do**

Membuat data Penawaran Penjualan baru atau mengedit data Penawaran Penjualan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| detailItem | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailExpense | array |  |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-receipt/bulk-save.do`

> **/api/sales-receipt/bulk-save.do**

Membuat mengedit beberapa data Penerimaan Penjualan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/sales-receipt/delete.do`

> **/api/sales-receipt/delete.do**

Menghapus data Penerimaan Penjualan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-receipt/detail.do`

> **/api/sales-receipt/detail.do**

Melihat detil data Penerimaan Penjualan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-receipt/list.do`

> **/api/sales-receipt/list.do**

Melihat daftar data Penerimaan Penjualan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| approvalStatusFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED

Cth: ["XXX", "YYY", "ZZZ"] |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| customerFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pelanggan

Cth: [{"id":50}, {"id":120}] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.customerId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pelanggan

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-receipt/save.do`

> **/api/sales-receipt/save.do**

Membuat data Penerimaan Penjualan baru atau mengedit data Penerimaan Penjualan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| bankNo | string | Nomor akun perkiraan bank yang digunakan untuk tujuan penerimaan pembayaran

Cth: Halo Semua 123 |
| chequeAmount | number | Jumlah cek untuk transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| detailInvoice | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| chequeDate | string | Tanggal cek untuk transaksi terkait, jika tidak diisi akan menggunakan tanggal transaksi

Cth: 31/03/2016 |
| chequeNo | string | Nomor cek untuk transaksi terkait

Cth: Halo Semua 123 |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| passValidateInvoiceDate | boolean | Bypass validasi tanggal pembayaran lebih kecil dari tanggal faktur

Cth: true / false |
| paymentMethod | string |  |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| useCredit | boolean | Pakai Kredit 

Cth: true / false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-return/bulk-save.do`

> **/api/sales-return/bulk-save.do**

Membuat mengedit beberapa data Retur Penjualan sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/sales-return/delete.do`

> **/api/sales-return/delete.do**

Menghapus data Retur Penjualan berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-return/detail.do`

> **/api/sales-return/detail.do**

Melihat detil data Retur Penjualan berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sales-return/list.do`

> **/api/sales-return/list.do**

Melihat daftar data Retur Penjualan, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| branchFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Cabang

Cth: [50, 120, 150] |
| customerFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Pelanggan

Cth: [{"id":50}, {"id":120}] |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.customerId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.customerNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pelanggan

Cth: Halo Semua 123 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.returnType.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.returnType.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| id | integer | False | Filter data yang ingin ditampilkan berdasarkan id

Cth: 1, 2, 3 (Angka non desimal) |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45)

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sales-return/save.do`

> **/api/sales-return/save.do**

Membuat data Retur Penjualan baru atau mengedit data Retur Penjualan yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| customerNo | string | Nomor identitas pelanggan

Cth: Halo Semua 123 |
| detailExpense | array |  |
| detailItem | array |  |
| returnType | string |  |
| taxDate | string | Untuk menentukan tanggal pencatatatn pajak untuk transaksi terkait (gunakan jika transaksi terkait ingin dicatat pada periode pajak yang berbeda dengan tanggal transaksi)

Cth: 31/03/2016 |
| taxNumber | string | Nomor faktur pajak. Jika dikosongkan otomatis akan menggunakan pernomoran faktur pajak yang sudah di-setting

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| cashDiscPercent | string | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam persen. Cth: 5 + 2 (berarti diskon bertingkat 5% lalu 2%)

Cth: Halo Semua 123 |
| cashDiscount | number | Isi jika ingin memberikan diskon untuk nilai total transaksi dalam nilai fix. Cth: 2500 (berarti diskon 2500 dalam satuan mata uang yang digunakan pada transaksi terkait)

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| deliveryOrderNumber | string | No Pengiriman Pesanan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| fiscalRate | number | Kurs pajak (fiskal) yang digunakan untuk transaksi terkait. Isi jika transaksi menggunakan mata uang yang berbeda dari mata uang dasar yang digunakan perusahaan

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| fobName | string | Nama record FOB (freight on board) yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| inclusiveTax | boolean | Apakah nilai transaksi terkait sudah termasuk pajak

Cth: true / false |
| invoiceNumber | string | No Faktur

Cth: Halo Semua 123 |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| paymentTermName | string | Nama record termin pembayaran yang diberlakukan untuk transaksi terkait

Cth: Halo Semua 123 |
| rate | number | Jika mata uang yang digunakan pada transaksiuser_ berbeda dari mata uang dasar yang digunakan perusahaan, isi parameter ini dengan nilai tukar mata uang (komersil) yang digunakan pada transaksi terkait

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| shipmentName | string | Nama record pengiriman yang digunakan untuk transaksi terkait. Cth: JNE, DHL, dll

Cth: Halo Semua 123 |
| taxable | boolean | Apakah transaki terkait dikenakan pajak

Cth: true / false |
| toAddress | string | Alamat penagihan (faktur penjualan) / alamat pengiriman (pengiriman pesanan) / alamat pemasok (faktur pembelian)

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/sellingprice-adjustment/delete.do`

> **/api/sellingprice-adjustment/delete.do**

Menghapus data Penyesuaian Harga/Diskon berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sellingprice-adjustment/detail.do`

> **/api/sellingprice-adjustment/detail.do**

Melihat detil data Penyesuaian Harga/Diskon berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/sellingprice-adjustment/list.do`

> **/api/sellingprice-adjustment/list.do**

Melihat daftar data Penyesuaian Harga/Diskon, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.currencyId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.currencyId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.suspended | boolean | False | Filter data berdasarkan status barang

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/sellingprice-adjustment/save.do`

> **/api/sellingprice-adjustment/save.do**

Membuat data Penyesuaian Harga/Diskon baru atau mengedit data Penyesuaian Harga/Diskon yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailItem | array |  |
| priceCategoryName | string | Kategori penjualan

Cth: Halo Semua 123 |
| salesAdjustmentType | string |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| currencyCode | string | sellingprice_adjustment.sellingprice_adjustment.api_currency_code_desc

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/shipment/bulk-save.do`

> **/api/shipment/bulk-save.do**

Membuat mengedit beberapa data Pengiriman sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/shipment/delete.do`

> **/api/shipment/delete.do**

Menghapus data Pengiriman berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| shipmentName | string | False | Menghapus daftar data sesuai dengan Nama Pengiriman (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/shipment/detail.do`

> **/api/shipment/detail.do**

Melihat detil data Pengiriman berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| shipmentName | string | False | Melihat daftar data sesuai dengan Nama Pengiriman (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/shipment/list.do`

> **/api/shipment/list.do**

Melihat daftar data Pengiriman, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/shipment/save.do`

> **/api/shipment/save.do**

Membuat data Pengiriman baru atau mengedit data Pengiriman yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Pengiriman (Cth: DHL, JNE, TIKI, POS, dll)

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/stock-opname-order/bulk-save.do`

> **/api/stock-opname-order/bulk-save.do**

Membuat mengedit beberapa data Perintah Stok Opname sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/stock-opname-order/delete.do`

> **/api/stock-opname-order/delete.do**

Menghapus data Perintah Stok Opname berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | False | Menghapus daftar sesuai dengan nomor SPK

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/stock-opname-order/detail.do`

> **/api/stock-opname-order/detail.do**

Melihat detil data Perintah Stok Opname berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/stock-opname-order/list.do`

> **/api/stock-opname-order/list.do**

Melihat daftar data Perintah Stok Opname, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/stock-opname-order/save.do`

> **/api/stock-opname-order/save.do**

Membuat data Perintah Stok Opname baru atau mengedit data Perintah Stok Opname yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| itemCategoryListName | array | Kategori barang yang akan diperiksa saat stok opname

Cth: Halo Semua 123 |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| personCharged | string | Nama penanggung jawab

Cth: Halo Semua 123 |
| userListAccount | array | Pengguna yang akan melakukan stock opname

Cth: Halo Semua 123 |
| warehouseName | string | Nama record gudang yang akan dilakukan stok opname

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| departmentId | integer | ID record department yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| departmentName | string | Nama Departemen

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| startDate | string | Tanggal mulai

Cth: 31/03/2016 |
| transDate | string | Tanggal SPK

Cth: 31/03/2016 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| vendorListNo | array | Pemasok dari barang yang akan diperiksa saat stock opname

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/stock-opname-result/bulk-save.do`

> **/api/stock-opname-result/bulk-save.do**

Membuat mengedit beberapa data Hasil Stok Opname sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/stock-opname-result/delete.do`

> **/api/stock-opname-result/delete.do**

Menghapus data Hasil Stok Opname berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| no | string | False | Menghapus daftar sesuai dengan nomor Hasil Stok Opname

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/stock-opname-result/detail.do`

> **/api/stock-opname-result/detail.do**

Melihat detil data Hasil Stok Opname berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/stock-opname-result/list.do`

> **/api/stock-opname-result/list.do**

Melihat daftar data Hasil Stok Opname, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.approvalStatus | string | False | Filter data yang ingin ditampilkan berdasarkan Status Persetujuan Transaksi. Nilai yang dapat digunakan adalah kombinasi dari DRAFT, UNAPPROVED, APPROVED, REJECTED, atau NEXTUSER_TOAPPROVED |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| transDateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Tanggal pengakuan transaksi |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/stock-opname-result/save.do`

> **/api/stock-opname-result/save.do**

Membuat data Hasil Stok Opname baru atau mengedit data Hasil Stok Opname yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailItem | array |  |
| orderNumber | string | Nomor Perintah Opname yang ingin digunakan

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/tax/bulk-save.do`

> **/api/tax/bulk-save.do**

Membuat mengedit beberapa data Pajak sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/tax/delete.do`

> **/api/tax/delete.do**

Menghapus data Pajak berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/tax/detail.do`

> **/api/tax/detail.do**

Melihat detil data Pajak berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/tax/list.do`

> **/api/tax/list.do**

Melihat daftar data Pajak, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.taxType.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.taxType.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/tax/save.do`

> **/api/tax/save.do**

Membuat data Pajak baru atau mengedit data Pajak yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| purchaseTaxGlAccountNo | string | Nomor akun pembelian untuk pajak tersebut. Digunakan untuk menjurnal transaksi-transaksi pembelian.

Cth: Halo Semua 123 |
| salesTaxGlAccountNo | string | Nomor akun penjualan untuk pajak tersebut. Digunakan untuk menjurnal transaksi-transaksi penjualan.

Cth: Halo Semua 123 |
| description | string | Deskripsi dari pajak tersebut

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| pph23Type | string |  |
| rate | number | Nilai persentase untuk perhitungan pajak

Cth: 95275.123456 (Nilai maksimum: 999 miliar dengan 6 digit desimal) |
| taxType | string |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/unit/bulk-save.do`

> **/api/unit/bulk-save.do**

Membuat mengedit beberapa data Satuan Barang sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/unit/delete.do`

> **/api/unit/delete.do**

Menghapus data Satuan Barang berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| unitName | string | False | Menghapus daftar data sesuai dengan Nama Satuan Barang (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/unit/detail.do`

> **/api/unit/detail.do**

Melihat detil data Satuan Barang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| unitName | string | False | Melihat daftar data sesuai dengan Nama Satuan Barang (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/unit/list.do`

> **/api/unit/list.do**

Melihat daftar data Satuan Barang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/unit/save.do`

> **/api/unit/save.do**

Membuat data Satuan Barang baru atau mengedit data Satuan Barang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama Satuan (Cth: Pcs, Lusin, Dus, dll)

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor/bulk-save.do`

> **/api/vendor/bulk-save.do**

Membuat mengedit beberapa data Pemasok sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/vendor/delete.do`

> **/api/vendor/delete.do**

Melihat detil data Pemasok berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| vendorNo | string | False | Menghapus daftar data sesuai dengan Nomor Identitas Pemasok (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor/detail.do`

> **/api/vendor/detail.do**

Melihat detil data Pemasok berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| vendorNo | string | False | Melihat detil daftar sesuai dengan Nomor Identitas Pemasok (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor/list.do`

> **/api/vendor/list.do**

Melihat daftar data Pemasok, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.no.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.no.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.suspended | boolean | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |
| suspendedFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true, false |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor/save.do`

> **/api/vendor/save.do**

Membuat data Pemasok baru atau mengedit data Pemasok yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama entitas. Cth: PT. XYZ, John Doe, dll)

Cth: Halo Semua 123 |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| billCity | string | Nama kota alamat penagihan

Cth: Halo Semua 123 |
| billCountry | string | Nama negara alamat pengiriman

Cth: Halo Semua 123 |
| billProvince | string | Nama provinsi alamat penagihan

Cth: Halo Semua 123 |
| billStreet | string | Nama jalan alamat penagihan

Cth: Halo Semua 123 |
| billZipCode | string | Kode pos alamat penagihan

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| categoryName | string | Nama record kategori pemasok

Cth: Halo Semua 123 |
| currencyCode | string | Kode record mata uang default yang ingin digunakan pada saat bertransaksi dengan perusahaan terkait (Cth: IDR, USD, dll)

Cth: Halo Semua 123 |
| defaultIncTax | boolean | Apakah secara default transaksi dengan perushaan terkait akan dikenakan pajak

Cth: true / false |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailContact | array |  |
| detailOpenBalance | array |  |
| email | string | Alamat Email (Cth: johndoe@example.com)

Cth: Halo Semua 123 |
| fax | string | Nomor faximili

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| mobilePhone | string | Nomor handphone

Cth: Halo Semua 123 |
| notes | string | Catatan tambahan untuk data perusahaan terkait

Cth: Halo Semua 123 |
| npwpNo | string | Nomor NPWP (Nomor Pokok Wajib Pajak)

Cth: Halo Semua 123 |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| pkpNo | string | Nomor PKP (Pengusaha Kena Pajak)

Cth: Halo Semua 123 |
| taxCity | string | Nama kota alamat pajak

Cth: Halo Semua 123 |
| taxCountry | string | Nama negara alamat pajak

Cth: Halo Semua 123 |
| taxProvince | string | Nama provinsi alamat pajak

Cth: Halo Semua 123 |
| taxSameAsBill | boolean | Apakah alamat pajak sama dengan alamat penagihan

Cth: true / false |
| taxStreet | string | Nama jalan alamat pajak

Cth: Halo Semua 123 |
| taxZipCode | string | Kode pos alamat pajak

Cth: Halo Semua 123 |
| termName | string | Nama record termin pembayaran default yang ingin digunakan pada saat bertransaksi dengan perusahaan terkait

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| vendorTaxType | string |  |
| website | string | Alamat Website (Cth: http://cpssoft.com)

Cth: Halo Semua 123 |
| workPhone | string | Nomor telepon kantor

Cth: Halo Semua 123 |
| wpName | string | company.api_wp_name_desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor-category/bulk-save.do`

> **/api/vendor-category/bulk-save.do**

Membuat mengedit beberapa data Kategori Pemasok sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/vendor-category/delete.do`

> **/api/vendor-category/delete.do**

Melihat detil data Kategori Pemasok berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| name | string | False | Menghapus daftar data sesuai dengan Nama Kategori Pemasok (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor-category/detail.do`

> **/api/vendor-category/detail.do**

Melihat detil data Kategori Pemasok berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| name | string | False | Melihat daftar data sesuai dengan Nama Kategori Pemasok (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor-category/list.do`

> **/api/vendor-category/list.do**

Melihat daftar data Kategori Pemasok, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.leafOnly | boolean | False | Filter data agar tidak menampilkan data induk

Cth: true / false |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor-category/save.do`

> **/api/vendor-category/save.do**

Membuat data Kategori Pemasok baru atau mengedit data Kategori Pemasok yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama kategori pemasok

Cth: Halo Semua 123 |
| defaultCategory | boolean | Kategori pemasok sebagai default

Cth: true / false |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| parentId | integer | ID induk kategori pemasok

Cth: 1, 2, 3 (Angka non desimal) |
| parentName | string | Nama induk kategori pemasok

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor-claim/bulk-save.do`

> **/api/vendor-claim/bulk-save.do**

Membuat mengedit beberapa data Klaim Pemasok sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/vendor-claim/delete.do`

> **/api/vendor-claim/delete.do**

Menghapus data Klaim Pemasok berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor-claim/detail.do`

> **/api/vendor-claim/detail.do**

Melihat detil data Klaim Pemasok berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor-claim/list.do`

> **/api/vendor-claim/list.do**

Melihat daftar data Klaim Pemasok, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.approvalStatus.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.approvalStatus.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan |
| filter.branchId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.branchId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.branchName | string | False | Filter data yang ingin ditampilkan berdasarkan Nama Cabang

Cth: Halo Semua 123 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.vendorId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.vendorId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.vendorNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pemasok

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor-claim/save.do`

> **/api/vendor-claim/save.do**

Membuat data Klaim Pemasok baru atau mengedit data Klaim Pemasok yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| detailItem | array |  |
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| vendorClaimType | string |  |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| fromVendorClaimNo | string | Nomor Klaim Pemasok

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| saveAsStatusType | string |  |
| toAddress | string | Alamat Pemasok

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| vendorId | integer | Nama pemasok yang akan digunakan untuk mencatat klaim pemasok terkait (ini adalah alternatif dari parameter vendorName)

Cth: 1, 2, 3 (Angka non desimal) |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor-price/bulk-save.do`

> **/api/vendor-price/bulk-save.do**

Membuat mengedit beberapa data Harga Pemasok sekaligus (Max: 100 data dalam 1 kali request). Ganti nama parameter "[n]" dengan index data mulai dari nol (Cth: data[0], data[1], dst.) pada parameter request.



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| data | array |  |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/vendor-price/delete.do`

> **/api/vendor-price/delete.do**

Menghapus data Harga Pemasok berdasarkan id tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Menghapus daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor-price/detail.do`

> **/api/vendor-price/detail.do**

Melihat detil data Harga Pemasok berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | False | Melihat detil daftar sesuai dengan Nomor transaksi (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/vendor-price/list.do`

> **/api/vendor-price/list.do**

Melihat daftar data Harga Pemasok, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| fields | string | False | Field-field yang ingin ditampilkan, dipisahkan dengan koma. Daftar field yang dapat digunakan dapat dilihat pada response dari API detail.do. Cth: id, name, no

Cth: Halo Semua 123 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.number.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.number.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.transDate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.transDate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 |
| filter.vendorId.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.vendorId.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.vendorNo | string | False | Filter data yang ingin ditampilkan berdasarkan Nomor Identitas Pemasok

Cth: Halo Semua 123 |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| lastUpdateFilter | string | False | Filter data yang ingin ditampilkan berdasarkan Waktu perubahan data (Cth: 25/07/2015 14:38:45) |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/vendor-price/save.do`

> **/api/vendor-price/save.do**

Membuat data Harga Pemasok baru atau mengedit data Harga Pemasok yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| transDate | string | Tanggal pengakuan yang ingin dicatat untuk transaksi terkait

Cth: 31/03/2016 |
| branchId | integer | ID record cabang yang ingin digunakan

Cth: 1, 2, 3 (Angka non desimal) |
| branchName | string | Nama cabang yang ingin digunakan

Cth: Halo Semua 123 |
| currencyCode | string | Kode mata uang yang ingin digunakan untuk transaksi terkait. Cth: IDR, USD, dll

Cth: Halo Semua 123 |
| description | string | Catatan tambahan untuk transaksi terkait

Cth: Halo Semua 123 |
| detailItem | array |  |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| number | string | Nomor transaksi yang ingin digunakan untuk mengidentifikasi transaksi terkait. Isi parameter ini jika tidak menggunakan penomoran otomatis.

Cth: Halo Semua 123 |
| typeAutoNumber | integer | ID record penomoran transaksi yang ingin digunakan (kosongkan jika menggunakan penomoran default)

Cth: 1, 2, 3 (Angka non desimal) |
| vendorNo | string | Nomor identitas vendor

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## DELETE `/api/warehouse/delete.do`

> **/api/warehouse/delete.do**

Melihat detil data Gudang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Menghapus daftar data sesuai dengan id data

Cth: 1, 2, 3 (Angka non desimal) |
| warehouseName | string | False | Menghapus daftar data sesuai dengan Nama Gudang (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/warehouse/detail.do`

> **/api/warehouse/detail.do**

Melihat detil data Gudang berdasarkan id atau identifier tertentu



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| id | integer | True | Identitas unik dari sebuah record data. Didapatkan dari field id yang ada di setiap record data.

Cth: 1, 2, 3 (Angka non desimal) |
| warehouseName | string | False | Melihat daftar data sesuai dengan Nama Gudang (ini adalah alternatif dari parameter id data)

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## GET `/api/warehouse/list.do`

> **/api/warehouse/list.do**

Melihat daftar data Gudang, dengan filter yang sesuai



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |
| filter.id.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.id.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 1, 2, 3 (Angka non desimal) |
| filter.keywords.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.keywords.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: Halo Semua 123 |
| filter.lastUpdate.op | string | False | Jenis Operator penyaringan data (Default: EQUAL) |
| filter.lastUpdate.val | array | False | Nilai yang akan digunakan untuk menyaring data. Jika nilai parameter yang dikirimkan hanya satu, boleh tidak menggunakan index pada nama parameter ([n]). Untuk Operator EQUAL, NOT_EQUAL, BETWEEN dan NOT_BETWEEN nilai parameter "val" bisa lebih dari 1 (gunakan index [n]). Untuk Operator EMPTY dan NOT_EMPTY nilai parameter "val" akan diabaikan

Cth: 31/03/2016 18:30:43 |
| filter.suspended | boolean | False | Filter data yang ingin ditampilkan berdasarkan Status Non Aktif

Cth: true / false |
| keywords | string | False | Kata kunci pencarian data

Cth: Halo Semua 123 |
| sp.page | integer | False | Halaman data. Mulai dari angka 1 (Cth: 1, 2, 3, dll)

Cth: 1, 2, 3 (Angka non desimal) |
| sp.pageSize | integer | False | Jumlah data per halaman. Default: 20

Cth: 1, 2, 3 (Angka non desimal) |
| sp.sort | string | False | Urutkan data berdasarkan nama field dan cara pengurutan (ascending / descending). Contoh, jika ingin diurutkan berdasarkan nama secara ascending, lalu berdasarkan nomor secara descending maka gunakan: name|asc;no|desc

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
## POST `/api/warehouse/save.do`

> **/api/warehouse/save.do**

Membuat data Gudang baru atau mengedit data Gudang yang sudah ada



### 🔗 Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| X-Session-ID | string | True | Kode Session yang didapatkan dari response saat memanggil API /api/open-db.do

Cth: Halo Semua 123 |


### 📦 Request Body 

| Field | Type | Description |
|-------|------|-------------|
| name | string | Nama gudang

Cth: Halo Semua 123 |
| city | string | Nama kota

Cth: Halo Semua 123 |
| country | string | Nama negera

Cth: Halo Semua 123 |
| description | string | Deskripsi gudang

Cth: Halo Semua 123 |
| id | integer | Nomor ID internal yang menjadi identitas dari data terkait. Perlu diisi apabila ingin melakukan perubahan atau penghapusan data terkait

Cth: 1, 2, 3 (Angka non desimal) |
| pic | string | Nama penanggung jawab

Cth: Halo Semua 123 |
| province | string | Nama propinsi

Cth: Halo Semua 123 |
| scrapWarehouse | boolean | Merupakan gudang barang rusak

Cth: true / false |
| street | string | Nama jalan

Cth: Halo Semua 123 |
| suspended | boolean | Gudang non-aktif

Cth: true / false |
| zipCode | string | Kode Pos

Cth: Halo Semua 123 |


### ✅ Responses

| Status Code | Description | Component |
|-------------|-------------|-----------|
| 200 | Success |  |
