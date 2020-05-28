<template>
    <div class="button">
        <p><slot></slot></p>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
@use "../colors.scss";
@use "../text.scss";

.button {
    padding: 25px 70px;
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 29px;
    background: colors.$magenta;
    display: inline-block;
    border-radius: 50px;
    margin-top: 2rem;

    cursor: pointer;
}
</style>