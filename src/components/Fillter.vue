<template>
  <div class="Fillter" >
   <p>{{ tongTien.toFixed(2).replace(/(\d)(?=(\d\d\d)+(?!\d))/g, "$1,")}}</p>
   <button @click= "tongTien += 50000">add</button> 
  </div>
</template>

<script>
export default {
    name: 'HelloWorld',
    data() {
        return {
            tongTien: 1000000,
        }
    }
    ,
    // filters: {
    //     dauChamPhanCach(tongTien) {
    //         return tongTien.toFixed(2).replace(/(\d)(?=(\d\d\d)+(?!\d))/g, "$1,");
    //     }
        
    // } // not suported
}
</script>


<style scoped>
 
</style>