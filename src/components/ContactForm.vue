<script setup>
import { ref } from 'vue'

const emit = defineEmits(['submit'])

const form = ref({
  firstName: '',
  lastName: '',
  email: '',
  phoneNumber: ''
})

const handleSubmit = () => {
  emit('submit', form.value)
}
</script>

<template>
  <div class="panel is-success">
    <div class="panel-heading">Add Contact</div>
    <div class="panel-block">
      <form @submit.prevent="handleSubmit" class="is-flex is-flex-direction-column is-flex-grow-1 mt-3">
        <div class="field">
          <label class="label">First Name</label>
          <div class="control">
            <input v-model="form.firstName" type="text" class="input" placeholder="First Name" />
          </div>
        </div>
        <div class="field">
          <label class="label">Last Name</label>
          <div class="control">
            <input v-model="form.lastName" type="text" class="input" placeholder="Last Name" />
          </div>
        </div>
        <div class="field">
          <label class="label">Email</label>
          <div class="control">
            <input v-model="form.email" type="text" class="input" placeholder="Email" />
          </div>
        </div>
        <div class="field">
          <label class="label">Phone Number</label>
          <div class="control">
            <input
              v-model="form.phoneNumber"
              type="text"
              class="input"
              placeholder="Phone Number"
            />
          </div>
        </div>
        <button type="submit" class="button is-link is-info">Add Contact</button>
      </form>
    </div>
  </div>
</template>

<style scoped></style>

http://localhost:5173/
https://github.com/nashville-software-school/Vue-Workshop/wiki/Lesson-2-(Props-&-Events)