<template>
    <div class="ability-container">
        <div class="abilities">
            <p><span>Passive: </span>{{ passive }}</p>
            <p><span>Ability-Q: </span>{{ Q }}</p>
            <p><span>Ability-W: </span>{{ W }}</p>
            <p><span>Ability-E: </span>{{ E }}</p>
            <p><span>Ability-R: </span>{{ R }}</p>
        </div>
        <AbilityDescription :descPassive="descPassive" :descQ="descQ" :descW="descW" :descE="descE" :descR="descR" />
    </div>
</template>

<script>
import AbilityDescription from './AbilityDescription.vue'

export default {
     name: 'ability',
    data() {
        return {
            descPassive: "Periodically, Aatrox's next basic attack deals bonus physical damage and heals him, based on the target's max health.",
            descQ: "Aatrox slams his greatsword down, dealing physical damage. He can swing three times, each with a different area of effect.",
            descW: "Aatrox smashes the ground, dealing damage to the first enemy hit. Champions and large monsters have to leave the impact area quickly or they will be dragged to the center and take the damage again.",
            descE: "Passively, Aatrox heals when damaging enemy champions. On activation, he dashes in a direction.",
            descR: "Aatrox unleashes his demonic form, fearing nearby enemy minions and gaining attack damage, increased healing, and movement speed. If he gets a takedown, this effect is extended."
        }
    },
     components: {
         AbilityDescription
     },
     props: {
         passive: String,
         Q: String,
         W: String,
         E: String,
         R: String
     }
}
</script>

<style scoped>
    .abilities {
        display: grid;
        grid-template-columns: 20% 20% 20% 20% 20%;
        text-align: center;
    }

    span {
        font-weight: bold;
    }
</style>