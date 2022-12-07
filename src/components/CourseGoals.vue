<template>
  <div>
    <goals-list :goals="filteredGoals"></goals-list>
    <add-goal @add-goal="addGoal"></add-goal>
  </div>
</template>
  
  <script>
import GoalsList from "./GoalsList.vue";
import AddGoal from "./AddGoal.vue";
import { ref, computed } from "vue";
export default {
  components: {
    GoalsList,
    AddGoal,
  },
  setup() {
    const goals = ref([]);
    //addding a computed property
    const filteredGoals = computed(function () {
      return goals.value.filter(
        (goal) => !goal.text.includes("Delhi") && !goal.text.includes("Mumbai")
      );
    });
    //adding a method in setup
    function addGoal(text) {
      const newGoal = {
        id: new Date().toISOString(),
        text: text,
      };
      goals.value.push(newGoal);
    }

    return {
      goals,
      filteredGoals: filteredGoals,
      addGoal: addGoal,
    };
    //You can use Options and composition api side by side . as other component is 
    //using optionsAPi at this time
  },
};
</script>