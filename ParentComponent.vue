<template>
    <div>
        <ChildComponent :message="parentMessage" @childEvent="handleChildEvent" />
        <p>Message du composant enfant: {{ childMessage }}</p>
    </div>
</template>
  
<script>
import ChildComponent from './ChildComponent.vue';

export default {
    components: {
        ChildComponent
    },
    data() {
        return {
            parentMessage: 'Message du parent',
            childMessage: ''
        };
    },
    methods: {
        handleChildEvent(data) {
            this.childMessage = data;
        }
    }
}
</script>