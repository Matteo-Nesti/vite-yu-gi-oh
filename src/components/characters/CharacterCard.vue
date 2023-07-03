<template >
    <div class="pokemonCard">
        <div>{{ name }}</div>
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

<style lang="scss" scoped></style>