<template>
  <div class="code" :title="Obj.prop">
    {{ Obj.prop }}
  </div>
</template>

<script lang="ts">
type myType = {
  prop: string;
  val: boolean;
};
enum MY_ENUM {
  PROP = "VALUE",
}
export default {
  data() {
    return {
      Obj: { prop: "val" },
    };
  },
  mounted() {
    const testObj: myType = { prop: "val", val: false };
    const test = "testing";
    let one: string | number = 1;
    one = "one";
    testObj.prop = "";
    testObj.val = true;
    console.log(this.Obj.prop);
    console.log(testObj.prop);
    console.log(test);
    console.log(one);
    console.log({
      test: "t",
      t: 1,
      [MY_ENUM.PROP]: "t",
    });
    console.log(MY_ENUM.PROP);
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
