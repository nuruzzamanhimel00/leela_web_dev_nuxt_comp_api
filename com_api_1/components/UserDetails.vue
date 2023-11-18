<template>
  <div>
    <div>
      <hr />
      <h1>User Detaisl component---------------</h1>
      <h4>Name: {{ user.name }}</h4>
      <h4>age: {{ user.age }}</h4>
      <button @click="changeDetials">Change detials</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "UserDetails",
  props: ["userDetails"],
  setup(props) {
    const user = reactive(props.userDetails);
    function changeDetials() {
      user.name = "change name XXXX";
      user.age = "change age 20";
    }
    return {
      user,
      changeDetials,
    };
  },
};
</script>
<!-- <script setup></script> -->

<style lang="scss" scoped></style>
