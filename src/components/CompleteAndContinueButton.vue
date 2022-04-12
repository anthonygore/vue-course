<script setup>
import { useRouter } from 'vue-router'
const router = useRouter()
const props = defineProps({
  courseId: {
    type: String,
    required: true
  },
  lessonId: {
    type: String,
    required: true
  }
})
function completeAndContinue () {
  router.push(`/courses/${props.courseId}/lessons/${props.lessonId}`)
}
</script>

<template>
  <button class="button primary" @click="completeAndContinue">
    Complete and continue
  </button>
</template>
