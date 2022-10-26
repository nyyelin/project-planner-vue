<template>
  <div class="project">
    <div class="flexing">
      <div>
        <h3 @click="showDetailToogle">{{ project.title }}</h3>
      </div>
      <div>
        <span class="material-icons" @click="deleteProject"> delete </span>
        <span class="material-icons"> edit </span>
        <span class="material-icons"> done </span>
      </div>
      
    </div>
    <p v-if="detail === true">{{ project.detail }}</p>
  </div>
</template>

<script>
export default {
  props: ["project"],
  data() {
    return {
      detail: false,
    };
  },

  methods: {
    showDetailToogle() {
        
      this.detail = !this.detail;
    },
  },
};
</script>

<style>
.project {
  padding: 20px;
  background-color: white;
  margin: 14px 10px;
  box-shadow: 4px 5px 20px rgb(180, 179, 179);
  border-radius: 5px;
  border-left: 5px solid crimson;
}
h3 {
  color: indigo;
  cursor: pointer;
}
.flexing {
  display: flex;
  justify-content: space-between;
  align-items: center; /** vertical **/
}
span{
    margin-left: 15px;
    cursor: pointer;
}
span:hover{
    color: #777;
}
</style>