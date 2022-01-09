<template>
 <div class="container">
    <h1 class="text-center">Ürün Ekleme Uygulaması</h1>
    <hr>
    <div class="row">
        <div class="col-md-6">
            <Image />
        </div>
        <div class="col-md-6">
            <UrunAdd />
        </div>
    </div>
</div>

</template>



<script>
import UrunAdd from './components/UrunAdd.vue'
import Image from './components/Image.vue'


export default{

    components:{
        UrunAdd,
        Image

    }
}

</script>

<style>

</style>
