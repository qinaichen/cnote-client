<template>
    <el-container class="container">
        <el-aside width="200px" class="sidebar">
            <el-row type="flex" justify="space-around">
                <el-col :span="20">
                    <el-tabs v-model="activeName" :stretch="true">
                        <el-tab-pane label="分类" name="categories"></el-tab-pane>
                        <el-tab-pane label="标签" name="tags"></el-tab-pane>
                    </el-tabs>
                </el-col>
            </el-row>
        </el-aside>
        <el-container class="right-container">
            <el-header class="header">
                <el-row :gutter="24">
                    <el-col :span="24">
                        <el-menu
                            :default-active="activeIndex"
                            mode="horizontal"
                            style="padding-left: 55px;"
                            router
                        >
                            <el-menu-item index="/editor">新文章</el-menu-item>
                        </el-menu>
                    </el-col>
                </el-row>
            </el-header>
            <el-main class="main">
                <router-view></router-view>
            </el-main>
        </el-container>
    </el-container>
</template>
<script>
export default {
    data() {
        return {
            activeName: "categories",
            activeIndex: "/editor"
        };
    }
};
</script>
<style lang="css">
.container {
    height: 100%;
}
.sidebar {
    height: 100%;
    margin: 0 !important;
    border-right: 1px solid #dcdfe6;
}
.main {
    height: 100%;
    padding: 1px;
}
.right-container {
    height: 100%;
}
.header {
    line-height: 60px;
    padding: 0;
}
</style>
