<template>
 <div class="container mt-3">
    <h1 class="text-center mt-3 mb-3">Ürün Ekleme Uygulaması</h1>
    <hr>
    <div class="row mt-5">
        <div class="col-md-12">
            <UrunAdd  :takip="listtakip"  :list="Ekle" />
        </div>
    </div>
    <div class="row">
        <div class="col-md-12">
            <Bar :list="Ekle"/>
        </div>
    </div>
    
    <hr>
    <div class="row">
        <div class="col-md- d-fle12x justify-content-center">
            <h1>Eklenen Ürünlerin Listesi</h1>

        </div>
    </div>
    <div class="row">
        <Urunler  :list="Ekle"/>
    </div>

  
</div>

</template>



<script>

import UrunAdd from './components/UrunAdd.vue'
import Bar from './components/Bar.vue'
import Urunler from './components/Urunler.vue'
 
export default{
    name:'App',
    components:{
        UrunAdd,
        Bar,
        Urunler
    },

    data() {
        return {
            Ekle:[],
            resim:"",
        }
   },
   methods:{
       listtakip(){
           if(this.Ekle.length>=10){
               alert("Sepetiniz Dolmuştur!!!")
               return true;
           }
           else return false;
       }
   }
}

</script>

<style>

</style>
