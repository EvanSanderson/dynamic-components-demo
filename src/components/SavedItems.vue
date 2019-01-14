<script>
export default {
  name: "SavedItems",
  props: {
    data: {
      type: Array,
      required: true,
      default: () => []
    }
  }
};
</script>

<template>
	<ul>
		<li v-for="item in data" :key="item">
			{{item}}
		</li>
	</ul>
</template>

