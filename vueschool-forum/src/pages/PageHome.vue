<template>

  <div class="col-full">
    <h1>Welcome to Forum</h1>
    <ThreadList :threads="threads"/>
  </div>

</template>

<script>
import sourceData from '@/data'
import ThreadList from '@/components/ThreadList'

console.log(sourceData)

export default {
  components: {
    ThreadList
  },

  data () {
    return {
      threads: Object.values(sourceData.threads),
      posts: sourceData.posts,
      users: sourceData.users
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
