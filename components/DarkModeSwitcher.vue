<script setup lang="ts">
import { useDark, useToggle } from '@vueuse/core'

import IconMoon from '~icons/radix-icons/moon'
import IconSun from '~icons/radix-icons/sun'

const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<template>
  <div class="cursor-pointer hover:opacity-60" @click="() => toggleDark()">
    <IconMoon v-if="!isDark" />
    <IconSun v-else />
  </div>
</template>
