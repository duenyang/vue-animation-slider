<template>
  <div class="an-slider">
      <div class="items">
          <slot></slot>
      </div>
  </div>
</template>
<script>
    export default {
        name: 'an-slider',
        data(){
            return {
                
            }
        },
        created(){

        },
        methods: {

        },
        mounted(){

        }
    }
</script>
<style scoped>
    .an-slider{
        width: 100%;
        height: 100%;
        position: relative;
        overflow: hidden;
    }
    .items{
        position: relative;
        width: 100%;
        height: 100%;
        overflow: hidden;
    }
</style>

