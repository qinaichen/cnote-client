<template>
    <div id="app" :style="{'height':windowHeight}">
        <router-view></router-view>
    </div>
</template>

<script>
export default {
    name: "app",
    components: {},
    data() {
        return {
            windowHeight: "300px"
        };
    },
    methods: {
        resize() {
            this.windowHeight = document.documentElement.clientHeight + "px";
            console.log(this.windowHeight);
        }
    },
    mounted() {
        window.addEventListener("resize", this.resize);
        this.resize();
    }
};
</script>

<style>
body {
    margin: 0;
}
</style>
