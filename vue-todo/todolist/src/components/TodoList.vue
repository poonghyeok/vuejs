<template>
    <section>
        <transition-group name="list" tag="ul">
            <li v-for="(todoItem,index) in propsdata" :key="todoItem" class="shadow">
                <i class="checkBtn fas fa-check" aria-hidden="true"></i>
                <input type="text" v-bind:value="todoItem" class="todoItemInput" :readonly="!editOn">
                <span class="editBtn" type="button" @click="editTodo(todoItem, index)">
                    <i class="fas fa-edit" aria-hidden="true"></i>
                </span>
                <span class="removeBtn" type="button" @click="removeTodo(todoItem, index)">
                    <i class="far fa-trash-alt" aria-hidden="true"></i>
                </span>
            </li>
        </transition-group>
    </section>
</template>

<script>
export default{
    methods : {
        removeTodo(todoItem,index){
            this.$emit('removeTodo',todoItem,index);
        },
        editTodo(){
            this.editOn = !this.editOn;
        }
    },
    props : ['propsdata'],
    data(){
        return {
            editOn : false
        }
    }
}
</script>

<style scoped>
    ul{
        list-style-type: none;
        padding-left: 0px;
        margin-top: 0;
        text-align: left;
    }

    li{
        display: flex;
        min-height: 50px;
        height: 50px;
        line-height: 50px;
        margin:0.5rem 0;
        padding: 0 0.9rem;
        background: white;
        border-radius: 5px;
    }

    .checkBtn {
        line-height: 45px;
        color : #62acde;
        margin-right: 5px;
        cursor: pointer;
    }
    
    .removeBtn{
        margin-left: auto;
        color : #de4343;
        cursor: pointer;
    }
    .editBtn{
        margin-left: auto;
        color : #8ed366;
        cursor: pointer;
    }

    .list-enter-active, .list-leave-active{
        transition: all 1s;
    }
    .list-enter, .list-leave-to{
        opacity: 0;
        transform: translateY(30px);
    }

    .todoItemInput{
        border : 0px solid;
    }
</style>
