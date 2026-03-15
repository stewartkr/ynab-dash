<template>
    <div id="page-container">
        <BudgetSelectorPage 
            v-if="!isBudgetSelected()" 
            :selectBudget
            :budgets
        />
        <DashPage v-else :transactions />
    </div>
</template>

<script>
import DashPage from '../pages/dash/DashPage.vue';
import BudgetSelectorPage from '../pages/budget-selector/BudgetSelectorPage.vue';

export default {
    props: ['isBudgetSelected', 'selectBudget', 'budgets', 'transactions'],
    components: {
        DashPage,
        BudgetSelectorPage
    }
}
</script>