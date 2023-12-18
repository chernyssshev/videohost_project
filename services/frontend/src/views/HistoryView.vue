<script>
import { useFetch } from '../assets/fetch.js';
import { formatDate, formatViews } from '../assets/formatters.js';
import Videos from '../components/Videos.vue';
export default {
    data() {
        return {
            history: null
        }
    },
    methods: {
        async getHistory() {
            const response = await useFetch('get_user_history', {}, true)
            this.history = response.result;
        }, formatDate, formatViews
    },
    mounted() {
        this.getHistory();
    }, components: { Videos }
}
</script>

<template>
    <Videos :videos="this.history" />
</template>