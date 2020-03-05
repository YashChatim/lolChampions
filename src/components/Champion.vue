<template>
    <div class="champion-container" @click="displayAbilities()">
        <h1>{{ name }}</h1>
        <p>{{ description }}</p>
    </div>
</template>

<script>
export default {
    name: 'champion',
    props: {
        name: String,
        description: String
    },
    methods: {
        displayAbilities() {
            console.log(`${this.name}`);
        }
    }
}
</script>

<style>
    .champion-container {
        background-color: gray;
    }
</style>