<template>
    <header class="w-full bg-[#151A1F] px-4 py-3 z-[99] lg:px-8" :class="{ 'fixed': fixed }">
        <div class="flex items-center justify-between">
            <div class="flex items-center">
                <NuxtLink :to="'https://serversideup.net'">
                    <img src="/images/logos/server-side-up-logo-horizontal.svg" class="mr-[10px]"/>
                </NuxtLink>
                
                <button type="button" @click.stop="showMenu = true" class="cursor-pointer flex items-center relative" style="box-shadow: 0px 20px 24px -4px rgba(16, 24, 40, 0.08), 0px 8px 8px -4px rgba(16, 24, 40, 0.03);">
                    <span class="font-inter tracking-[.1em] uppercase text-[10px] font-bold text-slate-300">Browse Products</span>
                    <svg class="ml-2" width="8" height="5" viewBox="0 0 8 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M1 0.985321L4 3.98532L7 0.985321" stroke="#CBD5E1" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>

                    <div v-show="showMenu"
                        ref="menuRef"
                        class="absolute shadow-sm z-10 bg-white rounded-b-lg p-4 w-64 top-[28px] flex flex-col content-left text-left">
                            <span class="font-inter font-bold text-black text-[14px]">Books</span>
                            <NuxtLink
                                @click="showMenu = false"
                                :to="'https://serversideup.net/ultimate-guide-to-building-apis-and-spas-with-laravel-and-nuxt3/'"
                                class="flex items-center text-[12px] font-medium font-inter py-2 group">
                                    <div class="w-3 h-3 flex items-center justify-center mr-2">
                                        <svg width="36" height="36" viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <g clip-path="url(#clip0_2716_52308)">
                                                <path d="M8.1 36H27.9C32.374 36 36 32.373 36 27.9V21H0V27.9C0 32.373 3.626 36 8.1 36Z" fill="#001E26" />
                                                <path d="M36 10H0V21H36V10Z" fill="#001E26" />
                                                <path d="M27.9 0H8.1C3.626 0 0 3.626 0 8.1V10H36V8.1C36 3.626 32.374 0 27.9 0Z" fill="#001E26" />
                                                <path d="M16.854 12.943L18.592 9.976L16.994 7.249C16.576 6.534 15.657 6.295 14.942 6.713C14.227 7.131 13.987 8.05 14.406 8.765L16.854 12.943Z" fill="#5ED687" />
                                                <path d="M20.786 6.71401C20.07 6.29501 19.151 6.53501 18.734 7.25001L10.09 22H13.567L21.321 8.76701C21.74 8.05201 21.5 7.13301 20.786 6.71401Z" fill="#5ED687" />
                                                <path d="M28.521 26.92L20.91 13.933L20.147 15.236C19.703 16.186 19.643 17.26 19.962 18.247L25.934 28.438C26.213 28.914 26.714 29.179 27.229 29.179C27.486 29.179 27.748 29.113 27.986 28.973C28.701 28.554 28.94 27.635 28.521 26.92Z" fill="#5ED687" />
                                                <path d="M19.473 21.919L19.302 21.63C19.154 21.406 18.99 21.196 18.804 21.009H6.3C5.471 21.009 4.8 21.674 4.8 22.493C4.8 23.312 5.471 23.977 6.3 23.977H19.694C19.888 23.324 19.835 22.595 19.473 21.919Z" fill="#5ED687" />
                                                <path d="M10.66 26.961C10.173 26.405 9.47 26.027 8.63 26.002H8.626C8.309 25.993 7.998 26.028 7.694 26.089L7.207 26.92C6.788 27.635 7.028 28.554 7.743 28.973C7.981 29.113 8.243 29.179 8.5 29.179C9.015 29.179 9.517 28.913 9.795 28.438L10.66 26.961Z" fill="#5ED687" />
                                                <path d="M24.196 21.009H29.7C30.529 21.009 31.2 21.674 31.2 22.493C31.2 23.312 30.529 23.977 29.7 23.977H24.306C24.112 23.324 24.01 21.196 24.196 21.009Z" fill="#5ED687" />
                                            </g>
                                            <defs>
                                                <clipPath id="clip0_2716_52308">
                                                    <rect width="36" height="36" fill="white" />
                                                </clipPath>
                                            </defs>
                                        </svg>
                                    </div>
                                    <span class="group-hover:underline">Ultimate Guide To APIs & SPAs</span>
                            </NuxtLink>
                            <span class="font-inter font-bold text-black text-[14px] mt-2">Open-Source Projects</span>
                            <NuxtLink
                                @click="showMenu = false"
                                :to="'https://github.com/serversideup/amplitudejs'"
                                class="flex items-center text-[12px] font-medium font-inter py-2 group">
                                    <div class="w-3 h-3 flex items-center justify-center mr-2">
                                        <svg width="53" height="48" class="w-full max-h-full" viewBox="0 0 53 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <path id="AmplitudeJS" fill-rule="evenodd" clip-rule="evenodd" d="M24.62 0L0 47.5191H1.71465L39.8115 28.3566L50.3631 47.596H52.0772L26.3346 0H24.62ZM20.2148 21.4592H24.935V16.6934H26.0462V21.4592H30.7664V22.5815H26.0462V27.3468H24.935V22.5815H20.2148V21.4592Z" fill="url(#paint0_radial_1_16)"/>
                                            <defs>
                                                <radialGradient id="paint0_radial_1_16" cx="0" cy="0" r="1" gradientUnits="userSpaceOnUse" gradientTransform="translate(24.0247 -26.2885) rotate(108.038) scale(65.5676 70.6079)">
                                                    <stop stop-color="#3CD3AD"/>
                                                    <stop offset="1" stop-color="#4CB8C4"/>
                                                </radialGradient>
                                            </defs>
                                        </svg>
                                    </div>
                                    <span class="group-hover:underline">AmplitudeJS</span>
                            </NuxtLink>
                            <NuxtLink
                                @click="showMenu = false"
                                :to="'https://github.com/serversideup/financial-freedom'"
                                class="flex items-center text-[12px] font-medium font-inter py-2 group">
                                    <div class="w-3 h-3 flex items-center justify-center mr-2">
                                        <svg width="24" height="35" class="w-full max-h-full" viewBox="0 0 24 35" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <path d="M0 34.8803H9.21929V21.314H22.4181V13.7168H9.21929H0V34.8803Z" fill="#0052FF"/>
                                            <path d="M0 34.8803H9.21929V21.314H22.4181V13.7168H9.21929H0V34.8803Z" fill="#0052FF"/>
                                            <path d="M0.000244141 7.74712H9.21954H23.8776V0.149963H0.000244141V7.74712Z" fill="#0052FF"/>
                                            <path d="M0.000244141 7.74712H9.21954H23.8776V0.149963H0.000244141V7.74712Z" fill="#0052FF"/>
                                        </svg>
                                    </div>
                                    <span class="group-hover:underline">Financial Freedom</span>
                            </NuxtLink>
                            <NuxtLink
                                @click="showMenu = false"
                                :to="'https://serversideup.net/open-source/docker-php'"
                                class="flex items-center text-[12px] font-medium font-inter py-2 group">
                                    <div class="w-3 h-3 flex items-center justify-center mr-2">
                                        <svg width="26" height="26" viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <g clip-path="url(#clip0_104_156)">
                                                <path d="M12.9672 25.5612L1.67615 19.9156V6.01892L12.9672 11.6645V25.5612Z" fill="#00A9FD"/>
                                                <path d="M12.9673 25.5612L24.2584 19.9156V6.01892L12.9673 11.6645V25.5612Z" fill="#2D7CFE"/>
                                                <path d="M1.67615 6.01892L12.533 0.373383L24.2583 6.01892L12.9672 11.6645L1.67615 6.01892Z" fill="#03E2FF"/>
                                            </g>
                                            <defs>
                                                <clipPath id="clip0_104_156">
                                                    <rect width="25.1878" height="25.1878" fill="white" transform="translate(0.373413 0.373383)"/>
                                                </clipPath>
                                            </defs>
                                        </svg>
                                    </div>
                                    <span class="group-hover:underline">PHP Docker Images</span>
                            </NuxtLink>
                            <NuxtLink
                                @click="showMenu = false"
                                :to="'https://serversideup.net/open-source/spin'"
                                class="flex items-center text-[12px] font-medium font-inter py-2 group">
                                    <div class="w-3 h-3 flex items-center justify-center mr-2">
                                        <svg width="106" height="105" class="w-full max-h-full" viewBox="0 0 106 105" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <rect y="52.7411" width="34.9627" height="34.9627" transform="rotate(-45 0 52.7411)" fill="#3B82F6"/>
                                            <rect x="28.0186" y="24.7224" width="34.9627" height="34.9627" transform="rotate(-45 28.0186 24.7224)" fill="#3B82F6"/>
                                            <rect x="56.0374" y="52.7411" width="34.9627" height="34.9627" transform="rotate(-45 56.0374 52.7411)" fill="#3B82F6"/>
                                        </svg>
                                    </div>
                                    <span class="group-hover:underline">Spin</span>
                            </NuxtLink>
                    </div>
                </button>
            </div>

            <div class="items-center hidden lg:flex">
                <nav class="flex gap-6 mr-6">
                    <NuxtLink v-for="(link, key) in links"
                        :href="link.url"
                        :key="'link-key-'+key"
                        class="font-inter tracking-[.1em] uppercase text-[10px] font-bold text-slate-300 hover:text-white">
                        {{ link.link }}
                    </NuxtLink>
                </nav>
                <nav class="flex gap-[10px]">
                    <NuxtLink 
                        :to="'https://twitter.com/serversideup'"
                        class="text-slate-300 hover:text-white"
                        target="_blank">
                        <svg width="16" height="15" viewBox="0 0 16 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M5.02214 14.0567C3.17357 14.0567 1.45039 13.5191 0 12.5914C1.23142 12.6711 3.40461 12.4802 4.75633 11.1909C2.7229 11.0976 1.80586 9.53805 1.68625 8.87157C1.85903 8.93822 2.68303 9.0182 3.14819 8.83158C0.809085 8.24509 0.450244 6.19235 0.529987 5.56586C0.96857 5.87244 1.71283 5.97908 2.00522 5.95242C-0.174404 4.39287 0.609729 2.04688 0.99515 1.54036C2.55933 3.7074 4.90354 4.92449 7.80365 4.99219C7.74897 4.75237 7.72009 4.50269 7.72009 4.24625C7.72009 2.40583 9.20766 0.913879 11.0427 0.913879C12.0015 0.913879 12.8654 1.32117 13.4718 1.97264C14.1125 1.82251 15.0767 1.47106 15.5481 1.16714C15.3105 2.02023 14.5708 2.73187 14.1234 2.99564C14.1197 2.98663 14.1271 3.00461 14.1234 2.99564C14.5164 2.93619 15.5799 2.7318 16 2.44677C15.7922 2.92602 15.008 3.72287 14.3644 4.16898C14.4842 9.44991 10.4437 14.0567 5.02214 14.0567Z" fill="currentColor"/>
                        </svg>
                    </NuxtLink>

                    <NuxtLink 
                        :to="'https://serversideup.net/discord'"
                        class="text-slate-300 hover:text-white"
                        target="_blank">
                        <svg width="16" height="13" viewBox="0 0 16 13" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M14.0183 2.14105C12.9174 1.21014 11.5963 0.74469 10.2018 0.667114L9.98165 0.899842C11.2294 1.21014 12.3303 1.83075 13.3578 2.68408C12.1101 1.9859 10.7156 1.52045 9.24771 1.3653C8.80734 1.28772 8.44037 1.28772 8 1.28772C7.55963 1.28772 7.19266 1.28772 6.75229 1.3653C5.2844 1.52045 3.88991 1.9859 2.6422 2.68408C3.66972 1.83075 4.77064 1.21014 6.01835 0.899842L5.79817 0.667114C4.40367 0.74469 3.08257 1.21014 1.98165 2.14105C0.733945 4.62348 0.0733945 7.4162 0 10.2865C1.10092 11.5277 2.6422 12.3035 4.25688 12.3035C4.25688 12.3035 4.77064 11.6829 5.13761 11.1398C4.18349 10.9071 3.30275 10.3641 2.7156 9.51075C3.22936 9.82105 3.74312 10.1314 4.25688 10.3641C4.91743 10.6744 5.57798 10.8295 6.23853 10.9847C6.82569 11.0623 7.41284 11.1398 8 11.1398C8.58716 11.1398 9.17431 11.0623 9.76147 10.9847C10.422 10.8295 11.0826 10.6744 11.7431 10.3641C12.2569 10.1314 12.7706 9.82105 13.2844 9.51075C12.6972 10.3641 11.8165 10.9071 10.8624 11.1398C11.2294 11.6829 11.7431 12.3035 11.7431 12.3035C13.3578 12.3035 14.8991 11.5277 16 10.2865C15.9266 7.4162 15.2661 4.62348 14.0183 2.14105ZM5.57798 8.89015C4.84404 8.89015 4.18349 8.19196 4.18349 7.33863C4.18349 6.4853 4.84404 5.78711 5.57798 5.78711C6.31193 5.78711 6.97248 6.4853 6.97248 7.33863C6.97248 8.19196 6.31193 8.89015 5.57798 8.89015ZM10.422 8.89015C9.68807 8.89015 9.02752 8.19196 9.02752 7.33863C9.02752 6.4853 9.68807 5.78711 10.422 5.78711C11.156 5.78711 11.8165 6.4853 11.8165 7.33863C11.8165 8.19196 11.156 8.89015 10.422 8.89015Z" fill="currentColor"/>
                        </svg>
                    </NuxtLink>
                    
                    <NuxtLink 
                        :to="'https://github.com/serversideup/docker-php'"
                        class="text-slate-300 hover:text-white"
                        target="_blank">
                        <svg width="14" height="15" viewBox="0 0 14 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M7 0.65799C3.1325 0.65799 0 3.79049 0 7.65799C0 10.7555 2.00375 13.3717 4.78625 14.2992C5.13625 14.3605 5.2675 14.1505 5.2675 13.9667C5.2675 13.8005 5.25875 13.2492 5.25875 12.663C3.5 12.9867 3.045 12.2342 2.905 11.8405C2.82625 11.6392 2.485 11.018 2.1875 10.8517C1.9425 10.7205 1.5925 10.3967 2.17875 10.388C2.73 10.3792 3.12375 10.8955 3.255 11.1055C3.885 12.1642 4.89125 11.8667 5.29375 11.683C5.355 11.228 5.53875 10.9217 5.74 10.7467C4.1825 10.5717 2.555 9.96799 2.555 7.29049C2.555 6.52924 2.82625 5.89924 3.2725 5.40924C3.2025 5.23424 2.9575 4.51674 3.3425 3.55424C3.3425 3.55424 3.92875 3.37049 5.2675 4.27174C5.8275 4.11424 6.4225 4.03549 7.0175 4.03549C7.6125 4.03549 8.2075 4.11424 8.7675 4.27174C10.1063 3.36174 10.6925 3.55424 10.6925 3.55424C11.0775 4.51674 10.8325 5.23424 10.7625 5.40924C11.2087 5.89924 11.48 6.52049 11.48 7.29049C11.48 9.97674 9.84375 10.5717 8.28625 10.7467C8.54 10.9655 8.75875 11.3855 8.75875 12.0417C8.75875 12.978 8.75 13.7305 8.75 13.9667C8.75 14.1505 8.88125 14.3692 9.23125 14.2992C10.6209 13.8301 11.8284 12.937 12.6839 11.7457C13.5393 10.5543 13.9996 9.12467 14 7.65799C14 3.79049 10.8675 0.65799 7 0.65799Z" fill="currentColor"/>
                        </svg>
                    </NuxtLink>
                </nav>
            </div>
        </div>
    </header>
</template>

<script setup>
const props = defineProps({
    fixed: {
        default: false
    }
});

const links = reactive([
    {
        url: 'https://serversideup.net',
        link: 'Blog'
    },
    {
        url: 'https://community.serversideup.net/',
        link: 'Community'
    },
    {
        url: 'https://serversideup.net/search/?type=all',
        link: 'Courses & Tutorials'
    }
]);

const showMenu = ref( false );
const menuRef = ref( null );
const toggleMenu = () => {
    showMenu.value = showMenu.value ? false : true;
}

onClickOutside( menuRef, (event) => {
    showMenu.value = false;
});
</script>