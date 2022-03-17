<template>
  <div class="p-2" >
    <a href="/detail" @click="setCommit()">
      {{sha}}
    </a>
  </div>
</template>

<script>
export default {
  name: 'Commit',
  props: {
    sha: String
  },
  methods: {
    setCommit() {
      localStorage.setItem("currentCommit",this.sha)
    },
  },
}
</script>