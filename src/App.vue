<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    increaseCounter() {
      this.counter++;
    },
    decreaseCounter() {
      this.counter--;
    },
    clearCounter() {
      this.counter = 0;
      const num = document.getElementById('num_bd') as HTMLDivElement
      num.style.color = '#fff';
    },
    color1() {
      const num = document.getElementById('num_bd') as HTMLDivElement
      num.style.color = '#dc2626';
    },
    color2() {
      const num = document.getElementById('num_bd') as HTMLDivElement
      num.style.color = '#ea580c';
    },
    color3() {
      const num = document.getElementById('num_bd') as HTMLDivElement
      num.style.color = '#16a34a';
    },
    color4() {
      const num = document.getElementById('num_bd') as HTMLDivElement
      num.style.color = '#0891b2';
    },
    color5() {
      const num = document.getElementById('num_bd') as HTMLDivElement
      num.style.color = '#2563eb';
    },
  },
});
</script>

<template>
  <main class="bg-[#000]">
    <div class="absolute px-[30px] container lg:border lg:rounded-[8px] md:w-[55%] lg:w-[25%] top-[50%] left-[50%]">
      <div class="mx-auto text-center">
        <div id="num_bd" class="text-[#fff] font-[Poppins] font-[600] text-[140px]">{{ counter }}</div>
        <div class="bg-[#fff] mt-[50px] mx-auto w-full md:w-full py-[8px] px-[24px] rounded-[10px]"></div>
        <!--start counter sign function-->
        <div class="mx-auto space-x-[30px] text-center mt-[30px] flex justify-center">
          <!--counter sign function-->
          <div @click="increaseCounter"
            class="bg-[#f9fafb] cursor-pointer w-[50%] md:w-[50%] py-[8px] rounded-[3px] px-[30px]">
            <div class="font-[600] mx-auto text-[#18181b] text-[40px]">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6 mx-auto">
                <path fill-rule="evenodd"
                  d="M12 3.75a.75.75 0 01.75.75v6.75h6.75a.75.75 0 010 1.5h-6.75v6.75a.75.75 0 01-1.5 0v-6.75H4.5a.75.75 0 010-1.5h6.75V4.5a.75.75 0 01.75-.75z"
                  clip-rule="evenodd" />
              </svg>
            </div>
            <div class="font-[600] text-center text-[#18181b] text-[20px]">Add</div>
          </div>
          <!--sss-->
          <div @click="clearCounter"
            class="bg-[#f9fafb] cursor-pointer w-[50%] md:w-[50%] rounded-[3px] py-[8px] px-[30px]">
            <div class="font-[600] mx-auto text-[#18181b] text-[40px]">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6 mx-auto">
                <path fill-rule="evenodd"
                  d="M5.47 5.47a.75.75 0 011.06 0L12 10.94l5.47-5.47a.75.75 0 111.06 1.06L13.06 12l5.47 5.47a.75.75 0 11-1.06 1.06L12 13.06l-5.47 5.47a.75.75 0 01-1.06-1.06L10.94 12 5.47 6.53a.75.75 0 010-1.06z"
                  clip-rule="evenodd" />
              </svg>
            </div>
            <div class="font-[600] text-center text-[#18181b] text-[20px]">Clear</div>
          </div>
        </div>
        <!--end sign function-->
        <!--another one sss-->
        <div @click="decreaseCounter"
          class="bg-[#f9fafb] cursor-pointer mx-auto mt-[15px] block w-full py-[8px] rounded-[3px] px-[30px]">
          <div class="font-[600] mx-auto text-[#18181b] text-[40px]">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6 mx-auto">
              <path fill-rule="evenodd" d="M3.75 12a.75.75 0 01.75-.75h15a.75.75 0 010 1.5h-15a.75.75 0 01-.75-.75z"
                clip-rule="evenodd" />
            </svg>
          </div>
          <div class="font-[600] text-center text-[#18181b] text-[20px]">Subtract</div>
        </div>
        <!--another one ssss-->
        <!--end signature function-->
        <div class="mt-[30px] color_scroll flex overflow-scroll space-x-[20px] lg:mb-[40px] items-center">
          <div @click="color1" class="bg-[#dc2626] rounded-[12px] cursor-pointer h-[10px] py-[5px] px-[60px]"></div>
          <div @click="color2" class="bg-[#ea580c] rounded-[12px] cursor-pointer h-[10px] py-[5px] px-[60px]"></div>
          <div @click="color3" class="bg-[#16a34a] rounded-[12px] cursor-pointer h-[10px] py-[5px] px-[60px]"></div>
          <div @click="color4" class="bg-[#0891b2] rounded-[12px] cursor-pointer h-[10px] py-[5px] px-[60px]"></div>
          <div @click="color5" class="bg-[#2563eb] rounded-[12px] cursor-pointer h-[10px] py-[5px] px-[60px]"></div>
        </div>
        <!--color picker-->
      </div>
    </div>
    <!--end container-->
  </main>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

html {
  height: 100%;
}

body,
main {
  height: 100vh;
}

.container {
  transform: translate(-50%, -50%);
}

.color_scroll::-webkit-scrollbar {
  display: none;
}
</style>
