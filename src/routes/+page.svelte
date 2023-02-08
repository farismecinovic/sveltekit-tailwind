<script>
	import Todo from '../components/Todo.svelte';
	import TodoForm from '../components/TodoForm.svelte';
	import { todos } from '../stores/todosStore';
</script>

<div>
	<h1 class="text-2xl font-bold text-center text-gray-800 md:text-3xl">My Todos</h1>
	<TodoForm />
	{#each $todos as todo}
		<Todo {todo} />
	{/each}
</div>
