<template>
    <div id="dash-page">
        <TabNav 
            :tabs 
            :selectTab
            :isSelectedTab
        />
        <component 
            :is="getSelectedTab().component"
            :transactions
        />
    </div>
</template>

<script>
import TabNav from '../../common/tab-nav/TabNav.vue';
import CategoriesTab from './tabs/categories/CategoriesTab.vue';
import DailyTab from './tabs/daily/DailyTab.vue';
import TransactionsTab from './tabs/transactions/TransactionsTab.vue';

export default {
    props: ['transactions'],
    data() {
        return {
            selectedTab: 'Transactions',
            tabs: [
                {
                    name: 'Transactions',
                    component: TransactionsTab,
                },
                {
                    name: 'Daily',
                    component: DailyTab,
                },
                {
                    name: 'Categories',
                    component: CategoriesTab,
                }
            ]
        }
    },
    components: {
        CategoriesTab,
        DailyTab,
        TransactionsTab,
        TabNav
    },
    methods: {
        selectTab(newTabName) {
            this.selectedTab = newTabName;
        },
        isSelectedTab(tabName) {
            return this.selectedTab === tabName;
        },
        getSelectedTab() {
            return this.tabs.find((tab) => tab.name === this.selectedTab)
        }
    }
}
</script>