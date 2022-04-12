<script setup>
defineProps({
  courseId: {
    type: String,
    required: true
  },
  num: {
    type: Number,
    required: true
  },
  lesson: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <section class="summary">
    <div>
      <div class="title">
        <h2>
          <router-link
            class="no-underline cursor-pointer"
            :to="'/courses/' + courseId + '/lessons/' + lesson.id"
          >
            {{ num }}. {{ lesson.title }}
          </router-link>
        </h2>
      </div>
      <p>
        <router-link
          class="no-underline cursor-pointer"
          :to="'/courses/' + courseId + '/lessons/' + lesson.id"
        >
          {{ lesson.description }}
        </router-link>
      </p>
    </div>
  </section>
</template>
