<template>
  <div class="m-4">
    <FormKit
      type="text"
      label="Username"
      :validation="[
        ['required'],
        ['length', 3, 20],
        ['matches', /^[A-Za-z0-9\_]+$/],
      ]"
      validation-visibility="live"
      :validation-messages="{
        matches: 'Please enter a valid Username.',
      }"
      placeholder="Enter your Username..."
    />
  </div>
</template>
