<template>
  <div class="member">
    <img
      :src="image"
      alt=""
      class="profile-photo"
    >
    <span class="location">{{ location }}</span>
    <span class="job-position">{{ jobPosition }}</span>
    <span class="hashtags">#{{ hashtags[0] }} #{{ hashtags[1] }}</span>
  </div>
</template>
<script>
export default {
  name: 'TeamMembers',
  props: {
    image: {
      type: String,
      required: true
    },
    location: {
      type: String,
      required: true
    },
    jobPosition: {
      type: String,
      required: true
    },
    hashtags: {
      type: Array,
      required: true
    }
  }
};
</script>
<style lang="scss" scoped>
@import "~/assets/scss/index.scss";
.member {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  width: 100%;
  height: auto;
  border-radius: 10px;
  background-color: #e0e0e0;
}

.profile-photo {
  width: inherit;
  max-height: auto;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  background-size: cover;
  object-fit: cover;
}

.location,
.job-position,
.hashtags {
  width: 100%;
  margin-top: 1vh;
  padding-left: 2vw;
  padding-right: 2vw;
}

.location {
  color: $primary-grey;
  text-transform: uppercase;
}

.hashtags {
  padding-bottom: 1vh;
}
</style>
