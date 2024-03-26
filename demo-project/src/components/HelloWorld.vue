<script setup lang="ts">
import { ref, type Ref, onMounted } from 'vue'
import UserCard from '../components/UserCard.vue'

defineProps<{ msg: string }>()

const users: Ref<Array> = ref([])

onMounted(async (): Promise<void> => {
  try {
    const res = await fetch('https://jsonplaceholder.typicode.com/users', {
      method: 'GET'
    })
    if (!res.ok) {
      throw new Error('ERROR while grabbing users from jsonplaceholder')
    }
    const jsonRes = await res.json()
    users.value = jsonRes
  } catch (err) {
    if (err instanceof Error) console.error(err.message)
  }
})
</script>

<template>
  <div class="greetings">
    <h1>{{ msg }}</h1>
  </div>
  <div class="users-wrapper" :key="user.id" v-for="user in users">
    <UserCard
      class="user-element"
      :id="user.id"
      :name="user.name"
      :username="user.username"
      :street="user.address.street"
      :suite="user.address.suite"
      :city="user.address.city"
      :zipcode="user.address.zipcode"
      :lat="user.address.geo.lat"
      :lng="user.address.geo.lng"
      :phone="user.phone"
      :website="user.website"
      :companyName="user.company.name"
      :catchPhrase="user.company.catchPhrase"
      :bs="user.company.bs"
    />
  </div>
</template>

<style scoped>
h1 {
  font-weight: 700;
  font-size: 2.4rem;
  position: relative;
  font-family: 'Arial';
  color: #34495e;
  top: -10px;
}

.greetings {
  display: flex;
  justify-content: center;
  margin: 0 auto;
}

.users-wrapper {
  display: flex;
  justify-content: center;
  margin: 0 auto;
  padding: 10px;
}

.user-element {
  background-color: #d3e5c8;
  grid-template-rows: repeat(3, 120px);
  border: 2.5px solid #34495e;
  border-radius: 5px;
  padding: 20px;
  width: 20em;
  min-width: 95vw;
  height: 21em;
  overflow: scroll;
}
</style>
