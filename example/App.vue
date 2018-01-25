<template>
    <div id="app">
        <a class="btn__loading" @click="switchLoading">Loading</a>
        <Loading :show="show"></Loading>
    </div>
</template>

<script>
    import Loading from '../src/Loading.vue';

    export default {
        name: 'app',
        components: {
            Loading
        },
        data(){
            return {
                show: false,
            }
        },
        methods: {
            switchLoading( ) {
                this.show = true;
                setTimeout(() => {
                    this.show = false;
                }, 3000);
            }
        }
    }
</script>

<style>
    .btn__loading {
        width: 200px;
        box-shadow: 0px 3px 1px -2px rgba(0, 0, 0, 0.2), 0px 2px 2px 0px rgba(0, 0, 0, 0.14), 0px 1px 5px 0px rgba(0, 0, 0, 0.12);
        background-color: #6200ee;
        color: white;
        font-family: Roboto, sans-serif;
        -moz-osx-font-smoothing: grayscale;
        -webkit-font-smoothing: antialiased;
        font-size: 0.875rem;
        line-height: 2.25rem;
        font-weight: 500;
        letter-spacing: 0.04em;
        text-decoration: none;
        text-transform: uppercase;
        --mdc-ripple-fg-size: 0;
        --mdc-ripple-left: 0;
        --mdc-ripple-top: 0;
        --mdc-ripple-fg-scale: 1;
        --mdc-ripple-fg-translate-end: 0;
        --mdc-ripple-fg-translate-start: 0;
        -webkit-tap-highlight-color: transparent;
        will-change: transform, opacity;
        display: inline-block;
        -webkit-box-sizing: border-box;
        box-sizing: border-box;
        min-width: 64px;
        height: 36px;
        padding: 0 16px;
        border: none;
        outline: none;
        text-align: center;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        -webkit-appearance: none;
        overflow: hidden;
        vertical-align: middle;
        border-radius: 2px;
        position: absolute;
        top: 50%;
        left: 50%;
        margin-right: -50%;
        transform: translate(-50%, -50%)
    }
</style>