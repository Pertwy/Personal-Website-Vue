<template>
    <div class="tech-map row">
        <div 
            v-for="tech in techStack" 
            :key="tech"
            @click="$emit('handleClick', tech)"
            :class="filterArray.includes(tech) ? 'tech-on' : 'tech'"
        >
            {{tech === "HTML_CSS_JS" ? "HTML CSS JS" : tech}}
        </div>
            
    </div>
</template>

<script>
    export default {
        props:["techStack", "filterArray"],
        name: "TechMap",
    }
</script>

<style scoped>
    .row{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        /* justify-content: space-around; */
    }
    .tech-map{
        margin-bottom: 20px;
    }
    .tech{
        margin: 5px;
        border: black 1px solid;
        padding: 5px 10px;
        border-radius: 20px;
    }
    .tech:hover{
        cursor: pointer;
        background-color: blueviolet;
    }
    .tech-on{
        margin: 5px;
        border: black 1px solid;
        padding: 5px 10px;
        border-radius: 20px;
        background-color: blue;
    }
    .tech-on:hover{
        cursor: pointer;
        background-color: burlywood;
    }
</style>