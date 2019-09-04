<template>
    <div class="mavonEditor">
        <mavon-editor v-model="value" style="height:100%;" />
    </div>
</template>

<script>
import Vue from "vue";
import mavonEditor from "mavon-editor";
import "mavon-editor/dist/css/index.css";
Vue.use(mavonEditor);
export default {
    name: "editor",
    data() {
        return {
            value: ""
        };
    }
};
</script>

<style scoped>
.mavonEditor {
    width: 100%;
    height: 100%;
}
</style>