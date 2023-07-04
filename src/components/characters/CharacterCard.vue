<template >
    <div class="pokemonCard" :class="color">
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
    box-shadow: 1px 1px 15px rgba(0, 0, 0, 0.8);
}

.img-container {

    img {
        border-radius: 10px;
        overflow: hidden;
        object-fit: cover;
        box-shadow: 1px 1px 15px rgba(0, 0, 0, 0.8);

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