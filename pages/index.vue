<template>
  <div>
    <NuxtLink v-for="item in menuItems" :key="item.text" :to="item.route">
      <img
        :src="require(`../${item.imagePath}`)"
        :alt="item.imageAlt"
      />
      <p>{{ item.text }}</p>
    </NuxtLink>
  </div>
</template>

<script>
import { MENU_ITEMS } from '../content/content'

export default {
  name: 'IndexPage',
  data () {
    return {
      menuItems: MENU_ITEMS
    }
  }
}
</script>
