<template>
  <div>
    <section v-show="inProgressAssignments.length">
      <h2>Todo Assignments</h2>
      <ul>
        <li v-for="assignment in inProgressAssignments" :key="assignment.id">
          <label>
            <input type="checkbox" v-model="assignment.complete"> {{ assignment.name }}
          </label>
        </li>
      </ul>
    </section>
    <section v-show="completedAssignments.length">
      <h2>Completed Assignments</h2>
      <ul>
        <li v-for="assignment in completedAssignments" :key="assignment.id">
          <label>
            <input type="checkbox" v-model="assignment.complete"> {{ assignment.name }}
          </label>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      assignments: [
        {
          id: 1,
          name: 'Task 1',
          complete: false
        },
        {
          id: 2,
          name: 'Task 2',
          complete: false
        },
        {
          id: 3,
          name: 'Task 3',
          complete: false
        },
      ]
    }
  },
  computed: {
    completedAssignments() {
      return this.assignments.filter(assignment => assignment.complete)
    },
    inProgressAssignments() {
      return this.assignments.filter(assignment => !assignment.complete)
    }
  }
}
</script>

<style scoped>
.text-green {
  color: green;
}

.text-red {
  color: red;
}
</style>