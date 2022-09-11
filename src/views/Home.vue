<template>
    <h1>Home</h1>
    <div class="text-black">
        hello
    </div>
    <div v-for="items in image" :key="items.albumId">
        <h1 class="text-black">Title : {{items.title}}</h1>
        <h1 class="text-black">image</h1>
        <img :src="items.thumbnailUrl" alt="" width="150" class="mx-auto">
    </div>
</template>

<script>
    import Axios from 'axios';
    export default {
        name:"Home",
        data() {
            return {
                image : null
            }
        },
        methods:{
           async getImage(){
                try {
                    let Data = await Axios.get('https://jsonplaceholder.typicode.com/photos');
                    this.image = Data.data;
                } catch (error) {
                    this.image = "Loading";
                }
            }
        },
        created() {
            this.getImage();
        },
    }
</script>