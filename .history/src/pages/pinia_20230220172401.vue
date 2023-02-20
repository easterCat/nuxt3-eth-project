<script setup lang="ts">
import { useCounter } from '~/store/counter';

const counter = useCounter();
</script>

<template>
    <div>
        <div class="global-text">
            <pre>{{ counter.$state }}</pre>
            <!-- Remove this component to get started! -->
            <p>
                N: {{ counter.n }}
                <br />
                myRef: {{ counter.myRef }}
            </p>
            <input v-model="counter.myRef" class="text-black" type="text" />
            <br />
            <input v-model="counter.n" class="text-black" type="number" />
        </div>
        <button class="p-4 global-text" @click="counter.increment()">+1 numberclick</button>
    </div>
</template>
