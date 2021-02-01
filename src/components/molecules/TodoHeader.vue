<template>
    <header>
     
        <DateDisplayer></DateDisplayer>
        
       
        <Button>
            <PlusIcon></PlusIcon>
        </Button>
       
    </header>
</template>

<script>
import PlusIcon from "vue-material-design-icons/Plus";

import Button from "../atoms/Button";
import DateDisplayer from "../atoms/DateDisplayer";

export default {
    components: {
        Button, DateDisplayer, PlusIcon
    }
}
</script>

<style lang="scss"> 
    header{
        width: 100%;
        display: flex;
        padding: 2rem 1.5rem;
        background-color: #FCFCFF;
        border-bottom: 1px solid #f0eded;
        justify-content: space-between;
    }
</style>