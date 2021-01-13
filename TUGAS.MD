Silahkan clone repository ini

1. Buat fungsi di file
```/composables/use-axios.ts```

yang mana nanti akan digunakan di pages/index.vue, penulisan diwajibkan menggunakan typescript dan vue composition API,
Untuk axios Anda bisa import fungsi
```
import { useContext } from '@nuxtjs/composition-api'

const { $axios } = useContext()
```
silahkan lihat file /pages/index.vue, ada 7 yang diimport dan semuanya harus terpenuhi

```
const {
  value,
  loading,
  error,
  get,
  post,
  put,
  del,
} = useAxios('/users')
```
- value = response data dari API yang tersedia yang akan ditampilkan di list rendering.
- get = Ambil semua data.
- post = Buat data baru.
- put = update data,
- del = delete data.
- loading = indikator request sedang berlangsung atau telah berhenti.
- error = response error dari server (apabila terjadi error).

mohon re-redesign design yang telah ada, dan tampilkan indikator loading, error (jika terjadi), Anda hanya perlu buat 1 page saja.

Jika tugas telah selesai silahkan informasikan kepada kami link repo Anda. terima kasih.

dokumentasi API bisa dilihat di https://reqres.in/



2. Diberikan n, ambil jumlah dari digit n. Jika nilai tersebut memiliki lebih dari satu digit, lanjutkan mengurangi dengan cara ini sampai satu digit dihasilkan. Masukan/inputan berupa bilangan bulat non-negatif.

Contoh
    16  -->  1 + 6 = 7
   942  -->  9 + 4 + 2 = 15  -->  1 + 5 = 6
132189  -->  1 + 3 + 2 + 1 + 8 + 9 = 24  -->  2 + 4 = 6
493193  -->  4 + 9 + 3 + 1 + 9 + 3 = 29  -->  2 + 9 = 11  -->  1 + 1 = 2

soal no.2 bisa pakai javascript biasa (tanpa framework)
