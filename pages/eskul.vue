<template>
  <div class="container text-center pt-5">
    <h2 class="pt-5">EKSTRAKULIKULER</h2>
    <hr>
    <div class="row">
      <div v-for="(foto, i) in eskul" :key="i" class="col-6 col-md-4 col-lg-3 mb-4">
        <img :src="foto.eskul" class="cover" alt="" />
        <h3>{{ foto.name }}</h3>
      </div>
    </div>
  </div>

</template>
<style scoped>
.col {
  margin-top: 30%;
}
img {
  width: 100%;
}
</style>
<script setup>
useHead({ title: "Ektrakulikuler" })
const supabase = useSupabaseClient()
const eskul = ref([])

const getEskul = async () => {
  const { data, error } = await supabase
    .from('eskul')
    .select('*')
  if (error) {
    console.error('Error fetching gallery:', error)
  } else {
    eskul.value = data
  }
}

onMounted(() => {
  getEskul()
})
</script>
