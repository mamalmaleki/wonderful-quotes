<template>
  <div class="row">
    <app-qoutes
      v-for="(qoute, index) in qoutes"
      :key="index"
      @click.native="deleteQoute(index)"
    >{{qoute}}</app-qoutes>
  </div>
</template>

<script>
import Qoute from "./Qoute.vue";
export default {
  props: ["qoutes"],
  methods: {
    deleteQoute(index) {
      this.$emit("qouteDeleted", index);
    }
  },
  components: {
    appQoutes: Qoute
  }
};
</script>