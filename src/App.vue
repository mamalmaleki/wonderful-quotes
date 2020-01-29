<template>
  <div class="container">
    <app-header :qouteCount="qoutes.length" :maxQoutes="maxQoute"></app-header>
    <app-new-qoute @qouteAdded="newQoute"></app-new-qoute>
    <app-qoute-grid :qoutes="qoutes" @qouteDeleted="deleteQoute"></app-qoute-grid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: click on a Qoute to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QouteGrid from "./components/QouteGrid.vue";
import NewQoute from "./components/NewQoute.vue";
import Header from "./components/Header.vue";

export default {
  data: function() {
    return {
      qoutes: ["Just a quote to see something"],
      maxQoute: 10
    };
  },
  methods: {
    newQoute(qoute) {
      if (this.qoutes.length >= this.maxQoute) {
        return alert("please delete a qoute.");
      }
      this.qoutes.push(qoute);
    },
    deleteQoute(index) {
      this.qoutes.splice(index, 1);
    }
  },
  components: {
    appQouteGrid: QouteGrid,
    appNewQoute: NewQoute,
    appHeader: Header
  }
};
</script>

<style>
</style>
