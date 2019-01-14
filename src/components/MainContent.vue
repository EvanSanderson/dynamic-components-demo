<script>
import ImageGallery from "@/components/ImageGallery";
import ByLine from "@/components/ByLine";
import SavedItems from "@/components/SavedItems";

export default {
  name: "MainContent",
  components: {
    ImageGallery,
    ByLine,
    SavedItems
  },
  props: {
    modules: {
      type: Array,
      required: true,
      default: () => []
    }
  }
};
</script>

<template>
	<div class="main-content">
		<component v-for="({type, data}, index) in modules" 
			:is="type" 
			:data="data" 
			:key="`${type}-${index}`"
		/>
	</div>
</template>

<style lang="scss" scoped>
.main-content {
  flex: 2;
  display: flex;
  flex-direction: column;
  background: rgba(144, 144, 219, 0.5);
}
</style>
