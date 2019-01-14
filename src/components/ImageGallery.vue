<script>
export default {
  name: "ImageGallery",
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
	<div class="gallery">
		<div v-for="item in data" :key="item" class="gallery__container">
			<img :src="item" />
		</div>
	</div>
</template>

