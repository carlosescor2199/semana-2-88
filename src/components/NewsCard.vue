<template>
  <div class="col mb-4">
    <a :href="url">
        <div class="card">
      <img :src="image" class="card-img-top" :alt="image" style="width: 100%; height: 300px;"/>
      <div class="card-body">
        <h5 class="card-title">{{ title }}</h5>
        <p class="card-text">
          {{ description }}
        </p>
        <span>{{ author ? author : 'Anonimo' }} - {{ date }}</span>
      </div>
    </div>
    </a>
  </div>
</template>

<script>
export default {
    name: 'NewsCard',
    props: {
        author: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true
        },
        url: {
            type: String,
            required: true
        },
        image: {
            type: String,
            required: true
        },
        date: {
            type: String,
            required: true
        },

    }
};
</script>

<style lang="scss" scoped></style>
