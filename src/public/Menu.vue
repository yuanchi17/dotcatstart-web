<template>
  <Menu as="div" class="flex flex-col relative ">
    <MenuButton class=" my-auto px-4 py-2 text-yellow-900 text-center border-b-2 border-yellow-900 border-opacity-0 transition duration-300 hover:border-opacity-50 focus:outline-none">
      {{ item.name }}
      <p class="text-xs text-yellow-500"> {{ item.en }}</p>
    </MenuButton>
    <!-- TODO: MenuItems的位置 orz -->
    <MenuItems class="absolute inset-x-0 bottom-0 border-2 border-yellow-900 rounded focus:outline-none">
      <MenuItem v-for="data in item.info" :key="data">
        <a href="/">{{ data.title }}</a>
      </MenuItem>
    </MenuItems>
  </Menu>
</template>

<script>
// import { ref } from 'vue'
import { Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'

export default {
  name: 'Nav',
  props: {
    item: Object
  },
  components: {
    Menu,
    MenuButton,
    MenuItem,
    MenuItems
  },
  setup () {
    return {
    }
  }
}
</script>

<style>

</style>
