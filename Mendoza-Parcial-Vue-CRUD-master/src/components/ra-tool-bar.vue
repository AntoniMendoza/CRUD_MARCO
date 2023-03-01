<template>
  <pv-toolbar
    style="background-color: rgb(1, 18, 70); color: rgb(255, 217, 91)"
  >
    <template #start>
      <h3>PEOPLE LIST</h3>
    </template>
    <template #end>
      <div class="flex-column">
        <router-link
          v-for="item in items"
          :to="item.to"
          custom
          v-slot="{ navigate, href }"
          :key="item.label"
        >
          <pv-button
            class="p-button-text text-white"
            :href="href"
            @click="navigate"
            >{{ item.label }}</pv-button
          >
        </router-link>
      </div>
    </template>
  </pv-toolbar>
</template>

<script>
export default {
  name: "RaToolBar",
  data() {
    return {
      drawer: false,
      items: [
        { label: "CHANLLENGES FOR PERSON", to: "/" },
        { label: "NEW CHALLENGE", to: "/business/challenges" },
      ],
    };
  },
};
</script>

<style scoped>

</style>
