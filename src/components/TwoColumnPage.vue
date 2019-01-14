<script>
import MainContent from "@/components/MainContent";
import SideBar from "@/components/SideBar";

export default {
  name: "TwoColumnPage",
  components: {
    MainContent,
    SideBar
  },
  props: {
    slots: {
      type: Array,
      required: true,
      default: () => []
    }
  }
};
</script>

<template>
<main class="page">
	<component v-for="({name, modules}, index) in slots" :is="name" :modules="modules" :key="`${name}-${index}`"/>
</main>
</template>

<style lang="scss" scoped>
.page {
  display: flex;
}
</style>
