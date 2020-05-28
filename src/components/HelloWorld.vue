<template>
  <div class="hello-world">
      <img class="shape1" src="../assets/Shape 1.svg" alt="">

      <div class="text-container">
          <h1>Hello <span class="purple">World</span></h1>
          <p>
                I’m a young web designer and front end developer, you probably know me from Stadia+ or Poppobot. <br>
                <br>
                Have something to say?
          </p>
      </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@use '../colors.scss';
@use '../text.scss';

.shape1 {
    position: absolute;
    top: 0;
    left: 0;
}

.text-container {
    position: absolute;
    top: 25%;
    left: 25%;
    z-index: 1;
    width: 600px;

    h1 {
        margin-bottom: 1rem;
    }

    .purple {
        color: colors.$purple;
    }
}
</style>
