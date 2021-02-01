<template>
    <div class="todo-header">
     
        <DateDisplayer></DateDisplayer>

        <PlusIcon
            @click="addTodo"
            class="button">
        </PlusIcon>
        
       
    </div>
</template>

<script>
import PlusIcon from "vue-material-design-icons/Plus";


import DateDisplayer from "../atoms/DateDisplayer";

export default {
    components: {
         DateDisplayer, PlusIcon
    },
    methods: {
        addTodo(){
            console.log('added')
        }
    }
}
</script>

<style lang="scss"> 
    .todo-header{
        width: 100%;
        display: flex;
        padding: 2rem 1.5rem;
        background-color: #FCFCFF;
        border-bottom: 1px solid #f0eded;
        justify-content: space-between;
    }
    
    .button{
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            padding: .5rem;
            border-radius: 50%;
            color: white;
            text-align: center;
            background-color: #F77374;
    }
</style>