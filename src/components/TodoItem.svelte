<script>
    export let todo;
    export let onDelete;
    export let onUpdate;
  </script>
  
  <div class="todo-item">
    <input type="text" bind:value={todo.name} on:blur={() => onUpdate(todo)} />
    <button on:click={() => onDelete(todo.id)}>Delete</button>
  </div>
  
  <style>
    .todo-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  </style>
  