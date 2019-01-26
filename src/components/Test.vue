<template lang="html">
  <div>
    <div class="container">
      <div class="row p-5">
        <div class="col-md-5">
          <div class="card">
            <div class="card-body">
              <form v-on:submit.prevent="addTask()">
                <div class="form-group">
                  <input type="text" v-model="newTask.title" class="form-control" placeholder="Task title">
                </div>
                <div class="form-group">
                  <textarea rows="11" cols="80" v-model="newTask.description" class="form-control" placeholder="Task description"></textarea>
                </div>
                <button type="submit" class="btn btn-dark btn-block">Add task</button>
              </form>
            </div>
          </div>
        </div>
        <div class="col-md-7">
          <table class="table table-bordered">
            <thead>
              <tr>
                <th>Task</th>
                <th>Description</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="task in tasks">
                <td>{{task.title}}</td>
                <td>{{task.description}}</td>
                <td>
                  <button type="button" class="btn btn-danger" v-on:click="deleteTask(task)">Delete</button>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data(){
    return {
      tasks: [],
      newTask: {}
    }
  },
  methods: {
    addTask(){
      if(this.newTask === {}){
        console.log('jsadlñkfjlñaskj')
      }
      this.tasks.push(this.newTask);
      this.newTask = {};
    },
    deleteTask(task){
      this.tasks.splice(this.tasks.indexOf(task), 1);
    }
  }
}
</script>

<style lang="css" scoped>

</style>
