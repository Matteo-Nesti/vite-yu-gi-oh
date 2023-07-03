<template >
    <div class="mainContainer">
        <div class="listContainer">
            <CharactersList />
        </div>
    </div>
</template>

<script>
import CharactersList from './characters/CharactersList.vue'
export default {
    components: { CharactersList },
}
</script>

<style lang="scss" scoped>
.mainContainer {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>