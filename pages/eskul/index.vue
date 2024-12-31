<template>
  <div class="container">
    <h3 class="text-center pt-3">Ekstrakurikuler</h3>
    <div class="row">
      <div v-for="(eskul, i) in cover" :key="i" class="col-lg-4">
        <div class="card mb-5" style="width: 18rem">
          <img :src="eskul.foto" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{{ eskul.nama }}</h5>
            <!-- <p class="card-text">
              Mengembangkan keterampilan teknologi informasi, termasuk
              pemograman,desain grafis, dan jaringan.
            </p> -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient();

const cover = ref([]);

const getCover = async () => {
  const { data } = await supabase.from("eskul").select("*");
  if (data) cover.value = data;
};

onMounted(() => {
  getCover();
});
</script>
