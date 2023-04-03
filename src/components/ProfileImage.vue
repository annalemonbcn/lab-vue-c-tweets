<template>
  <img :src="imageUrl" class="profile" alt="profile" />
</template>

<script>
export default {
  name: 'ProfileImage',
  props: {
    imageUrl: {
      type: String,
      required: true
    }
  }
}
</script>

<style>

</style>