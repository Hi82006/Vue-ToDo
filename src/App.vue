<template>
  <div class="app">
    <h1>страница с постами</h1>
    <my-button
    @click="showDialog"
    >
      Cоздать пост
  </my-button>
    <my-dialog 
    v-model:show="dialogVisible"
    >
      <post-form
      @create="createPost"
      />
    </my-dialog>
    <post-list 
    :posts="posts"
    @remove="removePost"
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
      dialogVisible: false,
    };
  },
  methods: {
    createPost(post, second, third) {
      console.log(post)
      console.log(second)
      console.log(third)
      this.posts.push(post)
    },
    removePost(post) {
      this.posts = this.posts.filter(p => p.id != post.id)
    },
    showDialog() {
      this.dialogVisible = true
    }
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
