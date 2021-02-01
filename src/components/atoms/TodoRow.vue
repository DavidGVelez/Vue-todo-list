<template>
    <li>
        <transition name="fade" mode="out-in">
            <div v-if="!edit" class="row-wrapper" :key="1">
                <label>
                    <input type="checkbox"
                        @change="changeTodoStatus"
                        :checked="done"
                        :name="item.id" 
                        :id="item.id"/>
                        <span :class="[this.done ? 'done' : null]">{{item.subject}}</span>
                </label>
                <div class="action-wrapper">
            
                    <PencilOutlineIcon
                        class="button"
                        @click="toogleEdit">
                    </PencilOutlineIcon>
            
                    <TrashCanOutlineIcon
                        class="button"
                        @click="toogleDelete">
                    </TrashCanOutlineIcon>
            
                </div>
            </div>
            <div v-else class="row-wrapper" :key="2">

                <input type="text" name="subject" :id="item.id" :value="item.subject">

                <div class="action-wrapper">
            
                    <CheckIcon
                        class="button"
                        @click="editTodo">
                    </CheckIcon>
                    
                </div>
            </div>
        </transition>
    </li>
</template>

<script>
    import PencilOutlineIcon from "vue-material-design-icons/PencilOutline"
    import TrashCanOutlineIcon from "vue-material-design-icons/TrashCanOutline"
    import CheckIcon from "vue-material-design-icons/Check"

export default {
    props: ['item'],
    components: {PencilOutlineIcon,TrashCanOutlineIcon,CheckIcon},

    data(){
        return {
            done: this.item.done,
            edit: false
        }
    },
    methods: {
        changeTodoStatus() {
            this.done = !this.done
        },
        toogleDelete(){
            console.log('delete')
        },
        toogleEdit(){
            this.edit = !this.edit
        },
        editTodo(){
            console.log('edited');
            this.toogleEdit();
        },
        deleteTodo(){
            console.log('deleted'),
            this.toogleDelete();
        }
    },
}
</script>

<style lang="scss">

    .fade-enter-active,
    .fade-leave-active {
    transition: opacity 0.5s ease;
    }

    .fade-enter-from,
    .fade-leave-to {
        opacity: 0;
    }

    .row-wrapper{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 0;
    }
    input[type="checkbox"]{
        margin: 0;
        margin-right: 1rem;
       
    }
    input[type="text"]{
        padding:0;
        border: none;
        border-bottom: 1px solid black;
    }
    .done {
        text-decoration: line-through;
    }
    .action-wrapper{
        display: flex;
        
        & .button{
            margin-right: 2rem;
            cursor: pointer;
            outline: none;
            padding: .5rem;
            border-radius: 50%;
            border: none;
            color: white;
            text-align: center;
            background-color: #F77374;
            
        }
        & :last-child{
            margin-right: 0rem;
        }

    

}
</style>