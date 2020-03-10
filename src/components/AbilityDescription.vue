<template>
    <div class="ability-description-continer">
        <p>{{ descPassive }}</p>
        <p>{{ descQ }}</p>
        <p>{{ descW }}</p>
        <p>{{ descE }}</p>
        <p>{{ descR }}</p>
    </div>
</template>

<script>
export default {
    name: 'abilityDescription',
    props: {
        descPassive: String,
        descQ: String,
        descW: String,
        descE: String,
        descR: String
    }
}
</script>

<style scoped>
    .ability-description-continer {
        display: grid;
        grid-template-columns: 20% 20% 20% 20% 20%;
        text-align: center;
    }

    p {
        margin-top: 0;
    }
</style>