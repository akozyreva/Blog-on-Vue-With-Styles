<template>
    <div>
    <article>
      <div class="container">
        <div class="row">
          <div class="col-lg-8 col-md-10 mx-auto">
             <h2 class="section-heading">Theme</h2>
            <p>{{ showArticle.description }}</p>
             <h2 class="section-heading">Article</h2>
            <p>{{ showArticle.theme }}</p>
         <button class="btn btn-primary" @click="deleteArticle(id)" data-toggle="modal" data-target="#myModal">Delete article</button>
        <app-popup></app-popup>
          </div>
        </div>
      </div>
    </article>

    <hr>

    </div>
</template>
<script>
import { mapGetters } from 'vuex';
import { mapActions } from 'vuex';
import Popup from './Popup.vue';
export default {
    data() {
        return {
            id: this.$route.params.id,
            mainTitle: this.$store.arcticle
        }
    },
    created() {
        this.$store.dispatch('getArticle', this.id);
       
    },
    beforeUpdate() {
         this.$store.dispatch('sendHeadTitle', {
            title: this.$store.state.article.title
        })
    },
     components: {
        'app-popup': Popup
    },
    computed: {
    	...mapGetters(['showArticle'])
    },
    methods: {
        ...mapActions(
            ['deleteArticle']
        )
    }

   	
}
</script>
<style>
</style>