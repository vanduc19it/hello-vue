<template>
    <div>
        <div class="list">
            <div v-for="(language, index) in languages" 
            :key="index" 
            @click="language.selected= !language.selected"
            :class= "{selected:language.selected}"
            >
                <span>{{language.name}}</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                languages: [
                   { name: 'PHP', selected: false},
                   { name: 'JS', selected: false},
                   { name: 'HTML', selected: false},
                   { name: 'NodeJS', selected: false},
                   { name: 'CSS', selected: false}
                    
                ]
            }
        }
    }
</script>

<style>
    .list div {
        display: inline-block;
        border: 1px solid #ebebeb;
        padding: 4px 15px;
        margin-right: 5px;
        border-radius: 4px;
    }
    .list div:hover {
        cursor: pointer;
    }
    .list div.selected {
        background-color: green;
        color: white;
    }
</style>

