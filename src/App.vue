<script lang="ts" setup>
import { theme } from 'ant-design-vue'
import zhCN from 'ant-design-vue/es/locale/zh_CN'

const locale = ref(zhCN)
</script>

<template>
  <a-config-provider
    :theme="{
      token: {
        colorPrimary: '#3498db',
      },
      algorithm: isDark ? theme.darkAlgorithm : theme.defaultAlgorithm,
    }"
    :locale="locale"
  >
    <RouterView />
  </a-config-provider>
</template>
