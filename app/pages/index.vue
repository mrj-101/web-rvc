<template>
    <div>
        <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
            <UPageCard
                v-for="item in news"
                :description="item.detail"
            >
                <template #title>
                    <img :src="item.image" />
                    <h2>{{item.title}}</h2>
                </template>
            </UPageCard>
        </div>
    </div>
</template>

<script setup>
    let news = ref(null)

    await $fetch('http://localhost:9000/api/news')
        .then(result => {
            if (result.success) {
                news.value = result.rows
            }
        })
</script>