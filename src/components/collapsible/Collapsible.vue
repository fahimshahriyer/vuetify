<template lang="pug">
  ul(
    v-bind:class="classes"
  )
    slot
</template>

<script>
  export default {
    name: 'collapsible',

    props: {
      expand: Boolean
    },

    computed: {
      classes () {
        return {
          'collapsible': true
        }
      },

      params () {
        return {
          expand: this.expand
        }
      }
    }
  }
</script>