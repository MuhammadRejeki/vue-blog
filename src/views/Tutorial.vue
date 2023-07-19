<template>
    <div class="container">
        <h1>Composition API Tutorial 1</h1>
        <h2>Refs</h2>
        <p>{{ data_refs.name }} - {{ data_refs.age }}</p>
        <button @click="handleClick">Change Refs</button>
        <br>
        <h2>Reactive</h2>
        <p>{{ data_reactive.name }} - {{ data_reactive.age }}</p>
        <button @click="handleClickReactive">Change Reactive</button>

        <br>
        <h2>Reactive cannot define primitive variable</h2>
        <!-- <p>data : {{ data_primitive }}</p> -->
        <!-- <button @click="handleClickPrimitive">Change Reactive</button> -->
        
    </div>
</template>

<script>
import { ref , reactive} from 'vue'

export default {
    name:"Tutorial",
    setup(){
        // console.log("setup loaded");

        const data_refs     = ref({name:'mario',age:'30'});
        const data_reactive = reactive({name:'budi',age:'10'});
        // const data_primitive = reactive("gokil");

        const handleClick = () => {
            data_refs.value.name = "luigi";
            data_refs.value.age++;
        }

        const handleClickReactive = () => {
            data_reactive.name = "reactive";
            data_reactive.age++;
        }

        // const handleClickPrimitive = () => {
        //     data_primitive = "sukses";
        // }

        return { data_refs , data_reactive , handleClick ,handleClickReactive}
        // data_primitive, handleClickPrimitive
    },
    created(){
        // console.log("created loaded");
    },
    mounted(){
        // console.log("mounted loaded");
    }
}
</script>

<style>

</style>