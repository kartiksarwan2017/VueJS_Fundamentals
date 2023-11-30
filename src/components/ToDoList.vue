<template>
    <h1>Hello From ToDo list template</h1>
</template>

<script>
  export default {
    data(){
        return {
            todos: [
                {todoString: "Make Angular Course", completed: false},
                {todoString: "Cook some food", completed: true},
                {todoString: "Make Youtube Videos", completed: true},
                {todoString: "Publish these videos", completed: false}
            ]
        }
    },
    methods: {
        addTodo(newTodo){
            this.todos.push({
                todoString: newTodo, 
                completed: false
            })
        },
        toggleTodo(todo){
            todo.completed = !todo.completed
        },
        editTodo(todo, newTodoString){
            todo.todoString = newTodoString
        },
        deleteTodo(deleteTodo){
            this.todos = this.todos.filter(todo => todo !== deleteTodo);
        }
    }
  };
</script>

<style>

</style>
