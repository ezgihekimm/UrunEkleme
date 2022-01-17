<template>
    <div class="progress mt-5">
        <div class="progress-bar progress-bar-striped bg-danger" role="progressbar" :style="bar"
            aria-valuenow="5" aria-valuemin="0" aria-valuemax="10">{{this.list.length}}/10</div>
    </div>


</template>



<script>
export default{
    props:{
        list:Array
    },
    computed : {
        bar(){
            return `width:${this.list.length*10}%`
        }
    }
}

</script>