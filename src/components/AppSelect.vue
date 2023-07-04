<template >
    <div class="container">
        <select class="form-select w-25 mx-auto mt-5 text-center" v-model="selectedOption" @change="$emit('select-change', this.selectedOption)">
            <option v-for="type in this.typelist" :value="type">{{ type }}</option>
        </select>
    </div>
</template>

<script>

export default {
    data() {
        return {
            typelist: [
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water",
            ],
            selectedOption: null,
        }
    },
    emits: ['select-change']
}
</script>

<style lang="scss" scoped></style>