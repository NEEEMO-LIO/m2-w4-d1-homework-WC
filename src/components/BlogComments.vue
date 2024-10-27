<template>
  <div id="blogposts" class="section">
    <div v-for="(comment, index) in comments" :key="index" class="post">
      <span class="author">{{comment.author}}</span> — 
      <span class="date">{{comment.date}}</span>
      <span class="reply">REPLY</span>
      <div class="content">{{ comment.content }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlogComments',
  props: {
    comments: {
      type: Array,
      required: true
    }
  }
}
</script>

<style>
.post {
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 15px;
    margin-bottom: 15px;
    background-color: white;
}

.content {
    margin-top: 10px;
}

.reply {
    cursor: pointer;
}
</style>