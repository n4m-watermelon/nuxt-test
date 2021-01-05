<template>
<div class="flex-now bg-black">
    <img  class="main-pic" :src="require('../assets/img/banner1.jpg')" alt="">
</div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.bg-black {
    z-index: 2;
   
    height: 400px;
    width: 100%;

    .main-pic{
        width: 100%;
        height: 100%;
    }
    
}


</style>
