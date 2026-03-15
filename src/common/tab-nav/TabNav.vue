<template>
    <nav id="tab-nav" class="navbar">
        <div v-for="tab in tabs" :key="tab.name">
            <button
                @click="selectTab(tab.name)" 
                class="tab-nav_button"
                :style="{ 'font-weight': isSelectedTab(tab.name) ? 'bold' : 'normal' }"
            >
                {{ tab.name }}
            </button>
        </div>
    </nav>
</template>

<script>
export default {
    props: ['tabs', 'selectTab', 'isSelectedTab']
}
</script>