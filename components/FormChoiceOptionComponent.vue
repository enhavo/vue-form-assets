<template>
    <option :ref="(el) => choice.element = (el as HTMLOptionElement)" :value="choice.value">{{ choice.label }}</option>
</template>

<script setup lang="ts">
import {Choice} from "@enhavo/vue-form/model/ChoiceForm"

const props = defineProps<{
    choice: Choice
    preferredChoices?: boolean
}>()
</script>
