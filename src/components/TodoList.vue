<template>
    <ul class="todo-main">
        <TodoItem v-for="item in todos" :key="item.id" :todo="item"/>
    </ul>
</template>

<script>
import TodoItem from './TodoItem.vue'
export default {
    name: 'TodoList',
    components: { TodoItem },
    data() {
        return {
            todos: [
                { id: '001', title: '抽烟', done: true },
                { id: '002', title: '喝酒', done: false },
                { id: '003', title: '烫头', done: true },
            ]
        }
    },
}
</script>

<style scoped>
.todo-main {
    margin-top: 15px;
    margin-left: 0px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding: 0px;
}

.todo-empty {
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
}
</style>