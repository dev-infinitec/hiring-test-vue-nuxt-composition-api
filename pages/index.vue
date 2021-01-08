<template>
  <div class="mx-auto max-w-screen-md px-6 pt-12">
    <div class="bg-gray-800 rounded-lg shadow">
      <div v-if="value" class="">
        <div
          v-for="o in value.data"
          :key="o.id"
          class="flex items-center px-6 py-4 list relative"
        >
          <div class="mr-5">
            <img
              :src="o.avatar"
              :alt="o.name"
              class="rounded-full"
              style="width: 50px"
            >
          </div>
          <div>
            <nuxt-link to="/" class="font-semibold text-white">
              {{ o.email }}
            </nuxt-link>
            <div class="text-gray-500">
              {{ o.first_name }} {{ o.last_name }}
            </div>
          </div>
          <div class="ml-auto">
            <a
              href="#"
              class="uppercase text-sm text-white text-opacity-75 hover:text-opacity-100 font-semibold"
            >
              Edit
            </a>
            <a
              href="#"
              class="uppercase text-sm text-red-500 text-opacity-75 hover:text-opacity-100 font-semibold"
            >
              Delete
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import {
  defineComponent,
} from '@nuxtjs/composition-api'

import useAxios from '@/composables/use-axios'

export default defineComponent({
  setup() {
    const {
      value = {},
      loading,
      get,
      post,
      put,
      del,
    } = useAxios('/users')

    // Jika parameter di function diisi akan mengirim request ke endpoint
    /// yang sesuai dengan paramter parameter
    // contoh get('/1'), berarti akan mengirim request ke baseurl/users/1
    get()

    const store = async () => {
      await post()
    }

    return { value, loading }
  }
})
</script>
