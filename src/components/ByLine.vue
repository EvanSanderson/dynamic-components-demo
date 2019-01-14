<script>
export default {
  name: "ByLine",
  props: {
    data: {
      type: String,
      required: true,
      default: ""
    }
  }
};
</script>

<template>
	<h1> By {{ data }} </h1>
</template>


<style>
</style>
