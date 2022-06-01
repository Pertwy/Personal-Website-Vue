<template>
    <div class="center">
        <a class="certification-link" target="_blank" :href="link">
        <img class="certification" :src="image" :alt="title">
        
            <p>{{title}}</p>
        </a>
    </div>  
</template>

<script>
    export default {
        props:["id", "title", "image", "link"],
        name: "Certification" 
    }
</script>

<style>
    .certification-link{
        text-decoration: none;
        color: black;
        cursor: pointer;
    }
    .certification{
        height:90px;
        width:90px;
    }
</style>