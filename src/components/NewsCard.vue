<template>
  <div class="col mb-4">
    <a :href="url">
      <div class="card">
        <img
          :src="image"
          class="card-img-top"
          :alt="image"
          style="width: 100%; height: 400px;"
        />
        <div class="card-body">
          <h5 class="card-title">{{ shortTitle }}</h5>
          <p class="card-text">
            {{ shortDescription }}
          </p>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  name: "NewsCard",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    date: {
      type: String,
      required: true,
    },
  },
  computed: {
    shortTitle: function () {
      let shortTitle =  this.title.length > 35 ? this.title.slice(0, 35) + "..." : this.title;
      return shortTitle
    },
    shortDescription: function () {
      let shortDescription =  this.description.length > 80 ? this.description.slice(0, 80) + "..." : this.description;
      return shortDescription
    },
  },
};
</script>

<style lang="scss" scoped></style>
