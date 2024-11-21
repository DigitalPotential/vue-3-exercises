<script setup>
import { reactive, computed } from 'vue'

const state = reactive({
  isDarkMode: false,
  newTodoText: '',
  showError: false,
  todos: [
    { id: 1, text: 'Lär dig Vue', completed: false, priority: true },
    { id: 2, text: 'Bygg en app', completed: false, priority: false }
  ]
})

const totalTodos = computed(() => state.todos.length)

const completedTodos = computed(() => 
  state.todos.filter(todo => todo.completed).length
)

const remainingTodos = computed(() => 
  state.todos.filter(todo => !todo.completed).length
)

const completionRate = computed(() => {
  if (totalTodos.value === 0) return 0
  return Math.round((completedTodos.value / totalTodos.value) * 100)
})

const isValidTodo = computed(() => 
  state.newTodoText.length >= 3
)

const toggleTheme = () => {
  state.isDarkMode = !state.isDarkMode
}

const addTodo = () => {
  if (!isValidTodo.value) {
    state.showError = true
    return
  }
  
  state.showError = false
  state.todos.push({
    id: Date.now(),
    text: state.newTodoText,
    completed: false,
    priority: false
  })
  state.newTodoText = ''
}

const togglePriority = (todo) => {
  todo.priority = !todo.priority
}

const removeTodo = (todoId) => {
  state.todos = state.todos.filter(todo => todo.id !== todoId)
}
</script>

<template>
  <div class="app-container">
    <header :class="{ 'dark-mode': state.isDarkMode }">
      <h1>Min Todo App</h1>
      <button 
        :class="{ 'theme-btn': true, 'dark': state.isDarkMode }"
        @click="toggleTheme"
      >
        {{ state.isDarkMode ? '☀️' : '🌙' }}
      </button>
    </header>

    <div class="add-todo">
      <input 
        type="text" 
        v-model="state.newTodoText"
        placeholder="Lägg till ny todo..."
        :class="{ 'error': state.showError }"
        @keyup.enter="addTodo"
      >
      <button 
        @click="addTodo"
        :disabled="!isValidTodo"
      >
        Lägg till
      </button>
    </div>

    <p v-if="state.showError" class="error-message">
      En todo måste ha minst 3 tecken
    </p>

    <div class="stats">
      <p>Totalt antal: {{ totalTodos }}</p>
      <p>Klara: {{ completedTodos }}</p>
      <p>Återstående: {{ remainingTodos }}</p>
      <p>Procent klara: {{ completionRate }}%</p>
    </div>

    <ul class="todo-list">
      <li 
        v-for="todo in state.todos" 
        :key="todo.id"
        :class="{ 
          'todo-item': true,
          'completed': todo.completed,
          'priority': todo.priority
        }"
      >
        <input 
          type="checkbox"
          v-model="todo.completed"
        >
        <span :class="{ 'done': todo.completed }">
          {{ todo.text }}
        </span>
        <div class="todo-actions">
          <button @click="togglePriority(todo)" class="priority-btn">
            {{ todo.priority ? '⭐' : '☆' }}
          </button>
          <button @click="removeTodo(todo.id)" class="delete-btn">
            🗑️
          </button>
        </div>
      </li>
    </ul>
  </div>
</template>

<style>
.app-container {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #f0f0f0;
  border-radius: 8px;
  margin-bottom: 20px;
}

header.dark-mode {
  background-color: #333;
  color: white;
}

.theme-btn {
  padding: 8px;
  border-radius: 50%;
  border: none;
  cursor: pointer;
  background: white;
}

.theme-btn.dark {
  background: #666;
}

.add-todo {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

.add-todo input {
  flex: 1;
  padding: 8px;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.add-todo input.error {
  border-color: red;
}

.error-message {
  color: red;
  font-size: 0.9em;
  margin-top: -15px;
  margin-bottom: 15px;
}

.stats {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
  background: #f9f9f9;
  padding: 15px;
  border-radius: 8px;
  margin-bottom: 20px;
}

.todo-list {
  list-style: none;
  padding: 0;
}

.todo-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px;
  background: white;
  border: 1px solid #ddd;
  margin-bottom: 5px;
  border-radius: 4px;
}

.todo-item.completed {
  background: #f8f8f8;
}

.todo-item.priority {
  border-left: 4px solid gold;
}

.done {
  text-decoration: line-through;
  color: #888;
}

button {
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  background: #4CAF50;
  color: white;
  cursor: pointer;
}

button:disabled {
  background: #cccccc;
  cursor: not-allowed;
}

.todo-actions {
  display: flex;
  gap: 8px;
  margin-left: auto;
}

.priority-btn, .delete-btn {
  padding: 4px 8px;
  border-radius: 4px;
  cursor: pointer;
}

.delete-btn {
  background-color: #ff4444;
}

.delete-btn:hover {
  background-color: #cc0000;
}
</style>
