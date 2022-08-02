<template>
  <div>
<!--<Header />-->
    <input type="text" v-model="userId">
    <button @click="onLoadUser">Load User</button>
    <nuxt-child />
  </div>
</template>

<script>
import Header from "~/components/Header"

export default {
  component: {
    Header
  },
  data() {
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser(){
      this.$router.push("/users/" + this.userId)
    }
  },
  layout: "users"
}
</script>
