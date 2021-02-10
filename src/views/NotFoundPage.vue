<template>
  <div>
    <!-- Header -->
    
    <!-- Page content -->
    <section class="py-6">
      <b-container >
        <b-row align-v="center" class="row-grid">
          <b-col md="6">
            <b-img src="img/theme/landing-2.png" fluid />
          </b-col>
          <b-col md="6">
            <div class="pr-md-5">
              <h1 class="text-light">Explore pages</h1>
              <p class="text-light">If you want to get inspiration or just show something directly to your clients, you can jump start your development with our pre-built example pages.</p>
              <router-link to="/user" class="font-weight-bold text-warning mt-5">Explore pages</router-link>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </section>
  </div>
</template>

<script>

export default {
  name: 'not-found'
};
</script>
