<template>
  <div class="app">
    <post-form
    @create="createPost"
    />
    <post-list 
    :posts="posts"
    />
    
  </div>
</template>
<script>
import PostForm from '@/components/PostForm';
import PostList from '@/components/PostList';

export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        { id: 1, title: "Javascript", body: "Описание поста" },
        { id: 2, title: "Javascript", body: "Описание поста" },
        { id: 3, title: "Javascript", body: "Описание поста" },
      ],
    };
  },
  methods: {
    createPost(post, second, third) {
      console.log(post)
      console.log(second)
      console.log(third)
      this.posts.push(post)
    },
  },
  
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}

</style>
