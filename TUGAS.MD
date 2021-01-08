Silahkan clone repository ini

Buat fungsi di file
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
