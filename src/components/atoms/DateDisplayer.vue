<template>
    <div class="date-wrapper">
        <h2>{{this.currentDate}}</h2>
        <small>{{this.year}}</small>
    </div>
        
</template>


<script>
import  moment  from "moment";

export default {

    data: () => {
        return {
            currentDate: new Date(),
            year: null
        }
    },
    methods:{
        getDate(){
            var date = moment();
            
            this.currentDate = date.format('dddd, do')
            this.year = date.format('MMMM')
        }
    },
    created(){ 
            this.getDate()
    },
 
}
</script>

<style lang="scss">
    .date-wrapper{
        display: flex;
        flex-direction: column;

        & h2 {
            font-size: 1.5rem;
            color: #20639e;
            margin-bottom: .5rem;
        }

        & small {
            font-size: .8rem;
            color: gray
        }
    
    }

</style>