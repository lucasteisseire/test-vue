<template>
  <div>
    <h1>Reusable Component Input Test</h1>
    <div class="container">
      <div class="image">
        <img src="../assets/ss.jpg" />
      </div>
      <div>
        <p class="name">lucas is</p>
        <Input />
      </div>
      <div>
        <p class="hours-old">hours old</p>
      </div>
    </div>
  </div>
</template>

<script>
import Input from "~/components/Input.vue";

export default {
  components: {
    Input
  }
};
</script>

<style>
h1 {
  text-transform: uppercase;
  margin: 40px 0px 0px 40px;
}
input {
  outline: none;
  appearance: none;
  border: none;
  color: lightgray;
  font-weight: bold;
  padding-bottom: 8px;
  border-bottom: 1px solid grey;
}
input:focus {
  color: black;
  font-weight: bold;
  border-bottom: 1px solid blue;
}
img {
  max-width: 100%;
  max-height: 100%;
  border-radius: 40px;
}

.name {
  text-transform: uppercase;
  font-size: 10px;
  text-align: left;
}
.hours-old {
  font-size: 8px;
  margin: 20px 0 0 10px;
}
.container:focus-within .image {
  border: 3px solid blue;
  color: blue;
}
.container:focus-within .name {
  color: blue;
}
.container {
  margin: 40px auto;
  min-height: 100vh;
  display: flex;
  text-align: center;
}
.image {
  margin-left: 40px;
  margin-right: 20px;
  width: 40px;
  height: 40px;
  border-radius: 40px;
}
</style>
