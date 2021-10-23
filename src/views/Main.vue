<template>
  <div class="container-fluid">
    <div class="card bg-dark text-white shadow">
      <div class="card-body">
        <PortfolioView />
      </div>
    </div>
  </div>
</template>

<script>
import PortfolioView from "@/components/PortfolioView.vue";

export default {
  name: "Main",
  components: {
    PortfolioView,
  },
};
</script>
