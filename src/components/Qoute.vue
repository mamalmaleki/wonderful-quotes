<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-defualt">
      <div class="panel-body qoute">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
};
</script>

<style>
.panel-body {
  font-family: "Arizonia", cursive;
  font-size: 24px;
  color: #6e6e6e;
}

.qoute {
  cursor: pointer;
}

.qoute:hover {
  background-color: #ffe2e2;
}
</style>