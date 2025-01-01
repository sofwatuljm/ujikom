<template>
  <div class="container pt-5 pb-5 mb-5">
    <div class="row">
      <form>
        <div class="mb-3">
          <label for="exampleInputtext" class="form-label">Nama</label>
          <input type="text" class="form-control" id="exampleInputtext" />
        </div>
        <div class="mb-3">
          <label for="exampleInputEmail1" class="form-label">Email</label>
          <input
            type="email"
            class="form-control"
            id="exampleInputEmail1"
            aria-describedby="emailHelp"
          />
          <div id="emailHelp" class="form-text"></div>
        </div>

        <div class="mb-3">
          <label for="exampleInputtext" class="form-label">Pesan</label>
          <textarea class="form-control" style="height: 100px"></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: "Kontak",
  meta: [
    {
      name: "description",
      content: "Kontak",
    },
  ],
});
</script>

<!-- <template>
  <div class="container">
    <h3 class="text-center pt-3">Ekstrakurikuler</h3>
    <div class="row">
      <div v-for="(book, i) in cover" :key="i" class="col-lg-4">
        <div class="card mb-5" style="width: 18rem">
          <img :src="book.foto" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{{ book.nama }}</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead({
  title: "Ekstrakurikuler",
  meta: [
    {
      name: "description",
      content: "Ekstrakurikuler",
    },
  ],
});
const supabase = useSupabaseClient();

const cover = ref([]);

const getCover = async () => {
  const { data } = await supabase.from("eskul").select("*");
  if (data) cover.value = data;
};

onMounted(() => {
  getCover();
});
</script> -->
