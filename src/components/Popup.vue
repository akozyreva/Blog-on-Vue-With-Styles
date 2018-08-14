<template>
    <div>
        <!-- Trigger the modal with a button 
    <button type="button" class="btn btn-info btn-lg" data-toggle="modal" data-target="#myModal">Open Modal</button>-->
        <!-- Modal -->
        
          <!-- The Modal -->
  <div class="modal" id="myModal">
    <div class="modal-dialog">
      <div class="modal-content">
      
        <!-- Modal Header -->
        <div class="modal-header">
          <h4 class="modal-title">Modal Heading</h4>
          <button type="button" class="close" data-dismiss="modal">&times;</button>
        </div>
        
        <!-- Modal body -->
        <div class="modal-body">
          {{ showMsg }}
        </div>
        
        <!-- Modal footer -->
        <div class="modal-footer">
          <button type="button" class="btn btn-danger" data-dismiss="modal">Close</button>
        </div>
        
      </div>
    </div>
  </div>
  
    </div>
</template>
<script>
import { mapGetters } from 'vuex';
export default {
    /*created() {
         while created, eventBus is listener on thi Vue
        eventBus.$on('textMsg', (data) => {
            this.myMsg = data;
        });
    }*/
    computed: {
        ...mapGetters(['showMsg'])
    }
}
</script>