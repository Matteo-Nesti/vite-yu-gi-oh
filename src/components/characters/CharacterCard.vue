<template >
    <div class="pokemonCard shadow" :class="color">
        <div class="img-container">
            <img :src="image" :alt="name">
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
    margin: 1rem 0;
    padding: 1rem;
    border-radius: 10px;
}

.img-container {

    img {
        border-radius: 50%;
        overflow: hidden;
        object-fit: cover;

        width: 150px;
        height: 150px;
    }
}


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