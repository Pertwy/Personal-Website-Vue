<template>
    <section>
        <h1>Portfolio</h1>
        <p>Click to select or deselect technologies</p>

        <TechMap
            :techStack="techStack"
            :filterArray="filterArray"
            @handleClick = "handleClick"
        />
        <div >
            <ProjectMap
                :filterArray="filterArray"
            />
        </div>
    </section>
</template>

<script>
    import TechMap from "../components/TechMap.vue"
    import ProjectMap from "../components/ProjectMap.vue"
    export default {
        name: 'Portfolio',
        components: {
            TechMap,
            ProjectMap
        },
        methods: {
            handleClick(tech){
                if(this.filterArray.includes(tech)){
                    this.filterArray = this.filterArray.filter(item => item != tech)
                } else {
                    this.filterArray.push(tech)
                }
            }
        },
        data() {
            return {
                showData: true,
                techStack:[
                    "React",
                    "ReactNative",
                    "Typescript",
                    "HTML_CSS_JS",
                    "MongoDB",
                    "Express",
                    "Firebase",
                    "RestfulAPIs",
                    "Heroku",
                    "Vue"
                ],
                filterArray:[]
            }
        }
    }
</script>

<style scoped>

</style>