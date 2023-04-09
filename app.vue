<template>
  <main class="flex bg-white">
    <Sidebar />
    <NuxtPage />
  </main>
</template>

<script>
useHead({
  title: "Dashboard",
  meta: [{ name: "description", content: "My amazing site." }],
  bodyAttrs: {
    class: "test",
  },
  script: [{ innerHTML: "console.log('Hello world')" }],
});
import Sidebar from "@/components/Sidebar.vue";
export default {
  name: "Dashboard",
  components: { Sidebar },
  data() {
    return {
      showSidebar: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.showSidebar = !this.showSidebar;
    },
  },
};
</script>
