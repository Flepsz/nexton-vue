<script setup lang="ts">
import { Switch } from "@/components/ui/switch";

const colorMode = useColorMode();
const isDark = computed({
  get () {
    return colorMode.value === 'dark'
  },
  set () {
    colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
  }
})
</script>

<template>
	<Switch @update:checked="isDark = !isDark"  />
</template>
