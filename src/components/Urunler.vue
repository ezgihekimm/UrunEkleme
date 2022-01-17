<template>
 <div class="container">
    <div class="row">
        <div v-for="item in list" :key="item" class="col-md-3 mb-4">
            <div class="card">
                <ul class="list-group list-group-flush " style="text-align:center">
                    <img :src="item.resim" alt="" style="width: 100px; display: block; margin: auto; padding:7px;">
                    <li class="list-group-item">Ürün İsim: {{item.isim}}</li>
                    <li class="list-group-item">Ürün Adet: {{item.adet}}</li>
                    <li class="list-group-item">Ürün Fiyat: {{item.fiyat}}</li>
                </ul> 
            </div>
        </div>
    </div>
 </div>
</template>

 
 /* <ul>
        <li v-for="item in list" :key="item" >
            {{item}}
            
            <img :src="item.resim" alt="">
           
        </li>
    </ul>*/

<script>

export default{
    props:{
        list:Array
    }
}
</script>
