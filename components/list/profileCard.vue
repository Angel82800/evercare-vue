<template>
    <v-card >
        <div class="card">
            <v-layout align-center justify-end class="verify">
                <v-icon color="#00AF7C" small>brightness_5</v-icon>
                <span>Verified by Evercare</span>
            </v-layout>
            <v-layout row align-center class="image_name">
                <v-flex md4 sm4 xs4 class="avatar">
                    <v-avatar
                        color="grey lighten-4"
                    >
                        <img src="https://vuetifyjs.com/apple-touch-icon-180x180.png" alt="avatar">
                    </v-avatar>
                </v-flex>
                <v-flex md8 sm8 xs8>
                    <h2>Winnie W.</h2>
                    <span><v-icon color="#00AF7C" small>location_on</v-icon>Hong Kong</span>
                    
                </v-flex>
            </v-layout>
            <v-layout>
                <v-flex md8 xs8 sm8 offset-md4 offset-xs4 offset-sm4>
                    <v-rating v-model="getRating" color="#00AF7C" background-color="#00AF7C" small></v-rating>
                </v-flex>
            </v-layout>
            <v-layout class="job-title">
                <span>Job Title............</span>
            </v-layout>
            <v-layout class="certified">
                <v-icon color="#00AF7C" small>brightness_5</v-icon>
                <span>Certified Registered Nurse, Healthcare Worker</span>
            </v-layout>
        </div>        
        <hr>
        <v-layout class="footer">
            <v-flex md8 xs8 sm8>
                <v-icon color="#00AF7C" small>brightness_5</v-icon>
                <span>HK$ 500/hour</span>
            </v-flex>
            <v-flex md4 xs4 sm4 class="save">
                <v-icon color="#00AF7C" small>favorite_border</v-icon>
                <span>Save</span>
            </v-flex>
        </v-layout>
    </v-card>
</template>
<style lang="scss" scoped>
    .card {
        padding: 20px;

        .verify {
            span {
                margin-left: 10px;
                font-size: 12px;
            }
        }

        .list-content {
            margin: 20px 0;
        }

        .avatar {
            text-align: center;
        }
        
        .image_name {
            margin-top: 10px;
        }

        .job-title {
            margin: 10px 0;
        }

        .certified {
            height: 70px;
            span {
                font-size: 12px;
                color:black;
                margin-left: 5px;
            }
        }
        
    }

    hr {
        display: block;
        border: 0;
        border-top: 0.5px solid #E0E0E0;
        padding: 0; 
    }

    .footer {
        padding: 20px;
        background-color: #F9F9F9;
        span {
            color: black;
        }
        .save {
            text-align: right;
        }
    }


    .v-avatar.grey.lighten-4:before {
        content: "";
        display: block;
        padding-top: 100%; 	/* initial ratio of 1:1*/
    }

    .v-avatar.grey.lighten-4 {
        position: relative;
        width: 80%!important;
        height: auto! important;
    }
</style>
<style lang="scss">
    .v-rating .v-icon {
        padding: 0px!important;
    }
</style>

<script>
export default {
    props: ['rating'],
    data() {
        return {
            // rating: 4
        }
    },
    computed: {
        getRating () {
            return parseFloat(this.rating);
        }
    }
}
</script>
