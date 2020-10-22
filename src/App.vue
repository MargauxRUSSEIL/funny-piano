<template>
  <div id="app" class="text-center m-auto pt-10 w-full h-full">
    <v-header></v-header>
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