<template>
    <div class="todo-body">
        <ul v-for="item in items" :key="item.id">
                <TodoRow
                    v-bind:item="item"
                ></TodoRow>
        </ul>
    </div>
</template>

<script>
import TodoRow from "../atoms/TodoRow";
export default {
    components: {TodoRow},
    data() {
        return {
            items: [
                {   
                    id: 1,
                    subject: 'Bajar al perro',
                    date: '2020-02-01',
                    done: false
                },
                {   
                    id: 2,
                    subject: 'Comprar verdura',
                    date: '2020-02-02',
                    done: false
                },
                {   
                    id: 3,
                    subject: 'Hacer una todo list',
                    date: '2020-02-02',
                    done: false
                }
                
            ]
        }
    }
}
</script>

<style lang="scss">
    .todo-body {
        width: 100%;
        padding: 2rem 1.5rem;
        background-color: #FCFCFF;
        
    }

</style>