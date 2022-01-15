<template>
 <div class="card" style="width: 18rem;">
 
  <ul v-for="item in list" :key="item" class="list-group list-group-flush">
      <img :src="item.resim" alt="">
    <li class="list-group-item">Ürün İsim :{{item.isim}}</li>
    <li class="list-group-item">Ürün Adet:{{item.adet}}</li>
    <li class="list-group-item">Ürün Fiyat :{{item.fiyat}}</li>
  </ul>
  
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
