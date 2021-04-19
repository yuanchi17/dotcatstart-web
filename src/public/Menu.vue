<template>
  <Popover>
    <PopoverButton class=" my-auto px-4 py-2 text-yellow-900 text-center border-b-2 border-yellow-900 border-opacity-0 transition duration-300 hover:border-opacity-50 focus:outline-none">
      {{ item.name }}
      <p class="text-xs text-yellow-500"> {{ item.en }}</p>
    </PopoverButton>

    <PopoverPanel class="absolute z-10 border-2 border-yellow-900 rounded pr-4 bg-white">
      <div class="flex space-x-2 my-2" v-for="data in item.info" :key="data">
        <p class="w-16 border-r border-yellow-500">{{ data.title }}</p>
        <div class="space-x-4">
          <a :href="i.href" v-for="i in data.body" :key="i">{{ i.title }}</a>
        </div>
      </div>
    </PopoverPanel>
  </Popover>
</template>

<script>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'

export default {
  name: 'Nav',
  props: {
    item: Object
  },
  components: {
    Popover, PopoverButton, PopoverPanel
  },
  setup () {
    return {
    }
  }
}
</script>

<style>

</style>
