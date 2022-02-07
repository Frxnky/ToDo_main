<template>

  <div>
    
    <FY @Input="validate"></FY>
    <Fx :F1="F1"></Fx>
    </div>
    
</template>

<script>
import FY from "../components/FY.vue"
import Fx from "../components/Fx.vue"
export default {
  data: () => ({
    F1: [],
  }),
components :{FY,Fx},
F1: "Input",
  methods: {
    validate(select, name) {
      this.F1.push({
        name: select + " : " + name,
      });
    },
  },
};
</script>

<style>

</style>