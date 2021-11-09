<template>
    <div>
        <h5  class="padding30">{{user_id}}님의 생활패턴</h5>

        <div>
            그래프: {{act2[this.user_id]}}
        </div>

        <p>
            <b v-if="user_most_participate.length > 0">{{user_most_participate.join(', ')}} 참여도</b>
            가 가장 높아요!
        </p>

        <p v-if="user_most_participate.length == 0">
            참여도가 높은 활동이 없어요!
        </p>

        <hr>

        <h5>사람들의 생활패턴</h5>

        그래프: {{act2}}

    </div>
    
</template>

<script>

export default {
    name: "Mainpage",
    // 필요 변수 임포트
    props : {
        user_id : String,
        act2 : Object,
        user_most_participate : Object
    },
    data(){
        return {

        }
    },
    methods : {
        
    }
}
</script>

<style>

</style>