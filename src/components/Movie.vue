<template>
    <div class="movie">
        <h2>{{title}}</h2>
        <p>{{description}}</p>
    </div>
</template>

<script>
export default {
    props: ['title', 'description']
}
</script>

<style>
.movie{
    background-color: deepskyblue;
    margin: 10px;
    padding: 10px;
}

.red{
  background-color: crimson;
}
</style>
