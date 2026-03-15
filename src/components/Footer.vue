<template>
  <footer class="pt-4 my-md-5 pt-md-5 border-top">
    <div>
      <button v-if="isBudgetSelected()" @click="resetBudget">Reset Budget</button>
      <h2>Privacy Policy</h2>
      <p>This website does not store any information from you or your YNAB account. All data retrieved from the YNAB API is stored only in your browser and is never transmitted to any other location or third-party.</p>
    </div>
  </footer>
</template>

<script>
export default {
  props: ['resetBudget', 'isBudgetSelected']
}
</script>
