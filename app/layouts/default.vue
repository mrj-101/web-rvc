<template>
  <div>
    <UHeader title="RVC">
      <UNavigationMenu :items="items" class="px-20" />

      <template #body>
        <UNavigationMenu :items="items" orientation="vertical" />
      </template>
    </UHeader>

    <UContainer class="mt-5">
      <slot />
    </UContainer>
  </div>
</template>

<script setup>
  const items = ref([
  {
    label: 'ข้อมูลพื้นฐาน',
    icon: 'i-lucide-book-open',
    children: [
      {
        label: 'ประวัติโรงเรียน',
        icon: 'i-lucide-house',
        to: '/about'
      },
      {
        label: 'ประวัติโรงเรียน',
        icon: 'i-lucide-house',
        to: '/about'
      },
    ]
  },
  {
    label: 'บุคลากร',
    icon: 'i-lucide-book-open',
    children: [
      {
        label: 'หมวดคณิตศาสตร์',
        icon: 'i-lucide-house',
        to: '/personnel/math'
      },
      {
        label: 'หมวดวิทยาศาสตร์',
        icon: 'i-lucide-house',
        to: '/personnel/science'
      },
      {
        label: 'หมวดคณิตศาสตร์',
        icon: 'i-lucide-house',
        to: '/personnel/math'
      },
      {
        label: 'หมวดวิทยาศาสตร์',
        icon: 'i-lucide-house',
        to: '/personnel/science'
      },
      {
        label: 'หมวดคณิตศาสตร์',
        icon: 'i-lucide-house',
        to: '/personnel/math'
      },
      {
        label: 'หมวดวิทยาศาสตร์',
        icon: 'i-lucide-house',
        to: '/personnel/science'
      },
    ]
  }
  ])
</script>