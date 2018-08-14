<template>
    <div>
        <!-- Main Content -->
        <div class="container">
            <div class="row">
                <div class="col-lg-8 col-md-10 mx-auto">
                    <div v-for="(article,index) in data">
                        <div class="post-preview">
                            <router-link tag="a" v-bind:to="`/articles/${article.id}`">
                                <h2 class="post-title">
                                {{ article.title }}
                                </h2>
                                <h3 class="post-subtitle">
                                {{ article.theme }}
                                 </h3>
                            </router-link>
                        </div>
                    </div>
                    <hr>
                    <div class="clearfix">
                        <a class="btn btn-primary float-right" href="#">Older Posts &rarr;</a>
                    </div>
                </div>
            </div>
        </div>
        <hr>
    </div>
</template>
<script>
import axios from '../axios';
import { mapActions } from 'vuex';
export default {
    data() {
        return {
            data: this.$store.state.data
        }
    },
    created() {
        this.$store.dispatch('getArticles');
    },
    mounted() {

        this.$store.dispatch('sendHeadTitle', {
            title: 'Articles',
            subtitle: `All Articles: ${this.$store.getters.countsArticle}`
        })
    },
    methods: {
        ...mapActions(
            ['deleteArticle']
        )
    }
}
</script>
<style scoped>
.theme {
    float: right;
}
</style>