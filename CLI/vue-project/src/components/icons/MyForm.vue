<template>
  <!--
    <div style="text-align: center;">
        <P> hello my name is {{ name }}, <br>
            I am {{ age }} years old,<br>
            and I am a student at {{ college }} </P>

    <div v-if="age > 18">
        <h3> Hello World</h3>
    </div>
    <p v-show="name ==! abdullah">
        his name is not abdullah
    </p>
   <ol class="names">
    <li v-for="(friend, index) in friends" :key="index">
        {{ friend }}
    </li>
   </ol>
   <input type=" text" :value="name">  
   <img :src="logo" :alt="alt"> 
    </div>-->

  <div>
    <div class="input-group mb-3">
      <input
        type="text"
        class="form-control"
        :placeholder="placeholder"
        aria-label="new Task"
        :value="task"
      />
      <button
        class="btn btn-primary my-3"
        type="button"
        id="button-addon2"
        @click="tasks.push(task)"
      >
        Add Task
      </button>
    </div>

    <ol class="list-group">
      <li
        class="list-group-item"
        aria-current="true"
        v-for="(task, index) in tasks"
        :key="index"
      >
        {{ task }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      /*name: "abdullah",
                friends:["Ahmed", "Ali","Mohammed"],
                age: 25,
                college: "FEE",*/

      tasks: ["get milk", "read", "write", "Go to the Gym", "Kill the cat"],
      task:"consider it a new task",
      placeholder: "add a new task",
    };
  },
};
</script>

<style></style>
