<script setup>

import * as Sentry from "@sentry/vue"

const user = {}
const post = {
  id: 1,
  title: 'Hello world',
  body: 'Blah blah blah'
}

Sentry.setContext("post", {
  id: post.id,
  postTitle: post.title
})
Sentry.setTag("randomTag", "random-tag")

const makeToast = () => {
  sliceCheese()
}

const testAlert = () => {
  throw new Error("Error while trying to test the alert")
}

</script>

<template>
  <div>
    <h1 class="text-4xl">About</h1>
    <button @click="user.email.send()">Send email</button>
    <button @click="makeToast">Make toasts</button>
    <button @click="testAlert">Test alert</button>
  </div>
</template>
