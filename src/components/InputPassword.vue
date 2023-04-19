<script setup>
import { ref, computed } from 'vue';

let passwordFieldType = ref("password")
const showPassword =  ()  => passwordFieldType.value = passwordFieldType.value === "password" ? "text" : "password";
</script>

<template>
    <div class="container text-center input-password">
        <h1 class="my-3">Exercise Input Password</h1>
        <input :type="passwordFieldType" class="form-control"  />         
        <div class="d-block">
            <button @click="showPassword" type="password"  class="mt-2 btn btn-primary"
        >Show Password</button>
        </div>
    </div>
</template>

<style lang="css" scoped>
    #show-password:hover {
        cursor: pointer;
        user-select: none;
    } 
</style> 