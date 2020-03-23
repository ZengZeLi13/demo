<!-- src/components/Hello.vue -->
<template>
    <div>
        <div class="greeting">Hello {{name}}{{swag}}</div>
        <button @click="add">swag+1</button>
    </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
    props: ['name', 'count'],
    data() {
        return {
            num: this.count,
            str: ''
        }
    },
    methods: {
        add() { this.str += 'skr~'; },
    },
    computed: {
        swag(): string {
            return Array(this.num ).join('!') + this.str;
        }
    }
});
</script>

<style>
.greeting {
    font-size: 20px;
}
</style>
