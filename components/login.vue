<script setup lang="ts">
import type { FormError, FormSubmitEvent } from '#ui/types'

const state = reactive({
  email: undefined,
  password: undefined
})

const validate = (state: any): FormError[] => {
  const errors = []
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
    <UFormGroup label="Email" name="email">
      <UInput v-model="state.email" placeholder="you@example.com" icon="i-heroicons-envelope" />
    </UFormGroup>

    <UFormGroup label="Password" name="password">
      <UInput v-model="state.password" placeholder="*******" type="password" />
    </UFormGroup>
    <UFormGroup>
        Don't have an account?
      <ULink class="register-link">
        <NuxtLink to="/register">Register here</NuxtLink>
        </ULink>
    </UFormGroup>
    <UButton type="submit">
      Login
    </UButton>
  </UForm>
</template>
<style scoped>
.register-link {
  color: #0293cc;
  text-decoration: underline;
}
</style>