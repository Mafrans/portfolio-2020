<template>
    <div class="about-me">
        <img class="shape shape1" src="../assets/Shape 3.svg" alt="">

        <div class="text-container">
            <h1>About Me</h1>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Eget magna fermentum iaculis eu non. Faucibus et molestie ac feugiat. Id leo in vitae turpis massa sed. Aliquet nec ullamcorper sit amet risus. 
            </p>
        </div>
    </div>
</template>

<script>
import Button from "./Button.vue";

export default {
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@use '../colors.scss';
@use '../text.scss';

.about-me {
    position: relative;
    height: 100vh;
    width: 100vw;
}

.shape {
    pointer-events: none;
    position: absolute;

    &.shape1 {
        top: -30vh;
        right: 0;
        height: 120vh;
    }
}

.text-container {
    position: absolute;
    top: 33%;
    left: 5%;
    z-index: 1;
    width: 50%;

    h1 {
        margin-bottom: 1rem;
    }

    .purple {
        color: colors.$purple;
    }
}
</style>
