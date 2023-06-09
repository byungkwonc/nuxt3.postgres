<template>
    <div>
    <!-- font-weight: bold; font-size: 1.875rem; -->
    <h1 class="font-bold text-3xl">Home</h1>
    <div v-if="pending">Loading..</div>
      <template v-else>
        <div v-if="error">Sorry, error occured.</div>
        <div v-else>{{ data }}</div>
      </template>

      <div>{{ userStore.user }}</div>

      <button @click="refresh()">Refresh</button>
      <button @click="userStore.save({ email: 'peterkimzz69@gmail.com' })">Increment</button>
    </div>
  </template>