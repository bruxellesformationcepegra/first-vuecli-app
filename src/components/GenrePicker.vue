<template>
    <div>
        <h2>Sélectionnez un genre de films</h2>
        <button @click="setGenre('Cartoon')">Cartoon</button>
        <button @click="setGenre('Comedy')">Comedy</button>
        <button @click="setGenre('Teen')">Teen</button>
    </div>
</template>

<script>
export default {
    methods:{
        setGenre(genre){
            //dire qu'on a sélectionné un genre
            //devoir émettre un événement pour communiquer avec son parent
            this.$emit('genreSelected', genre)
        }
    }
}
</script>

<style>

</style>
