<script setup>
import { ref } from 'vue';

const menu = ref({
  payment: {
    deposit: {
      create: {
        id: 1,
        name: "Create Deposit",
        code: "payment-deposit-create"
      },
      update: {
        id: 2,
        name: "Update Deposit",
        code: "payment-deposit-update"
      }
    }
  },
  finance: {
    deposit: {
      create: {
        id: 3,
        name: "Create Deposit",
        code: "payment-deposit-create"
      }
    }
  }
})

</script>

<template>
  <ul>
    <li v-for="key1 in Object.keys(menu)">
      {{ key1 }}
      <ul>
        <li v-for="key2 in Object.keys(menu[key1])">
          {{ key2 }}
          <ul>
            <li v-for="key3 in Object.keys(menu[key1][key2])">
              {{ menu[key1][key2][key3].name }} (code : {{ menu[key1][key2][key3].code }})
            </li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</template>

<style scoped>
li {
  text-align: left;
}
</style>
