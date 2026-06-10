<template>
    <Link href="/">Main Page</Link>&nbsp;
    <Link href="/hello">Show Page</Link>
    <!-- <div>The page with time {{ timer }}</div> -->
    <div v-if="flashSuccess" class="success">
        {{ flashSuccess }}
    </div>
    <div v-if="flashError" class="error">
        {{ flashError }}
    </div>

    <slot>Default</slot>
</template>

<script setup>
import { computed } from "vue";
import { Link, usePage } from "@inertiajs/vue3";
// import { ref } from "vue";

// const timer = ref(0);
// setInterval(() => {
//     timer.value++;
// }, 1000);

const page = usePage();
const flashSuccess = computed(() => page.props.flash.success);
const flashError = computed(() => page.props.flash.error);
</script>

<style scoped>
.success {
    background-color: green;
    color: white;
}
.error {
    background-color: red;
    color: white;
}
</style>
