<template>
  <div class="p-3 mb-2 ml-2 bg-dark text-white min-vh-100">
    <div class="container">
      <div class="text-center">
        <nuxt-link to="/"><img class="img-fluid" src="../assets/dnb.png" title="If you’ve never heard Drum and Bass before, here’s the condensed version: a marriage of sped-up Hip Hop breakbeats with dubby bass lines, overlaid with strong melodies from Techno and House music. The genre’s hype dipped off after a few years, but in the past decade the music industry has seen a dramatic resurgence of this once-beloved genre." width="600" height="345"></nuxt-link>
      </div>
      <div class="container-fluid">
        <div class="row">
          <div class="col-lg-2 col-md-12 d-none d-lg-block large-screen-menu">
            <div class="btn-group-vertical">
              <button v-for="item in menu" @click="$router.push(item.replace(' ', '_').toLowerCase())" type="button" class="btn btn-outline-warning btn-lg">{{item}}</button>
            </div>
          </div>
          <div class="d-lg-none small-screen-menu">
            <button v-for="item in menu" @click="$router.push(item.replace(' ', '_').toLowerCase())"
                    type="button" class="btn btn-outline-warning btn-sm">{{item}}</button>
          </div>

          <div class="col-lg-10 col-md-12">
            <Nuxt />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
html, body {
  height: 100%;
}

body {
  font-family: 'Gruppo', cursive;
  font-size: 16px;
  margin-inside: 30px;
}

.btn {
  font-family: 'Graduate', cursive;
  font-size: 15px;
}

.large-screen-menu button {
  margin: 8px;
  margin: 19px;
  margin-right: 8px;
  margin-left: 8px;
}

.small-screen-menu {
  text-align: center;
}

.small-screen-menu button {
  margin: 2px;
}
</style>

<script>
module.exports = {
  data: function () {
    return {
      menu: [
        "TECHSTEP",
        "NEUROFUNK",
        "JUMP UP",
        "DUBSTEP",
        "BREAKCORE",
        "DRUMFUNK",
        "LIQUID",
        "CROSSBREED",
        "TECHNOID",
        "MINIMAL"
      ]
    }
  }
}
</script>

