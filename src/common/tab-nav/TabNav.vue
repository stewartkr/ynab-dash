<template>
    <div id="tab-nav">
        <div v-for="tab in tabs" :key="tab.name">
            <button 
                @click="selectTab(tab.name)" 
                class="tab-nav_button"
                :style="{ 'font-weight': isSelectedTab(tab.name) ? 'bold' : 'normal' }"
            >
                {{ tab.name }}
            </button>
        </div>
    </div>
</template>

<script>
export default {
    props: ['tabs', 'selectTab', 'isSelectedTab']
}
</script>