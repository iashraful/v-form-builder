<template>
<div class="example">
  <h2 class="title">Example 1</h2>
  <v-form-maker
    submitBtnText="Save"
    :config="config"
  />
</div>
</template>

<script>
import VFormMaker from '../components/VFormMaker'

export default {
  name: 'Example',
  components: { VFormMaker },
  data () {
    return {
      config: {
        props: [
          {
            group: 'Basic Information',
            fields: [
              {
                title: 'First Name',
                type: 'text',
                name: 'first_name',
                required: true
              },
              {
                title: 'Last Name',
                type: 'text',
                name: 'last_name'
              },
              {
                title: 'Email',
                type: 'email',
                name: 'email',
                required: true
              },
              {
                title: 'Phone',
                type: 'number',
                name: 'phone_number',
                required: false
              },
              {
                title: 'Profile Picture',
                type: 'image',
                name: 'profile_photo',
                required: true
              }
            ]
          },
          {
            group: 'Location Information',
            fields: [
              {
                title: 'Address',
                type: 'text',
                name: 'address',
                required: true
              }
            ]
          }
        ]
      }
    }
  }
}
</script>

<style scoped lang="scss">
    .example {
        width: 550px;
        margin: 0 auto;
        .title {
            text-align: center;
        }
    }
</style>
