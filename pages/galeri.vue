<template>
  <div class="container-fluid pt-5">
    <div class="judul text-center pt-5">
      <h2>DOKUMENTASI KEGIATAN</h2>
    </div>

    <div class="row">
      <div v-for="(foto, i) in galeri" :key="i" class="col-6 col-md-4 col-lg-3 mb-4">
            <img :src="foto.galeri" class="cover" alt="" />
          </div>
    </div>
  </div>
</template>
<style scoped>
img {
  width: 100%;
}
</style>
<script setup>
useHead({ title: "Galeri" })
const supabase = useSupabaseClient()
const galeri = ref([])

const getGaleri = async () => {
  const { data, error } = await supabase
    .from('galeri')
    .select('galeri')
  if (error) {
    console.error('Error fetching gallery:', error)
  } else {
    galeri.value = data
  }
}

onMounted(() => {
  getGaleri()
})
</script>
