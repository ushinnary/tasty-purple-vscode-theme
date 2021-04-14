<template>
  <div class="code" :title="Obj.prop">
    {{ Obj.prop }}
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      Obj: { prop: "val" },
    };
  },
  mounted() {
    const testObj = { prop: "val", val: false };
    const test = "testing";
    testObj.prop = "";
    testObj.val = true;
    console.log(this.Obj.prop);
    console.log(testObj.prop);
    console.log(test);
  },
  methods: {
    test(params) {
      console.log(params);
      return true;
    },
  },
};
</script>

<style scoped lang="scss">
#id {
  .class {
    color: red;
  }
}
</style>
