<template>
  <main>
    <div class="main-heading">
      <h1>Storywriter</h1>
    </div>
    <div class="main-teaser">
      <div>
        Welcome to Storywriter! The feature-rich editor so you can compose your stories however you like.
        <hr/>
        To start, click on the "New Story" button below. We'll guide you through some basics you'll need to get started.
      </div>
    </div>
    <div class="buttons">
      <button @click="newStory">
        New Story
      </button>

      <button @click="openSettings">
        Settings
      </button>
    </div>
  </main>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'
  import './Application.less'

  export default defineComponent({
    data() {
      return {
        variable: 0
      }
    },
    methods: {
      newStory() {
        this.variable++

        console.log("New story: " + this.variable);
      },
      openSettings() {
        this.variable--

        console.log("Settings opened: " + this.variable);
      },
    },
  })
</script>
