<template>
  <div>
    <post-form 
      @create="createPost"
    />
    <post-list
      :many="many"
    />
    
  </div>
</template>

<script>
import PostForm from '@/components/PostForm'
import PostList from '@/components/PostList'

export default {
  components: {
    PostForm, PostList
  },

  data() {
    return {
      many: [
      { id: 1, title: "Abdulaziz", body: "Sobirjonov" },
      { id: 2, title: "Abdulaziz 1", body: "Sobirjonov 1" },
      { id: 3, title: "Abdulaziz 2", body: "Sobirjonov 2" },
    ],
    }
  },
  
  methods: {
    createPost(post) {
      this.many.push(post)
    }
  }
}
</script>


<style>
.posts {
  border: 1px solid teal;
  margin-bottom: 15px;
  margin-top: 15px;
}
</style>