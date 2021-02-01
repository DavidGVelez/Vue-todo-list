<template>
    <li>
        <label>
            <input type="checkbox"
                @change="changeTodoStatus"
                :checked="done"
                :name="item.id" 
                :id="item.id"/>
            <span :class="[this.done ? 'done' : null]">{{item.subject}}</span>
        </label>
        <div class="action-wrapper">
            <Button
            @click="editTodo">
                <PencilOutlineIcon></PencilOutlineIcon>
            </Button>
           
            <Button
            @click="deleteTodo">
                <TrashCanOutlineIcon></TrashCanOutlineIcon>
            </Button>
        </div>
      
        
       
    </li>
</template>

<script>
    import PencilOutlineIcon from "vue-material-design-icons/PencilOutline"
    import TrashCanOutlineIcon from "vue-material-design-icons/TrashCanOutline"

export default {
    props: ['item'],
    components: {PencilOutlineIcon,TrashCanOutlineIcon},

    data(){
        return {
            done: this.item.done,
        }
    },
    methods: {
        changeTodoStatus() {
            this.done = !this.done
        },
        deleteTodo(){
            console.log('delete')
        },
        editTodo(){
            console.log('edit')
        }
    },
}
</script>

<style lang="scss">
    li{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 0;
    }
    input[type="checkbox"]{
        margin: 0;
        margin-right: 1rem;
       
    }
    .done {
        text-decoration: line-through;
    }
    .action-wrapper{
        display: flex;
        
        & Button{
            margin-right: 2rem
            
        }
        & :last-child{
            margin-right: 0rem;
        }
    }
</style>