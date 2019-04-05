<template>
  <section>
    <h1>Todos</h1>

    <div class="btn-group my-4" role="group" aria-label="Basic example">
      <nuxt-link to="/todos" :class="{ 'btn-primary': !completed }" class="btn">All</nuxt-link>
      <nuxt-link :to="{name: 'todos', query: { completed: 'true' } }" :class="{ 'btn-primary': completed === 'true' }" class="btn">Complete</nuxt-link>
      <nuxt-link :to="{name: 'todos', query: { completed: 'false' } }" :class="{ 'btn-primary': completed === 'false' }" class="btn">Uncomplete</nuxt-link>
    </div>

    <ul class="list-group">
      <li v-for="todo in todos" :key="todo.id" class="list-group-item d-flex justify-content-between align-items-center">
        {{ todo.title }}
        <span v-if="todo.completed" class="badge badge-success badge-pill">:)</span>
        <span v-if="!todo.completed" class="badge badge-light badge-pill">:(</span>
      </li>
    </ul>

  </section>
</template>

<script>
export default {
  async asyncData ({ query }) {
    const value = query.completed ? `?completed=${query.completed}` : '';
    const response = await fetch(`https://jsonplaceholder.typicode.com/todos${value}`);
    const todos = await response.json();
    return { todos, completed: query.completed };
  },

  watchQuery: ['completed']
}
</script>

<style>
</style>
