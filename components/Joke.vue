<template>

<nuxt-link :to="'/jokes/'+ id">

    <div class="joke">
        <ul>
         <li>{{ joke }}</li>
        </ul>



    </div>
</nuxt-link>
    
</template>

<script>
export default {
    name: "Joke",
    props:['joke','id']
}
</script>

<style scoped>

</style>