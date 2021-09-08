<template>
    <div class="user">
        <ul v-for="user in users" :key="user">
       <li>
            {{ user.name}}
            {{ user.lastName}}
            {{ user.anyProp}}
        </li>            
        </ul>
    </div>
</template>

<script>
export default {
    name: 'UserDataInfo',
    data () {
        return {
            users: [
                {name: 'Beata', lastName: 'Sk', anyProp: 'xyz'},
                {name: 'Zdzich', lastName: 'Ab', anyProp: 'ooo'},
                {name: 'Ziutek', lastName: 'xD', anyProp: '2xD'}
            ]
        }
    }
}
</script>

<style>
    .user {
        width: 80 vw;
        height: 60 vh;
        background-color: rgb(20, 165, 20);
        color: antiquewhite

    }
</style>