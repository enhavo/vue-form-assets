<template>
    <component :is="child.rowComponent" v-for="child of form.children" :form="child" />
</template>

<script setup lang="ts">
import {CheckboxForm} from "@enhavo/vue-form/model/CheckboxForm";

const props = defineProps<{
    form: CheckboxForm
}>()
</script>
