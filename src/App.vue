<template>
    <div id="app">
        <div>
            <app-header></app-header>
            <app-main-header></app-main-header>
            <router-view></router-view>
        </div>
    </div>
</template>
<script>
import Header from './components/Header.vue'
import MainHeader from './components/single components/MainHeader.vue'
export default {
    name: 'app',
    components: {
        'app-header': Header,
        'app-main-header': MainHeader
    },
    data: function() {
        return {
            title: 'This is main page of blog'
        }
    }
}
</script>
<style>
</style>