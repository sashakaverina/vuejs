<template>
    <div id="tasks">
        <button class="btn round-icon" @click="addTask('My new task', 'Desc')">+</button>
        <TaskCard 
        v-for="(task, index) in tasks"
        :key="index"
        :title="task.title"
        :description="task.description"
        :done="task.done"
        >

        </TaskCard>

        <p v-if="tasks.length === 0">You don't have any tasks yet</p>
    </div>


    
</template>

<script>
import TaskCard from './TaskCard.vue'

export default {
   components: {TaskCard },


  data() {
  return {
    tasks: [],
  };
},

methods: {
    addTask(title, description, done = false){
        this.tasks.unshift({title, description,done});
    },
  },
};


</script>
