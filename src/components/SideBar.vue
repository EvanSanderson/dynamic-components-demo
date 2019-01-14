<script>
import ImageGallery from "@/components/ImageGallery";
import ByLine from "@/components/ByLine";
import SavedItems from "@/components/SavedItems";

export default {
  name: "SideBar",
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
	<div class="side-bar">
		<component v-for="({type, data}, index) in modules" 
			:is="type" 
			:data="data" 
			:key="`${type}-${index}`"
		/>
	</div>
</template>

<style lang="scss" scoped>
.side-bar {
  flex: 1;
  display: flex;
  flex-direction: column;
  background: rgba(247, 125, 125, 0.2);
}
</style>
