<template>
    <h1>HEADER COMPONENT</h1>
    <h5>{{Text}}</h5>
    <br>
    <p>{{Paragraft}}</p>
    <h1>{{Value}}</h1>
    <br>

</template>

<script>
    export default{
        name : "Header",
        props : ["Text","Paragraft","Value"],
        data(){
            return{
            NewText : "Ubah text Dari Header.vue"
            }
        },
        method:{
            
        },
    }
</script>