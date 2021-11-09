<template>
    <div>
        <h5  class="padding30">약 복용정보</h5>

        <p> 그래프:
            {{aveMedTime}}
        </p>

        <p>
            
            사람들은 평균적으로 {{ people_drug_time[0] }}AM, 
            {{ people_drug_time[1] }}PM 에 약을 복용합니다.
        </p>

        <hr class="rotate">

        <p> 그래프:
            {{ aveMedTime[user_id] }}
        </p>

        <p>
            {{user_id}}님은 평균적으로 {{ aveMedTime[user_id] }}시에 약을 복용합니다.
        </p>
    </div>
    
</template>

<script>

export default {
    name: "Drugpage",
    // 필요 변수 임포트
    props : {
        user_id : String,
        aveMedTime : Object,
        people_drug_time : Object
    },
    data(){
        return {
        }
    },
    methods : {
    },
}
</script>

<style>
.rotate {
    transform: rotate(-2deg);
}
</style>