<template>
  <div>
    <px-assests-table :assets="assets" />
  </div>
</template>

<script>
import api from "@/api";
import PxAssestsTable from "@/components/PxAssestsTable";

export default {
  name: "Home",
  components: { PxAssestsTable },

  data() {
    return {
      assets: [],
    };
  },
  created() {
    api.getAssets().then((assets) => (this.assets = assets));
  },
};
</script>
