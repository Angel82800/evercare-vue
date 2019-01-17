<template>
    <v-layout wrap>
        <v-flex md12 xs12 sm12>
            <v-layout wrap class="respond-title">
                <div>
                    <h2>Let Carers Respond To You</h2>
                    <span>How Does This Work?</span>
                </div>
                <v-btn color="#00AF7C" class="post-job-request">Post A Job Request</v-btn>
            </v-layout>
            <v-layout wrap>
                <v-flex md3 xs12 sm6 class="profile-card first">
                    <profileCard 
                        rating="4"/>
                </v-flex>
                <v-flex md3 xs12 sm6 class="profile-card">
                    <profileCard 
                        rating="4"/>
                </v-flex>
                <v-flex md3 xs12 sm6 class="profile-card">
                    <profileCard 
                        rating="4"/>
                </v-flex>
                <v-flex md3 xs12 sm6 class="profile-card">
                    <profileCard 
                        rating="4"/>
                </v-flex>
            </v-layout>
            <v-layout wrap>
                <v-flex md3 xs12 sm6 class="profile-card first">
                    <profileCard 
                        rating="4"/>
                </v-flex>
                <v-flex md3 xs12 sm6 class="profile-card">
                    <profileCard 
                        rating="4"/>
                </v-flex>
                <v-flex md3 xs12 sm6 class="profile-card">
                    <profileCard 
                        rating="4"/>
                </v-flex>
                <v-flex md3 xs12 sm6 class="profile-card">
                    <profileCard 
                        rating="4"/>
                </v-flex>
            </v-layout>
        </v-flex>
    </v-layout>
</template>
<style lang="scss" scoped>
    .post-job-request {
        color: white;
        padding: 0 30px;
        margin-left: 30px;
    }

    .profile-card {
        padding: 5px;
    }

    .profile-card.first {
        padding-left: 0px;
    }

    .respond-title {
        margin-bottom: 50px;
    }
</style>
<script>
import profileCard from '~/components/list/profileCard';
export default {
    components: {
        profileCard
    }
}
</script>
