<template>
    <h3>To Do App</h3>

    <form @submit.prevent="addNewTodo">
        <label>Neue Task</label>
        <input v-model="newTodo" name="newTodo" />
        <button>hinzufügen</button>
    </form>
    <h2>{{ newTodo }}</h2>
</template>

<script>
import { ref } from 'vue'

export default {
    setup() {
        function addNewTodo() {
            const newTodo = ref('')
            console.log(newTodo.value)
        }

        return {
            addNewTodo,
            

        }
    }
}
</script>

<style>

</style>