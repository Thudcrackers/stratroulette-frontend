<template>
  <div id="strat">
      <div class="container">
          <div class="columns">
              <div class="column is-desktop"></div>
              <div class="column is-half-desktop">
                  <div class="card">
                      <div class="card-content">
                          <div class="media">
                              <div class="media-content">
                                  <p class="title is-4 has-text-centered">{{title}}</p>
                              </div>
                          </div>
                          <div class="content">
                              {{text}}
                          </div>
                      </div>
                  </div>
              </div>
              <div class="column is-desktop"></div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Strat',
    props: {
        title: String,
        text: String
    }
}
</script>

<style>

</style>
