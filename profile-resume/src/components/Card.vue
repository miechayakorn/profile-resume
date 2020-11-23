<template>
  <div class="card card-blog animated fadeInUp delay-2s">
    <div class="card-image">
      <a :href="project.URL" target="_blank">
        <img class="img" :src="project.Image" />
      </a>
      <div class="ripple-cont"></div>
    </div>
    <div class="table">
      <h6 class="text-success">
        <i class="fa fa-university"></i> {{ project.Course }}
      </h6>
      <h4 class="card-caption">
        {{ project.Name }}
      </h4>
      <p class="card-description">
        {{ project.Description }}
      </p>
      <div v-if="project.Button != `can't show`" class="col text-center">
        <a :href="project.URL" target="_blank">
          <button
            class="btn btn-github"
            style="background-color: #554488; color: #f5f5f5"
          >
            {{ project.Button }}
          </button>
        </a>
      </div>
      <div v-else class="col text-center">
        <button
          class="btn btn-github"
          style="background-color: #1e2327; color: #f5f5f5"
        >
          {{ project.Button }}
        </button>
      </div>
      <div class="ftr">
        <div class="author">
          <p class="card-text">
            <small class="text-muted">{{ project.Year }}</small>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "card",
  props: {
    project: {},
  },
};
</script>
