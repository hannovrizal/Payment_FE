# Payment_FE
Pembuatan Repository khusus untuk pembuatan Spesifikasi yang dibutuhkan dalam pembuatan Biller Pinjaman Online

Background
---
Aplikasi Payment Online untuk yang dapat digunakan pembayaran biller pinjaman online

 ![2](https://github.com/hannovrizal/Payment_FE/assets/8992033/e06cc84b-3426-474a-a121-a70da45aa335)

Proses Transaksi Inquiry
---
1.	OpenAPI mengirim request ke OpenShift (A)
2.	Aplikasi akan memproses transaksi ke Switching (B) sekaligus mencatat LOG transaksi yang disimpan di database (F)
3.	Switching akan mengatur transaksi akan dikirim kemana, dalam hal ini switching akan mengirim ke payment gateway (C) lalu ke biller (D)
4.	Setelah mendapatkan jawaban dari biller maka proses akan dikembalikan ke payment gateway (D) > Switching (C) > OpenShift (B) dan terakhir kembali ke depan (A).
   
Proses Transaksi Payment
---
1.	OpenAPI mengirim request ke OpenShift (A)
2.	Aplikasi akan memproses transaksi ke Switching (B) sekaligus mencatat LOG transaksi yang disimpan di database (F)
3.	Switching akan mengatur transaksi akan dikirim kemana, dalam hal ini Switching akan mendebit pengguna dengan mengirimkan data ke core banking (E) setelah debit berhasil dan data Kembali ke switching, switching akan melakukan proses Credit ke biller melewati Payment Gateway lalu ke biller (C dan D)
4.	Setelah mendapatkan jawaban dari biller maka proses akan dikembalikan ke payment gateway (D) > Switching (C) > OpenShift (B) dan terakhir kembali ke depan (A).


