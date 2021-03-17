<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :id="post.id"
      :key="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnail-image="post.thumbnailUrl"
    />
  </section>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'

export default {
  components: {
    PostPreview,
  },
  data() {
    return {
      posts: [
        {
          title: 'A New Beginning',
          previewText: "This will be awesome, don't miss it!",
          thumbnailUrl:
            'https://images.unsplash.com/photo-1615910388452-fdad95ebb038?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1000&q=80',
          id: 'a-new-beginning',
        },
        {
          title: 'A Second Beginning',
          previewText: "This will be awesome, don't miss it!",
          thumbnailUrl:
            'https://images.unsplash.com/photo-1615729947596-a598e5de0ab3?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=934&q=80',
          id: 'a-second-beginning',
        },
      ],
    }
  },
}
</script>

<style scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
