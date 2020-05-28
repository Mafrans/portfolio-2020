<template>
    <div class="hello-world">
        <img class="shape shape1" src="../assets/Shape 1.svg" alt="">

        <div class="text-container">
            <h1>Hello <span class="purple">World</span></h1>
            <p>
                I’m a young web designer and front end developer, you probably know me from Stadia+ or Poppobot. <br>
                <br>
                Have something to say?
            </p>
            <btn>Contact Me</btn>
        </div>
        
        <div class="profile">
            <img class="shape shape2" src="../assets/Shape 2.svg" alt="">
            <div class="circle1"></div>
            <div class="circle2"></div>
            <img src="../assets/profile picture.png" alt="" class="profile-picture">
        </div>
    </div>
</template>

<script>
import { Component, Prop, Vue } from 'vue-property-decorator';
import Button from "./Button.vue";

export default {
    components: {
        btn: Button,
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@use '../colors.scss';
@use '../text.scss';

.hello-world {
    height: 100vh;
    width: 100vw;
}

.shape {
    pointer-events: none;
    position: absolute;

    &.shape1 {
        top: 0;
        left: 0;
    }

    &.shape2 {
        top: 10%;
        right: 3%;
    }
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

.profile {
    .profile-picture {
        position: absolute;
        top: 25%;
        right: 10.5%;
        width: 25%;
        border-radius: 50%;
    }

    .circle2 {
        position: absolute;
        top: 22%;
        right: 8%;
        width: 22vw;
        height: 22vw;
        border-radius: 50%;
        background: colors.$pink;
    }

    .circle1 {
        position: absolute;
        top: 21%;
        right: 7%;
        width: 15vw;
        height: 15vw;
        border-radius: 50%;
        background: colors.$light-pink;
    }
}
</style>
