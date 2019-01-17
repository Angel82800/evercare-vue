<template>
    <v-layout wrap>
        <v-flex md12 xs12 sm12>
            <v-layout column>
                <h2>Find The Best Healthcare Professionals</h2>
                <span>All Professionals Have Been Screen And Verified By Evercare</span>
            </v-layout>
            <v-layout class="filter-items">
                <v-card>
                    <v-layout wrap>
                        <v-flex md10 xs12 sm12>
                            <v-layout wrap>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Categories"
                                        example="Registered Nurses"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Location"
                                        example="West Kowloon"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Hourly Rate"
                                        example="$200 - $400"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Rating"
                                        example="4.5+"
                                        :items="items"/>
                                </v-flex>
                            </v-layout>
                        </v-flex>
                        <v-flex md2 xs12 sm12 class="filter">
                            <v-layout justify-center>
                                <v-btn @click="moreFilters">
                                    <v-icon>filter_list</v-icon>&nbsp;&nbsp;More Filters
                                </v-btn>
                            </v-layout>
                        </v-flex>
                    </v-layout>
                    <v-layout v-if="!filter_flag" class="filter-condition">
                        <span>Filter Applied: Condition is <strong>Dementia</strong></span>
                    </v-layout>
                    <!-- More Filter Part -->
                    <v-layout wrap v-if="filter_flag">
                        <v-flex md10 xs12 sm12>
                            <v-layout wrap>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Shift"
                                        example="Night Shifts"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Languages"
                                        example="English"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Gender"
                                        example="Male"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Age Range"
                                        example="40 - 50 years old"
                                        :items="items"/>
                                </v-flex>
                            </v-layout>
                        </v-flex>
                        <v-flex md2 xs12 sm12>
                            
                        </v-flex>
                    </v-layout>
                    <v-layout wrap v-if="filter_flag">
                        <v-flex md10 xs12 sm12>
                            <v-layout wrap>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Categories"
                                        example="Toileting and"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Location"
                                        example="Fitness And Training"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Common Conditions"
                                        example="Dementia"
                                        learn_more_title="Common Conditions"
                                        learn_more_url="#"
                                        :items="items"/>
                                </v-flex>
                                <v-flex md3 xs12 sm6>
                                    <filterItem
                                        title="Common Needs"
                                        example="Companionship"
                                        learn_more_title="Common Needs"
                                        learn_more_url="#"
                                        :items="items"/>
                                </v-flex>
                            </v-layout>
                        </v-flex>
                        <v-flex md2 xs12 sm12>
                            
                        </v-flex>
                    </v-layout>
                    <v-layout wrap align-center v-if="filter_flag">
                        <v-btn color="#00AF7C" class="close-filter">Close Filters</v-btn>
                        <div class="loading">
                            <v-progress-circular
                                indeterminate
                                color="#00AF7C"
                                ></v-progress-circular>
                            <span>Filters have been applied</span>
                        </div>
                        
                    </v-layout>
                </v-card>
            </v-layout>
        </v-flex>
    </v-layout>
</template>
<style lang="scss" scoped>
    span {
        font-size: 12px;
    }
    .filter-items {
        margin-top: 50px;
        .v-card {
            padding: 30px;
            width: 100%;
        }
    }

    .filter {
        padding-top: 20px;
        button {
            color: #00AF7C;
            text-transform: none;
        }
    }

    .filter-condition {
        padding: 20px 0 0 10px;
    }

    .close-filter {
        color: white;
        text-transform: none;
        padding: 0 35px;
    }

    .loading {
        margin-left: 40px;
        span {
            margin-left: 10px;
        }
    }
</style>
<script>
import filterItem from '~/components/list/filterItem';
export default {
    data () {
        return {
            items: ['All', 'item1', 'item2'],
            filter_flag: false
        }
    },
    components: {
        filterItem
    },

    methods: {
        moreFilters () {
            this.filter_flag = !this.filter_flag;
        }
    }
}
</script>
