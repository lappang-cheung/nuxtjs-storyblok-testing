<template>
  <div>
    <TheHeader />
    <main class="main-content">
      <Nuxt />
    </main>
  </div>
</template>

<script>
import TheHeader from '@/components/TheHeader/TheHeader'

export default {
  components: {
    TheHeader,
  },
}
</script>

<style>
* {
  box-sizing: border-box;
}

body {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  margin: 0;
}

.main-content {
  margin-top: 4.5rem;
}
</style>
