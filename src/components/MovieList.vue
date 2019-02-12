<template>
    <div>
        <Movie v-for="(m, index) in movies"  
        :key="index"  
        :title="m.title"  
        :description="m.description"/>
    </div>
</template>

<script>
import Movie from './Movie.vue'

export default {
    props: ['movies'],
    components: {
        Movie
    }

}
</script>

<style>

</style>
