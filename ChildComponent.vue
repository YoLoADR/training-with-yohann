<template>
    <div>
        <p>{{ message }}</p>
        <button @click="emitEvent">Envoyer un message au parent</button>
    </div>
</template>
  
<script>
export default {
    props: ['message'],
    methods: {
        emitEvent() {
            this.$emit('childEvent', 'Bonjour du composant enfant!');
        }
    }
}
</script>
  