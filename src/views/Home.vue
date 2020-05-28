<template>
  <div class="home">
    <HelloWorld/>
    <About/>
    <Portfolio/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import About from '@/components/About.vue'
import Portfolio from '@/components/Portfolio.vue'

export default {
    name: 'Home',
    components: {
        HelloWorld,
        About,
        Portfolio,
    }
}
</script>
