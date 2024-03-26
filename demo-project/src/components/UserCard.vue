<script setup lang="ts">
defineProps<{
  id: number
  name: string
  username: string
  street: string
  suite: string
  city: string
  zipcode: string
  lat: string
  lng: string
  phone: string
  website: string
  companyName: sring
  catchPhrase: string
  bs: string
}>()
</script>

<template>
  <div class="user-card">
    <p><em>Name:</em> {{ name }}</p>
    <p><em>UserName:</em> {{ username }}</p>
    <p><em>Address:</em> {{ street }}</p>
    <p><em>Suite:</em> {{ suite }}</p>
    <p><em>City:</em> {{ city }}</p>
    <p><em>ZipCode:</em> {{ zipcode }}</p>
    <p><em>Latitude:</em> {{ lat }}</p>
    <p><em>Longitude:</em> {{ lng }}</p>
    <p><em>PhoneNumber:</em> {{ phone }}</p>
    <p><em>WebSite:</em> {{ website }}</p>
    <p><em>CompanyName:</em> {{ companyName }}</p>
    <p><em>CatchPhrase:</em> {{ catchPhrase }}</p>
    <p><em>BS:</em> {{ bs }}</p>
  </div>
</template>

<style scoped>
.user-card {
  text-align: left;
  font-size: 22.5px;
  color: #34495e;
  overflow: scroll;
  text-wrap: nowrap;
}
.user-card > p {
  font-weight: 400;
}
em {
  font-weight: 500;
}
</style>
