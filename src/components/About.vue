<template>
    <div>
        <h1>about</h1>
    </div>
</template>
<script>
import { eventBus } from '../main.js';
export default {
    data: function() {
        return {
            title: 'This is section about me'
        }
    },
    created() {
        this.$store.dispatch('sendHeadTitle', {
            title: this.title
        })
    }
}
</script>