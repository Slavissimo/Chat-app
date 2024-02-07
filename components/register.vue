<script setup lang="ts">
import type { FormError, FormSubmitEvent } from '#ui/types'

const state = reactive({
    username: undefined,
    email: undefined,
    password: undefined
})

const validate = (state: any): FormError[] => {
  const errors = []
  if (!state.username) errors.push({ path: 'username', message: 'Required' })
  if (!state.email) errors.push({ path: 'email', message: 'Required' })
  if (!state.password) errors.push({ path: 'password', message: 'Required' })
  return errors
}

async function onSubmit (event: FormSubmitEvent<any>) {
  // Do something with data
  console.log(event.data)
}
</script>

<template>
  <UForm :validate="validate" :state="state" class="space-y-5" @submit="onSubmit">
    <UFormGroup label="Username" name="username">
      <UInput v-model="state.username" placeholder="Cool username" icon="i-heroicons-user-solid" />
    </UFormGroup>
    <UFormGroup label="Email" name="email">
      <UInput v-model="state.email" placeholder="you@example.com" icon="i-heroicons-envelope" />
    </UFormGroup>

    <UFormGroup label="Password" name="password">
      <UInput v-model="state.password" placeholder="*******" type="password" />
    </UFormGroup>
    <UFormGroup>
        Have an account?
      <ULink class="register-link">
        <NuxtLink to="/">Login here</NuxtLink>
        </ULink>
    </UFormGroup>
    <UButton type="submit">
      Register
    </UButton>
  </UForm>
</template>
<style scoped>
.register-link {
  color: #0293cc;
  text-decoration: underline;
}
</style>