<template >
    <div class="pokemonCard" :class="color">
        <div class="img-container">
            <img :src="image" :alt="name" class="rounded-circle img-fluid">
        </div>
        <div>{{ number }}</div>
        <h5>{{ name }}</h5>
        <i>{{ type1 }} {{ type2 }}</i>
    </div>
</template>

<script>
export default {
    props: {
        name: String,
        image: String,
        type1: String,
        type2: String,
        color: String,
        number: Number,
    }
}
</script>

<style lang="scss" scoped>
.pokemonCard {
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 1rem 0;
    padding: 1rem;
    border-radius: 10px;
}

.img-container {}

.Red {
    background-color: #fddfdf;
}

.Green {
    background-color: #defde0;
}

.Blue {
    background-color: #def3fd;
}

.Black {
    background-color: #747474;
}
</style>