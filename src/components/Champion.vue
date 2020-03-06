<template>
    <div class="champion-container">
        
        <a href="#" v-on:click="showAbility = !showAbility, displayChampionAbility()"><h1>{{ name }}</h1></a>
        <p>{{ description }}</p>
        <Ability v-show="showAbility" :passive="passive" :Q="abilityQ" :W="abilityW" :E="abilityE" :R="abilityR" />
    </div>
</template>

<script>
import Ability from './Ability.vue';

export default {
    name: 'champion',
    data() {
    return {
      showAbility: false,
      passive: "",
      abilityQ: "",
      abilityW: "",
      abilityE: "",
      abilityR: ""
    }
  },
    components: {
        Ability
    },
    props: {
        name: String,
        description: String
    },
    methods: {
        displayChampionAbility() {
            switch(this.name) {
                case "AATROX": this.passive = "DEATHBRINGER STANCE"; this.abilityQ = "THE DARKIN BLADE"; this.abilityW = "INFERNAL CHAINS"; this.abilityE = "UMBRAL DASH"; this.abilityR = "WORLD ENDER"; break;
                case "AHRI": this.passive = "VASTAYAN GRACE"; this.abilityQ = "ORB OF DECEPTION"; this.abilityW = "FOX-FIRE"; this.abilityE = "CHARM"; this.abilityR = "SPIRIT RUSH"; break;
                case "AKALI": this.passive = "ASSASSIN'S MARK"; this.abilityQ = "FIVE POINT STRIKE"; this.abilityW = "TWILIGHT SHROUD"; this.abilityE = "SHURIKEN FLIP"; this.abilityR = "PERFECT EXECUTION"; break;
                case "ALISTAR": this.passive = "TRIUMPHANT ROAR"; this.abilityQ = "PULVERIZE"; this.abilityW = "HEADBUTT"; this.abilityE = "TRAMPLE"; this.abilityR = "UNBREAKABLE WILL"; break;
                case "AMUMU": this.passive = "CURSED TOUCH"; this.abilityQ = "BANDAGE TOSS"; this.abilityW = "DESPAIR"; this.abilityE = "TANTRUM"; this.abilityR = "CURSE OF THE SAD MUMMY"; break;
                case "ANIVIA": this.passive = "REBIRTH"; this.abilityQ = "FLASH FROST"; this.abilityW = "CRYSTALLIZE"; this.abilityE = "FROSTBITE"; this.abilityR = "GLACIAL STORM"; break;
                case "ANNIE": this.passive = "PYROMANIA"; this.abilityQ = "DISINTEGRATE"; this.abilityW = "INCINERATE"; this.abilityE = "MOLTEN SHIELD"; this.abilityR = "SUMMON: TIBBERS"; break;
                case "APHELIOS": this.passive = "THE HITMAN AND THE SEER"; this.abilityQ = "WEAPON ABILITES"; this.abilityW = "PHASE"; this.abilityE = "WEAPON QUEUE SYSTEM"; this.abilityR = "MOONLIGHT VIGIL"; break;
                case "ASHE": this.passive = "FROST SHOT"; this.abilityQ = "RANGER'S FOCUS"; this.abilityW = "VOLLEY"; this.abilityE = "HAWKSHOT"; this.abilityR = "ENCHANTED CRYSTAL ARROW"; break;
                case "AURELION SOL": this.passive = "CENTER OF THE UNIVERSE"; this.abilityQ = "STARSURGE"; this.abilityW = "CELESTIAL EXPANSION"; this.abilityE = "COMET OF LEGEND"; this.abilityR = "VOICE OF LIGHT"; break;
                case "AZIR": this.passive = "SHURIMA'S LEGACY"; this.abilityQ = "CONQUERING SANDS"; this.abilityW = "ARISE!"; this.abilityE = "SHIFTING SANDS"; this.abilityR = "EMPEROR'S DIVIDE"; break;
                default: return 0;
            }
        }
    }
}
</script>

<style>
    .champion-container {
        background-color: gray;
    }
</style>