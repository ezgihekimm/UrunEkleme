 <template>
     <div class="container">
         <div class="row">
             <div class="col-md-6 d-flex justify-content-end">
                 <div class="card" style="width: 18rem; height:18rem;">

                   

                     <div class="card-body text-center  d-flex align-items-center justify-content-center">

                         <div class="row">
                             <div class="col-md-12">
                                  <img :src="selectedimage == null ? require('../assets/default.png') : selectedimage" class="img-responsive text-center"
                         style="width:150px;" />

                         <div class="row d-flex justify-content-center align-items-center">
                           <div class="col">
                                 <input style="display: none" ref="file"  type="file" @change="onchange($event)" class="form-control">
                         
                            <button type="button" class="btn btn-outline-success" @click="$refs.file.click()">Resim Seç</button>
                                </div>
                            </div>

                            <div v-if="selectedimage == null ? false : true">{{$refs.file.files[0].name}}</div>
                             </div>
                         </div>


                     </div>
                 </div>
             </div>
             <div class="col-md-6 d-flex justify-content-start ">
                 <div class="card" style="width:27rem; height:18rem">
                     <div class="card-body">

                         <div class="row mb-1">
                             <div class="mb-3">
                                 <label for="exampleFormControlInput1" class="form-label">Ürün Adı</label>
                                 <input v-model="isim" type="email" class="form-control" id="exampleFormControlInput1"
                                     placeholder="Adını giriniz">
                             </div>
                         </div>

                         <div class="row mb-1">
                             <div class="col md-6">
                                 <div class="mb-3">
                                     <label for="exampleFormControlInput1" class="form-label">Ürün Adeti</label>
                                     <input v-model="adet" type="email" class="form-control" id="exampleFormControlInput1"
                                         placeholder="Adetini giriniz">
                                 </div>
                             </div>

                             <div class="col-md-6">
                                 <div class="mb-3">
                                     <label for="exampleFormControlInput1" class="form-label">Ürün Fiyatı</label>
                                     <input v-model="fiyat" type="email" class="form-control" id="exampleFormControlInput1"
                                         placeholder="Fiyatı giriniz">
                                 </div>
                             </div>
                         </div>

                         <div class="row ">
                             <div class="col-md-12">

                      
                                  <div>
                                 <button @click="Submit" type="button" class="btn btn-outline-success d-grid col-12">Ekle!!</button>
                                  </div>
                     


                             </div>
                         </div>

                     </div>
                 </div>
             </div>


         </div>
     </div>
 </template>

 <script>
    export default {
        name:'UrunAdd',

        props: {
        list: Array, 
        takip:Function,
            
        },
        methods: {
            
            Submit() {
                this.takip()
                if(this.takip() == false){
                    this.$props.list.push({isim: this.isim,adet: this.adet,fiyat: this.fiyat, resim:this.selectedimage})
                }
            },

            onchange(e){
                const file = e.target.files[0];
                this.selectedimage = URL.createObjectURL(file)
            }
        },
        data(){
            return{
                isim:"",
                adet:"",
                fiyat:"",
                selectedimage:null,

            }
        }

    }
 </script>

 <style >

 </style>