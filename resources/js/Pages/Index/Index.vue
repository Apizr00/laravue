
<template>
    <div>Index</div>
    <div>
        The message is: {{ message }}
    </div>
    <Link href="/hello">Show Page</Link>
</template>

<script setup>
import { Link } from '@inertiajs/vue3';
defineProps({
    message: String
});

</script>