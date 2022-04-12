<script setup>
defineProps({
  course: {
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
            :to="{ name: 'course', params: { courseId: course.id } }"
          >
            {{ course.title }}
          </router-link>
        </h2>
      </div>
      <p>
        <router-link
          class="no-underline cursor-pointer"
          :to="{ name: 'course', params: { courseId: course.id } }"
        >
          {{ course.description }}
        </router-link>
      </p>
    </div>
  </section>
</template>
