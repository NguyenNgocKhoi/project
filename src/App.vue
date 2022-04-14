<script>
import AppHeader from "./components/AppHeader.vue";

export default {
    components: {
        AppHeader,
    },
};
</script>

<template>
    <div id="app">
        <AppHeader />

        <div class="main mt-3">
            <router-view />
        </div>
    </div>
</template>

<style>
.page {
    /* max-width: 400px; */
    margin: auto;
}
.main{
    max-width:1200px;
    margin: 0 auto;
}
</style>