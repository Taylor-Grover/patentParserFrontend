<template>
  <div>
    <h1>Reference: {{ referenceNum }}</h1>
    <div>
      <div v-for="ref in referenceList" :key="ref._id" class="singleReference">
        <b>Description: </b> <span>{{ ref.description }}</span
        ><br />
        <b>Paragraph Referenced: </b><span>{{ ref.paragraphReferenced }}</span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Reference",
  props: {
    referenceList: Object,
    referenceNum: Number,
  },
};
</script>
<style>
.singleReference {
  border-radius: 8px;
  margin: 8px 0 8px 0;
  padding: 8px;
  font-size: 20px;
  border: 4px solid rgb(77, 73, 73);
}
</style>