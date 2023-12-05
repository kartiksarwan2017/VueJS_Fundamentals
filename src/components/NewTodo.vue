<template>
   <form @submit.prevent="addTodo()" class="col-12 col-lf-6">
     <input class="form-control" type="text" v-model="newTodo" placeholder="Enter Todo" />
   </form>
</template>

<script>
export default{
    data() {
        return {
            newTodo: ""
        }
    },
    methods: {
        addTodo(){
            if(this.newTodo.length > 1){
                this.$emit("on-addtodo", this.newTodo);
            }
            this.newTodo = "";
        } 
    }
}
</script>

<style lang="stylus" scoped>

</style>