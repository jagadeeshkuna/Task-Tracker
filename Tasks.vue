<template>
<div>
 <div  :key="task.id" v-for="task in tasks">
         <Task :task="task"/>
         <h3>{{task.text}}</h3>
<p>{{task.day}}</p>
</div>
</div>
</template>

<script>
import Task from './Task'
export default{
    name: 'Tasks',
    props: {
        tasks: Array,
        },
        components: {
            Task,
        }

}
</script>

<style>
.task {
    background: #f4f4f4;
    margin: 5px;
    padding: 10px 20px;
    cursor: pointer;
}
.task.remainder {
    border-left: 5px solid black;
}
.task h3 {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>