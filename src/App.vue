<script setup>
import {ref, onMounted, computed, watch} from 'vue'

const todos = ref([])
const name = ref('')

const input_content = ref('')
const input_category = ref(null)

const todo_asc = computed(() => todos.value.sort((a, b) => {
    return b.createdAt - a.createdAt
}))
</script>

<template>
      <main class="app">
           <section class="greeting">
                <h2 class="title">
                   what's up, <input type="text" placeholder="Name here"  v-model="name" />
                </h2>
           </section>
      </main>
</template>

