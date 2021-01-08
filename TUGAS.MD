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

get = Ambil semua data,
post = Buat data baru,
put = update data,
del = delete data,
loading = indikator request sedang berlangsung atau telah berhasil
error = response error dari server (apabila terjadi error)

dokumentasi API bisa dilihat di https://reqres.in/
