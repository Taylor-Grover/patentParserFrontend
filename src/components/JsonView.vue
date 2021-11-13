<template>
  <div class="mainView">
    <div v-for="k in keys" :key="k._id">
      <Reference :referenceList="referenceJson[k]" :referenceNum="k" />
      <br />
    </div>
  </div>
</template>
<script>
import jsonFile from "../../references.json";
import Reference from "./Reference.vue";
export default {
  name: "JsonView",
  components: {
    Reference,
  },
  data() {
    return {
      hi: "asdf",
      referenceJson: jsonFile,
      keys: [],
    };
  },
  computed: {
    json: function () {
      return this.referenceJson;
    },
  },
  methods: {},
  beforeMount() {
    this.keys = Object.keys(this.referenceJson);
    // for (let i = 0; i < this.keys.length; i += 1) {
    //     this.referenceJson[keys[i]].referenceNum
    // }
    console.log(this.keys);
  },
};
</script>
<style>
.mainView {
  margin: 0 48px 0 48px;
}
</style>