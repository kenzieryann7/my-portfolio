<template>
  <div class="container">
    <div class="row mb-3">
      <div class="col-6">
        <h1 class="text-start">
          <span class="fw-bold me-3 text-white">Hi, I'm Kenzie Noggle</span
          ><br />
          <span class="fw-bold">{{ title }}</span>
        </h1>

        <div class="card bg-dark text-white shadow mb-3">
          <div class="card-header fw-bold">{{ cardTitle }}</div>
          <div class="card-body">{{ cardBody }}</div>
        </div>
        <router-link :to="{ name: 'Main' }" class="btn btn-primary fw-bold">{{
          buttonLabel
        }}</router-link>
      </div>

      <div class="col-6">
        <div class="card bg-dark text-white shadow">
          <div class="card-body">
            <img
              src="@/assets/intro-me.png"
              class="img-fluid"
              alt="Personal Image"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import content from "@/data/content-intro.json";

// @ is an alias to /src
//import Card from "@/components/Card.vue";

export default {
  name: "Intro",
  data() {
    return {
      course: process.env.VUE_APP_COURSE,
      title: process.env.VUE_APP_TITLE,
      cardTitle: content.cardTitle,
      cardBody: content.cardBody,
      buttonLabel: content.buttonLabel,
      buttonView: content.buttonView,
    };
  },
};
</script>

<style scoped>
img {
  opacity: 0.8;
}
</style>
