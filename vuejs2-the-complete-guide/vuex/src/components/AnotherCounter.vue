<template>
    <div>
        <button class="btn btn-primary" @click="asyncIncrement({by: 50, duration: 500})">Increment</button>
        <button class="btn btn-primary" @click="asyncDecrement">Decrement</button>
    </div>
</template>

<script>
    import { mapActions } from 'vuex';
    export default {
        methods: {
            ...mapActions([
                'asyncIncrement',
                'asyncDecrement'
            ])
            /*increment() {
                // this.$emit('updated', 1);
                this.$store.state.counter++;
            },
            decrement() {
                // this.$emit('updated', -1);
                this.$store.state.counter--;
            }*/
        }
    }
</script>