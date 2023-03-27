<template>
  <Link href="/listing">Listings</Link>&nbsp;
  <Link href="/listing/create">New Listing</Link>

  <!-- <div>The page watch time {{ timer }}</div>  -->
 
  <div v-if="flashSuccess" class="success">
    {{ flashSuccess }}
  </div>
  <slot>Default</slot>
</template>

<script setup>

import { computed } from 'vue'

import { Link, usePage } from '@inertiajs/vue3'


const page = usePage()

const flashSuccess = computed(
  () => page.props.flash.success,
)

// import { ref } from 'vue'

// const timer = ref(0)
// setInterval(() => timer.value++, setTimeout(1000))



</script>

<style scoped>
.success {
  background-color: green;
  color: white;
}
</style>
