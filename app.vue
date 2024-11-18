<script setup lang="ts">
const sleep = (ms: number) => new Promise((resolve) => setTimeout(resolve, ms))

const fakeSubmit = async (index) => {
  console.log('Form submitted', index)
  await sleep(3000)
}
</script>

<template>
  <div class="m-4">
    <FormKit type="form" @submit="fakeSubmit(1)" :actions="false">
      <FormKit
        type="text"
        label="Username"
        :validation="[['required']]"
        validation-visibility="live"
        :validation-messages="{
          matches: 'Please enter a valid Username.',
        }"
        placeholder="Enter your Username..."
      />
    </FormKit>

    <FormKit type="form" @submit="fakeSubmit(2)" :actions="false">
      <MyTextInput
        label="Username"
        :validation="[['required']]"
        validation-visibility="live"
        :validation-messages="{
          matches: 'Please enter a valid Username.',
        }"
        placeholder="Enter your Username..."
      />
    </FormKit>

    <FormKit type="form" @submit="fakeSubmit(3)" :actions="false">
      <MyTextInputBad
        label="Username"
        :validation="[['required']]"
        validation-visibility="live"
        :validation-messages="{
          matches: 'Please enter a valid Username.',
        }"
        placeholder="Enter your Username..."
      />
    </FormKit>
  </div>
</template>
