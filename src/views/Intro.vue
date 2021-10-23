<template>
  <div class="container">
    <div class="row mb-3">
      <div class="col-6">
        <h1 class="text-start">
          <span class="fw-bold me-3 text-white">Hey there! I'm Kenzie</span
          ><br />
          <span class="fw-bold">{{ title }}</span>
        </h1>

        <div class="card bg-dark text-white shadow mb-3">
          <div class="card-header fw-bold h4">About me</div>
          <div class="card-body text-start">
            <div class="mb-3">
              I am currently pursuing a bachelor's degree in Computer Science at
              Oregon State Univeristy. <span class="beaver">GO BEAVS!</span> I
              started my journey here at OSU in 2018 and jumped right into web
              development. I was offered a job at Oregon State Univeristy's
              Ecampus program. I am still employed there as of today going on my
              third year being a web developer.
            </div>
            <div class="mb-3">
              My tasks as a web developer consists of following AGILE software
              development methodology, developing educational interactives with
              the Vue framework, maintaining front-end web application, and
              designing illustrations as SVGs in Adobe Illustrator. Also, I have
              experience with SQL and database design.
            </div>
            <div class="mb-3">
              I have always had a passion for technology. On my free time, I
              like to develop simple games that are easily played through the
              browser. Continue on to see my work by clicking the button below!
            </div>
            <div class="text-center">
              <router-link
                :to="{ name: 'Main' }"
                class="btn btn-lg btn-purple fw-bold text-white"
                >Portfolio <i class="bi bi-journal-code h4"></i
              ></router-link>
            </div>
          </div>
        </div>
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

.beaver {
  color: #d73f09;
  font-weight: bold;
}
</style>
