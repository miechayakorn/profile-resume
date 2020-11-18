<template>
  <div id="app">
    <div class="container mt-3">
      <h3 class="animated fadeInUp">Profile</h3>
      <profile-card></profile-card>
    </div>

    <div
      class="section p-1 mb-4 animated fadeInLeftBig delay-1s"
      style="background-color: #3D3731;"
    >
      <div class="container">
        <h3>Project</h3>
      </div>
    </div>

    <div class="container">
      <article class="col-md-12">
        <div class="row">
          <div class="container">
            <div class="card-deck mb-4">
              <div
                class="col-12 col-md-4 mb-md-3"
                v-for="(project, index) in projects"
                :key="index"
              >
                <card :project="project"></card>
              </div>
            </div>
          </div>
        </div>
      </article>
    </div>
  </div>
</template>

<script>
import axios from "axios";

import ProfileCard from '@/components/ProfileCard'
// const Card = () => import("./components/Card");
import Card from '@/components/Card'

export default {
  name: "app",
  components: {
    ProfileCard,
    Card,
  },
  data() {
    return {
      projects: null
    };
  },
  async mounted() {
    const urlProject =
      "https://script.google.com/macros/s/AKfycbynRlK1sysszgfiSj095HOfjF9yWIkEWQ_xunJfKyJw0qZD5EA2/exec?path=/product";
    await axios.get(urlProject).then(res => {
      this.projects = res.data.items;
    });
    console.log(urlProject);
    console.log(this.projects);
  }
};
</script>

<style>
body {
  background: linear-gradient(
    to left bottom,
    #ffd168,
    #ffc369,
    #ffb56d,
    #ffa973,
    #ff9d79,
    #fc937f,
    #f1838b,
    #e47c90
  );
  font-family: "Exo", sans-serif;
  color: #fff;
}

h1,
h2,
h3 {
  font-family: "Exo", sans-serif;
  text-transform: uppercase;
  font-weight: 200;
}

footer {
  background-color: #dfe0df;
  position: fixed;
  height: 60px;
  bottom: 0;
  width: 100%;
}

/* --------------------------------------------------------------- */

.sidenav {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
  text-align: center;
}

.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #f1f1f1;
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

@media screen and (max-height: 450px) {
  .sidenav {
    padding-top: 15px;
  }

  .sidenav a {
    font-size: 18px;
  }
}
</style>
