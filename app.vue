<template>
  <main class="flex bg-white">
    <Sidebar />
    <NuxtPage />
  </main>
</template>

<script>
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
