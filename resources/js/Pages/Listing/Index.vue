<template>
    <div v-for="listing in listings" :key="listing.id">
        {{ listing.city }}
    </div>
</template>

<script setup>
defineProps({
    listings: Array,
});
</script>
