<template>
    <div>
        <hr>
        <h3>Another Counter Button</h3>
        <button class="btn btn-primary" @click="asyncIncrement({by: 50, duration: 500})">Increment</button>
        <button class="btn btn-primary" @click="asyncDecrement({by: 50, duration: 500})">Decrement</button>
    </div>
</template>

<script>
    import { mapActions } from 'vuex';

    export default {
        methods: {
            ...mapActions({
                asyncIncrement: 'counter/asyncIncrement',
                asyncDecrement: 'counter/asyncDecrement'
            })
        }
    }
</script>