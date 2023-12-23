<template>
    <button v-on="$listeners" v-bind:type="type" class="btn btn--outlined">
        <slot></slot>
    </button>
</template>

<script>
    export default {
        name: 'MyButton',
        props: {
            type: {
                type: String,
                default: 'button',
            },
            outlined: {
                type: Boolean,
                default: false
            }
        },
    }
</script>

<style lang="scss" scoped>
.btn {
    display: inline-block;
    border: 1px solid transparent;
    padding: 10px 20px;
    margin: 5px 10px;
    font-size: 18px;
    background: #FF6620;
    color: #fff; 
    min-width: 220px;
    padding: 8px 15px;

    &--outlined {
        background: none;
        border: 1px solid #FF6620;
        color: #FF6620;
    }
}

</style>