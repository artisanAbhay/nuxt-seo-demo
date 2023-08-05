<template>
<div class="col-lg-12 mt-2">
    <div class="card">
        <div class="card-header">
            Home
        </div>
        <div class="card-body">
            <h5 class="card-title">Special title treatment</h5>
            <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</div>
</template>

<script setup>
const route = useRoute()
const {
    data,
    pending,
    error,
    refresh
} = await useAsyncData(
    'meta',
    () => $fetch('https://dev-xod6z6w15z02b67.api.raw-labs.com/mock/meta-tags',{
    params: {
      id: route.name
    }
  })
)
useSeoMeta({
  title: () => data.value?.title,
  description: () => data.value?.description,
  keywords: () => data.value?.keywords,
});
</script>
