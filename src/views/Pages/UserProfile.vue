<template>
  <div>
     <base-header class="pb-6 pb-8 pt-5 pt-md-8 bg-white" style="padding-top:49px !important">
      <!-- Card stats -->
      <b-row>
        
        
      </b-row>
      
    </base-header>

    <b-container fluid class="mt--6">
        <b-row >
          <b-col md=10 lg=10>
          <user-card></user-card>
          </b-col>
        </b-row>
      
    </b-container>
  </div>
</template>
<script>
  import EditProfileForm from './UserProfile/EditProfileForm.vue';
  import UserCard from './UserProfile/UserCard.vue';

  export default {
    components: {
      EditProfileForm,
      UserCard
    }
  };
</script>
<style>
</style>
