<script>
export default { 
  data(){
    return{

    }
  },
    props: {
        task: {
            type: Object,
        },
        idx: {
            type: Number,
        }
    },
    emits: ['removeTask'],
    computed:{

    }
}
</script>

<template>
    <div class="card" style="width: 18rem; display: inline-block; margin: 5px;">
        <div class="card-body">
            <h5 class="card-title">Deadline: {{ task.deadline }}</h5>
            <p class="card-text">{{ task.desc }}</p>
            <button class="btn btn-primary" @click="$emit('removeTask', idx)">
                Done
            </button>
        </div>
    </div>
</template>

<style scoped>
.card {
    margin-bottom: 10px;
}
</style>
