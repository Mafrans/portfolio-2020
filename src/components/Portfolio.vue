<template>
    <div class="portfolio">
        <div class="bar load"></div>

        <div class="shape shape1 load"></div>
        <div class="shape shape2 load"></div>
        <img class="image load" src="../assets/StadiaPlus Large.png" alt="">

        <div class="text-container">
            <h1>STADIA+</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Eget magna fermentum iaculis eu non. Faucibus et molestie ac feugiat. Id leo in vitae turpis massa sed. Aliquet nec ullamcorper sit amet risus. </p>
        </div>

        <div class="links">
            <a target="_blank" href="https://github.com">
                <img src="../assets/vertical_align_bottom.svg" alt="">
            </a>
            <a target="_blank" href="https://github.com">
                <img src="../assets/GitHub-Mark.png" alt="">
            </a>
        </div>
    </div>
</template>

<script>
export default {
    mounted() {
        this.$el.querySelectorAll('.load').forEach(e => e.classList.add('loaded'));
    }
}
</script>

<style lang="scss" scoped>
@use "../text.scss";
@use "../colors.scss";

.portfolio {
    height: 100vh;
    position: relative;
}

.bar {
    position: absolute;
    top: 15%;
    height: 70px;
    width: 0%;
    background: colors.$magenta;
    transition: width 1s ease;

    &.loaded {
        width: 100%;
    }
}

.image, .shape {
    position: absolute;
    top: 14%;
    left: 10%;
    width: 720px;
    height: 530px;
    object-fit: cover;
    border-radius: 75px;
    transform: translate(150px, 150px);
    transition: transform 1s ease;

    &.loaded {
        transform: translate(0px, 0px);
    }
}

.shape {
    transition: transform 1s ease;

    &.shape1 {
        background: colors.$pink;
        transform: translate(150px, 150px);
    }
    &.shape2 {
        background: colors.$light-pink;
        transform: translate(150px, 150px);

        &.loaded {
            transform: translate(75px, 75px);
        }
    }
}

.text-container {
    position: absolute;
    top: 9%;
    left: 40%;
    width: 50%;

    h1 {
        margin-bottom: 1rem;
    }
}

.links {
    position: absolute;
    display: flex;
    justify-content: space-between;
    width: 280px;
    top: 70%;
    right: 10%;
    img {
        height: 120px;
    }
}
</style>