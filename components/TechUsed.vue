<template>
    <div>
            <img v-for="tech in techUsed" 
            :key="tech" class="tech-logo" :src="require(`@/images/${tech}.png`)"/>
    </div>
</template>

<script>
    export default {
        props:["techUsed"]
    }
</script>

<style scoped>
    .tech-logo{
    height:30px;
    margin-right: 5px;
    }
</style>