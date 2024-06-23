<script setup lang="ts">
defineOptions({
  name: 'IndexPage',
})
const user = useUserStore()
const name = ref(user.savedName)

const router = useRouter()
function _go() {
  if (name.value)
    router.push(`/hi/${encodeURIComponent(name.value)}`)
}

const { _t } = useI18n()
</script>

<template>
  <div />
</template>

<route lang="yaml">
meta:
  layout: home
</route>
