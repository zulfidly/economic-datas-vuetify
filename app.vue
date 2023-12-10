<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>


<script setup>
const route = useRoute()
const router = useRouter()
console.log(router.getRoutes());
const navItem = router.getRoutes()
let navTitles = []
let group = []
navItem.forEach((x)=> {
  if(x.path === '/') return
  
  navTitles.push(x.meta)
  group.push(x.meta.group)
})
console.log(navTitles);
console.log(Array.from(new Set(group)))

let temp = new Set()

</script>