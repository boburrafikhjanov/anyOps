<script setup lang="ts">
import logo from '~/assets/icons/logo.svg'
import { menu } from '~/constants/menu'
</script>

<template>
  <header>
    <div class="px-[70px]">
      <div
        class="flex items-center py-[24px] border-b-[#ffffff1f] border-b-[1px]"
      >
        <NuxtLink to="/">
          <img :src="logo" alt="" />
        </NuxtLink>

        <nav
          class="hidden lg:flex mx-auto bg-[#ffffff0d] py-[10px] px-[45px] rounded-[50px] border-[1px] border-[#ffffff14]"
        >
          <ul class="flex items-center justify-between gap-[30px]">
            <li v-for="item in menu" :key="item.href">
              <NuxtLink
                :to="item.href"
                class="hover:text-[#0ABBB5] text-[16px] leading-[24px] font-medium"
              >
                {{ $t(item.label as string) }}
              </NuxtLink>
            </li>
          </ul>
        </nav>

        <div class="w-[140px] h-[29px] flex-none"></div>
      </div>
    </div>
  </header>
</template>
