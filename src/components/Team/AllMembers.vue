<template>
    <div id="AllMembers">
        <div class="container-fluid" style="margin: 15vh 0 10vh 0;">
            <div class="row">
                <div class="col-lg-10 offset-lg-1 col-sm-12">
                    <h1>All Tosun Members</h1>
                    <p class="text-muted">
                        Even though, there are founders and several teams in the organization,
                        only people that matters are the members.
                    </p>
                    <hr>

                    <div class="row mt-5">
                        <div v-for="member in members" :key="member.url" class="col-1">
                            <a :href="member.url" target="_blank">
                                <img :src="member.image" alt="Member image" class="member-image">
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import AllMembers from '@/assets/members.json'

export default {
  name: 'AllMembers',
  data () {
    return {
      members: AllMembers
    }
  }
}
</script>

<style>
.member-image {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    border: 1px solid #e9ecef;
    margin-top: 10px;
}
</style>
