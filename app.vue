<script setup lang="ts">
import { Authenticator } from "@aws-amplify/ui-vue";
import "@aws-amplify/ui-vue/styles.css";
</script>

<template>
  <div>
    <Authenticator>
      <template v-slot="{ user, signOut }">
        <h1>Hello {{ user.username }}!</h1>
        <div>
          <NuxtWelcome />
        </div>
        <button @click="signOut">Sign Out</button>
      </template>
    </Authenticator>
  </div>
</template>