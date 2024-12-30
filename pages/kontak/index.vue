<template>
  <div class="container pt-4">
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
