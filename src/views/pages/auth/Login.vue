<script setup>

import { ref } from 'vue';
//IMAGENES
import myImage from '@/assets/images/PrensaIbericaLogo.jpg';
import backgroundImage from '@/assets/images/bg.jpg';

const email = ref('');
const password = ref('');
const checked = ref(false);
</script>

<template>

    <div class="flex items-center justify-center min-h-screen min-w-[100vw] overflow-hidden"
        :style="{ backgroundImage: `url(${backgroundImage})`, backgroundSize: 'cover', backgroundPosition: 'center' }">
        <div class="flex flex-col items-center justify-center">
            <div
                style="border-radius: 56px; padding: 0.3rem; background: linear-gradient(180deg, #0f5274 10%, rgba(15, 82, 116, 0) 30%)">
                <div class="w-full bg-surface-0 dark:bg-surface-900 py-20 px-8 sm:px-20" style="border-radius: 53px">
                    <div class="text-center mb-8">
                        <img :src="myImage" alt="Logo de Recursos en la Red" class="mb-8 w-70 h-32 shrink-0 mx-auto">


                    </div>

                    <div>
                        <label for="email1"
                            class="block text-surface-900 dark:text-surface-0 text-xl font-medium mb-2">Email</label>
                        <InputText id="email1" type="text" placeholder="Dirección email"
                            class="w-full md:w-[30rem] mb-8" v-model="email"
                            @focus="e => e.target.style.borderColor = '#0f5274'"
                            @blur="e => e.target.style.borderColor = ''" />

                        <label for="password1"
                            class="block text-surface-900 dark:text-surface-0 font-medium text-xl mb-2">Contraseña</label>
                        <Password id="password1" v-model="password" placeholder="Contraseña" :toggleMask="true"
                            class="mb-4" fluid :feedback="false" @focus="e => e.target.style.borderColor = '#0f5274'"
                            @blur="e => e.target.style.borderColor = ''"></Password>

                        <div class="flex items-center justify-between mt-2 mb-8 gap-8">


                        </div>
                        <Button label="ACCEDER" class="w-full" as="router-link" to="/"
                            :style="{ backgroundColor: '#0f5274 !important', color: '#FFFFFF !important', fontWeight: 'bold !important', padding: '0.5rem 1rem !important', borderRadius: '0.375rem !important', borderColor: '#0f5274 !important', borderWidth: '1px' }"></Button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.pi-eye {
    transform: scale(1.6);
    margin-right: 1rem;
}

.pi-eye-slash {
    transform: scale(1.6);
    margin-right: 1rem;
}
</style>
