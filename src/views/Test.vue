<template>
    <div class="test">
        <h1>Ben Test</h1>

        test: {{ test }}
        params: {{ params }}

        envTest: {{ envTest }}
    </div>
</template>

<script>
    export default {
        name: 'test',
        data() {
            return {
                test: '123'
            }
        },
        computed: {
            params() {
                return this.$route.params
            },
            envTest() {
                return process.env.VUE_APP_TEST_PARAM
            }
        },
        mounted() {
            console.log('this.route.params', this.$route.params)

            console.log('process.env.VUE_APP_TEST_PARAM', process.env.VUE_APP_TEST_PARAM)
        }
    }
</script>
