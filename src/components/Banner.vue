<template>
  <section class="banner">
    <div class="banner_img">
      <img
        class="images"
        :class="{ active: activeFoto1 }"
        src="../assets/Banner1.jpg"
        alt="Foto Banner"
      >
      <img class="images" :class="{ active: activeFoto2 }" src="../assets/Banner2.jpg">
    </div>
    <div class="container banner_content">
      <div class="row">
        <div class="col-md-10">
          <p>
            Simply dummy text of the printing and typesetting industry. Lorem
            Ipsum has been the industry's standard dummy text ever since the
            1500s, when an unknown printer took a galley of type and scrambled
            it to make a type specimen book.
          </p>
          <button>Discografia</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Banner",
  data: function() {
    return {
      activeFoto1: true,
      activeFoto2: false
    };
  },
  methods: {
    toMove: function() {
      this.activeFoto1 = !this.activeFoto1;
      this.activeFoto2 = !this.activeFoto2;
    }
  },
  created: function() {
    setInterval(() => {
      this.toMove();
    }, 5000);
  }
};
</script>

<style>
.banner {
  width: 100%;
  height: 700px;
  background-color: #212121;
  background-image: "../asserts/Banner1.jpg";
  position: relative;
  color: white;
  overflow: hidden;
}
.banner_content .row {
  height: 700px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 20px;

}

.banner_content {
  position: relative;
}

.banner_content p {
  font-size: 20px;
  line-height: 25px;
  font-weight: bold;
}

.banner_img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 700px;
}

.banner_img {
  width: 100%;
  position: absolute;
  top: 0;
}

.images {
  width: 100%;
  position: absolute;
  top: 0;
  opacity: 0;
  transition: opacity linear 2.5s;
}
.active {
  opacity: 1;
}
</style>
