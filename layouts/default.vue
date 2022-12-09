<template>
    <div class="grid grid-cols-1 gap-8">
        <div class=" bg-black bg-gradient-to-t from-gray-700">
            <nav class=" grid grid-cols-4 content-center h-24">
                <NuxtLink to="/" class="col-span-2 ml-4" >
                    <img  src="../assets/image/logo_branca_header.svg" alt="Logotipo induspharma">
                </NuxtLink>
                <ul class="menu col-span-2 flex justify-between items-center mr-4 text-white">
                    <li>
                        <Menu v-slot="{ open }" >
                            <MenuButton class="" :class="[ open ? 'bg-blue-500 hover:no-underline ' : '', 'hover:underline underline-offset-4 p-1 rounded-t']">Produtos</MenuButton>

                            <MenuItems class="absolute  bg-white text-black rounded-b w-60 border-t-4 border-blue-500">
                                <div class="flex flex-col">
                                    <MenuItem  class="border hover:border-blue-500 p-2 group">
                                        <NuxtLink to="/products">
                                            <div class="flex items-end justify-between">
                                                <div class="flex flex-col justify-between">
                                                    <svg class="mb-6" width="18" height="19" viewBox="0 0 18 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                                                        <path class="group-hover:fill-blue-500" fill-rule="evenodd" clip-rule="evenodd" d="M9 18.5C13.9706 18.5 18 14.4706 18 9.5C18 4.52944 13.9706 0.5 9 0.5C4.02944 0.5 0 4.52944 0 9.5C0 14.4706 4.02944 18.5 9 18.5ZM9.00343 16.2832C8.06867 16.2832 7.3109 15.5254 7.3109 14.5906V11.6386H4.33963C3.40488 11.6386 2.64711 10.8808 2.64711 9.94608C2.64711 9.01132 3.40488 8.25355 4.33963 8.25355H7.3109V4.85859C7.3109 3.92384 8.06867 3.16607 9.00343 3.16607C9.93819 3.16607 10.696 3.92384 10.696 4.85859V8.25355H14.0717C15.0064 8.25355 15.7642 9.01132 15.7642 9.94608C15.7642 10.8808 15.0064 11.6386 14.0717 11.6386H10.696V14.5906C10.696 15.5254 9.93819 16.2832 9.00343 16.2832Z" fill="#B7B7B7"/>
                                                    </svg>
                                                    <p>Acelerador Biologico</p>
                                                </div>
                                                <img src="../assets/image/amf_menu.svg" alt="">
                                            </div>
                                        </NuxtLink>
                                    </MenuItem>
                                </div>
                            </MenuItems>
                        </Menu>    
                    </li>
                    <li>
                        <Menu v-slot="{ open }">
                            <MenuButton  class="" :class="[ open ? 'bg-blue-500 hover:no-underline ' : '', 'hover:underline underline-offset-4 p-1 rounded-t']">Cadastre-se</MenuButton>
                            <menuItems class="absolute  bg-white text-black rounded-b w-60 border-t-4 border-blue-500">
                                <div class="flex flex-col">
                                    <MenuItem class="border hover:border-blue-500 p-2 group">
                                        <NuxtLink to="/about">Seja distribuidor</NuxtLink>
                                    </MenuItem>
                                    <MenuItem class="border hover:border-blue-500 p-2 group">
                                        <NuxtLink to="/about">Cadastre sua Loja</NuxtLink>
                                    </MenuItem>
                                </div>
                            </menuItems>
                        </Menu>        
                    </li>
                    <li class="hover:underline underline-offset-4 p-2"><NuxtLink to="/products">Onde comprar</NuxtLink></li>
                    <li class="hover:underline underline-offset-4 p-2"><NuxtLink to="/products">Nossa História</NuxtLink></li>
                </ul>
            </nav>
        </div>
        <main>
            <slot />
        </main>
        
        <footer class="flex flex-col justify-around  bg-black bg-gradient-to-b from-gray-800 h-96">
            <div class="grid grid-cols-4 gap-4 h-56 content-center">

                <div class="flex flex-col items-center justify-between">
                    <img src="../assets/image/Logomarca_branca.svg" alt="" class="mb-4">
                    <button class="flex border border-white p-2 rounded-lg hover:bg-white hover:border-black hover:text-black">
                        <p class="text-white mr-3">Fale com a gente!</p>
                        <img src="../assets/icons/wpp_branco.svg" alt="" class="hover:fill-black">
                    </button>

                </div>

                <div class="text-white flex flex-col justify-between">
                    <div class="flex">
                        <img src="../assets/icons/fone_braco.svg" alt="" class="mr-2">
                        <p>55 (41) 3245-3903</p>
                    </div>
                    <div class="flex">
                        <img src="../assets/icons/horario_branco.svg" alt="" class="mr-2">
                        <p>Seg a Sex 9h as 17h</p>
                    </div>
                    <div class="flex">
                        <img src="../assets/icons/email_branco.svg" alt="" class="mr-2">
                        <p>Contato@induspharma.com</p>
                    </div>
                    <div class="flex">
                        <img src="../assets/icons/localizacao_branco.svg" alt="" class="mr-2">
                        <p>
                            R. Vicente Celestino, nº 269
                            Fazendinha, Curitiba – PR, 81330-360
                        </p>
                    </div>
                </div>

                <div class="text-white flex flex-col justify-between">
                    <h3 class="text-3xl">Instucional</h3>
                    <NuxtLink to="/" class="hover:underline underline-offset-4">Pagina Inicial</NuxtLink>
                    <NuxtLink>Produtos</NuxtLink>
                    <NuxtLink>Nossa Historia</NuxtLink>
                    <NuxtLink>Politica de privacidade</NuxtLink>
                </div>
                <div class="flex flex-col justify-between">
                    <h3 class="text-3xl text-white">Siga nossas redes</h3>
                    <div class="flex"> 
                        <img src="../assets/icons/icon_youtube.svg" alt="" class="mr-2">
                        <img src="../assets/icons/icon_insta.svg" alt="">
                    </div>
                    <div>
                        <button class="text-white rounded-lg border mr-2 border-white p-3 hover:bg-white hover:text-black hover:border-black">Seja um distribuidor</button>
                        <button class="text-white rounded-lg border border-white p-3 hover:bg-white hover:text-black hover:border-black">Cadastre sua Loja</button>
                    </div>
                </div>
            </div>
    
            <p class="text-center text-white text-sm ">Copyright © 2022 Induspharma. Todos os Direitos Reservados | CNPJ: 12.502.011/0001-59</p>
           
        </footer>
    </div>
</template>

<script setup>
import {Menu, MenuButton, MenuItems, MenuItem} from '@headlessui/vue'

</script>