<template>
    <button>
        {{text}}
        {{buttonIcon}}
    </button>
</template>

<script>
export default {
    props: ['text', 'icon'],

    data(){
        return {
            buttonIcon: this.icon
        }
    }
}
</script>

<style lang="scss">
    button {
        cursor: pointer;
        outline: none;
        padding: .5rem;
        border-radius: 50%;
        border: none;
        color: white;
        text-align: center;
        background-color: #F77374;
    }
</style>
