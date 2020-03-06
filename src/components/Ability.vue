<template>
    <div class="ability-container">
        <p>{{ passive }}</p>
        <p>{{ Q }}</p>
        <p>{{ W }}</p>
        <p>{{ E }}</p>
        <p>{{ R }}</p>
    </div>
</template>

<script>
export default {
     name: 'ability',
     props: {
         passive: String,
         Q: String,
         W: String,
         E: String,
         R: String
     }
}
</script>