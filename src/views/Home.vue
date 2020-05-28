<template>
  <div class="home">
    <HelloWorld/>
    <About/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import About from '@/components/About.vue'

export default {
    name: 'Home',
    components: {
        HelloWorld,
        About
    }
}
</script>
