<script>
export default {
    props: {
        contacts: { type: Array, default: [] },
        activeIndex: { type: Number, default: -1 },
    },
    emits: ["update:activeIndex"],
    watch: {
        activeIndex(newValue) {
            if (newValue === -1) {
                this.selected = -1;
            }
        },
    },
    data() {
        return {
            selected: this.activeIndex,
        };
    },
    methods: {
        select(index) {
            this.selected = index;
            this.$emit("update:activeIndex", index);
        },
    },
    ////////////////////////////////////////////////////////////////
     
};



</script>

<template>
    <ul class="list-group list-group-horizontal">
        <li
            class="list-group-item rounded"
            v-for="(contact, index) in contacts"
            :key="contact.id"
            :class="{ active: index === selected }"
            @click="select(index)"
        >
            {{ contact.name }}
        </li>
         <!-- <li
            class="list-group-item rounded"        >
             <button class="btn btn-sm btn-success" @click="goToAddContact">
                    <i class="fas fa-plus"></i> Thêm mới
                </button>

        </li> -->
    </ul>
</template>

<style>
    .list-group-item{
        background-color:gray;
        height:200px;
        min-width:200px;      
        margin: 10px 20px;
        /* display: flex; */
    }
    .list-group{
        width:1200px;
        display: flex;
    flex-wrap: wrap;
    }
</style>