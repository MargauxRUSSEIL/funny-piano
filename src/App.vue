<template>
  <div id="app" class="text-center m-auto pt-10 w-full h-full">
    <h1 class="title m-auto pt-2">The emoji piano</h1>
    <v-emoji></v-emoji>
    <v-piano></v-piano>
  </div>
</template>

<script>
import VPiano from '@/components/VPiano'
import VEmoji from '@/components/VEmoji'
export default {
  name: 'App',
  components: {
    VPiano,
    VEmoji
  }
}
</script>

<style lang="postcss" scoped>
.title {
  @apply bg-black text-white ; 
  height: 60px ;
  width: 332px ;
  border-radius: 10px ;
  font-size: 30px ;
}

#app {
  font-family: 'PT Mono', monospace ;
  background: linear-gradient(135deg, #FF9D6C 0%, #BB4E75 100%) ;
}
</style>