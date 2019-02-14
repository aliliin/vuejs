<template>
    <div class="navbar navbar-default topnav">
        <div class="container">
            <div class="navbar-header">
                <a href="/" class="navbar-brand">
                    <span class="title">{{ logo.title }}</span>
                    <img :src="logo.src" :alt="logo.title">
                </a>
            </div>

            <div id="top-navbar-collapse" class="collapse navbar-collapse">
                <ul class="nav navbar-nav">
                    <li v-for="item in navList">
                        <a href="#">{{ item }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'TheHeader',
        data() {
            return {
                logo: {
                    src: `${this.uploadsUrl}sites/ByvFbNlQYVwhvTyBgLdqitchoacDNznN.jpg`,
                    title: 'VuejsCaff'
                },
                navList: ['社区', '头条', '问答', '教程']
            }
        },
        beforeCreate() {
            this.uploadsUrl = 'https://vuejscaffcdn.phphub.org/uploads/'
        }
    }
</script>

<style scoped>
    .title { display: none;}
</style>