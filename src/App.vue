<template>
  <div class="app">
    <JobList :jobs = "jobs"/>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref} from "vue";
import JobList from "./components/JobsList.vue";
import Job from "./types/Job";

export default defineComponent({
  name: "App",
  components: {JobList},
  setup() {
    const jobs = ref<Job[]>([
      {title: "worker",location: "viet nam",salary: 300000,id: "1"},
      {title: "worker2",location: "viet nam",salary: 400000,id: "2"},
      {title: "worker3",location: "viet nam",salary: 320000,id: "3"},
      {title: "worker4",location: "viet nam",salary: 310000,id: "4"},
    ]);
    return { jobs };
  },

  methods: {
    
  },
});
</script>

<style></style>
