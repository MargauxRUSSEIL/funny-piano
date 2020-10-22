<template>
  <div id="app" class="text-center m-auto pt-10 w-full h-full">
    <h1 class="title m-auto pt-2">The emoji piano</h1>
    <v-piano></v-piano>
  </div>
</template>

<script>
import VHeader from '@/components/VHeader'
import VPiano from '@/components/VPiano'
export default {
  name: 'App',
  components: {
    VHeader,
    VPiano
  }
}
</script>

<style lang="postcss" scoped>
#app {
  font-family: 'PT Mono', monospace ;
  background: linear-gradient(135deg, #FF9D6C 0%, #BB4E75 100%) ;
}
</style>