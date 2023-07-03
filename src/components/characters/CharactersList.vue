<template>
    <section id="characters">
        <div class="row row-cols-5">
            <div v-for="character in store.pokemonList">
                <CharacterCard :name="character.name" :image="character.imageUrl" :type1="character.type1" :type2="character.type2" :color="character.color" :number="character.number" />
            </div>
        </div>
    </section>
</template>

<script>
import CharacterCard from './CharacterCard.vue'
import { store } from '../../store/store.js';

export default {
    components: { CharacterCard },
    data() {
        return { store }
    }
}
</script>

<style lang="scss" scoped></style>