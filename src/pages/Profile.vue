<template>
  <div class="row">
    <div class="col-md-8">
      <edit-profile-form :model="model">
      </edit-profile-form>
    </div>
    <div class="col-md-4">
      <user-card :user="user"></user-card>
    </div>
  </div>
</template>
<script>
  import EditProfileForm from './Profile/EditProfileForm';
  import UserCard from './Profile/UserCard'
  export default {
    components: {
      EditProfileForm,
      UserCard
    },
    data() {
      return {
        model: {
          company: 'Nom Inc.',
          email: 'mike@nom.com',
          username: 'michael23',
          firstName: 'Mike',
          lastName: 'Andrew',
          address: 'Main Ave No. 654, 35 floor',
          city: 'Singapore',
          country: 'Singapore',
          about: 'Nom Inc Senior Relationship Manager, Department IWM.'
        },
        user: {
          fullName: 'Mike Andrew',
          title: 'Senior Relationship Manager/IWM',
          description: `Join Nom Inc since 2010 Jan. Tel: 330-683-2225.`
        }
      }
    }
  }
</script>
<style>
</style>
