<template>
  <div class="tweet">
    <ProfileImage :imageUrl="image" />

    <div class="body">
      <div class="top">
        <User :user="userData" />
        <Timestamp :time="timestamp" />
      </div>

      <Message :message="message"/>
      
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue'
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Actions from './Actions.vue';

export default{
  name: 'Tweet',
  props: {
    image: {
      type: String,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    handle: {
      type: String,
      required: true
    },
    timestamp: {
      type: String,
      required: true
    },
    message: {
      type: String,
      required: true
    }
  },
  computed: {
    userData() {
      return {
        name: this.name,
        handle: this.handle
      }
    }
  },
  components: {
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
