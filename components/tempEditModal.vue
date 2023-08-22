


<template>
  <div class="mx-auto">
  <background/>
   <div class="fixed inset-0 h-screen z-60 w-full bg-black bg-opacity-30 backdrop-blur-sm">
      <div
        class="absolute px-5 inset-0 py-6 m-auto max-w-[1450px] w-full h-[879px] overflow-auto content-scroll shadow-xl rounded-lg bg-[#f5f5f5] flex justify-center gap-7"
      >
    <TempPreview :templateData="templateData" />
       <TempModal />
    <div class="flex flex-col gap-3 font-medium">
      <div class="w-full flex items-center justify-between mb-7">
        <div class="flex items-center gap-1 cursor-pointer text-neutral-800 dark:text-neutral-200">
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M15 18L9 12L15 6"
              stroke="currentColor"
              stroke-width="1.2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
          <p
            class="font-semibold text-base leading-none text-neutral-600 dark:text-neutral-400"
          >Back</p>
        </div>
        <svg
          class="cursor-pointer text-neutral-800 dark:text-neutral-200"
          width="11"
          height="12"
          viewBox="0 0 11 12"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0.575736 10.5757C0.341421 10.8101 0.341421 11.1899 0.575736 11.4243C0.810051 11.6586 1.18995 11.6586 1.42426 11.4243L0.575736 10.5757ZM6.42426 6.42426C6.65858 6.18995 6.65858 5.81005 6.42426 5.57574C6.18995 5.34142 5.81005 5.34142 5.57574 5.57574L6.42426 6.42426ZM5.57574 5.57574C5.34142 5.81005 5.34142 6.18995 5.57574 6.42426C5.81005 6.65858 6.18995 6.65858 6.42426 6.42426L5.57574 5.57574ZM11.4243 1.42426C11.6586 1.18995 11.6586 0.810051 11.4243 0.575736C11.1899 0.341421 10.8101 0.341421 10.5757 0.575736L11.4243 1.42426ZM6.42426 5.57574C6.18995 5.34142 5.81005 5.34142 5.57574 5.57574C5.34142 5.81005 5.34142 6.18995 5.57574 6.42426L6.42426 5.57574ZM10.5757 11.4243C10.8101 11.6586 11.1899 11.6586 11.4243 11.4243C11.6586 11.1899 11.6586 10.8101 11.4243 10.5757L10.5757 11.4243ZM5.57574 6.42426C5.81005 6.65858 6.18995 6.65858 6.42426 6.42426C6.65858 6.18995 6.65858 5.81005 6.42426 5.57574L5.57574 6.42426ZM1.42426 0.575736C1.18995 0.341421 0.810051 0.341421 0.575736 0.575736C0.341421 0.810051 0.341421 1.18995 0.575736 1.42426L1.42426 0.575736ZM1.42426 11.4243L6.42426 6.42426L5.57574 5.57574L0.575736 10.5757L1.42426 11.4243ZM6.42426 6.42426L11.4243 1.42426L10.5757 0.575736L5.57574 5.57574L6.42426 6.42426ZM5.57574 6.42426L10.5757 11.4243L11.4243 10.5757L6.42426 5.57574L5.57574 6.42426ZM6.42426 5.57574L1.42426 0.575736L0.575736 1.42426L5.57574 6.42426L6.42426 5.57574Z"
            fill="currentColor"
          />
        </svg>
      </div>
      <p class="font-semibold">Edit Heading settings</p>
      <p class="font-semibold text-sm text-neutral-800">Text</p>
      <div class>
        <textarea
          v-model="templateData.headline"
          class="font-normal text-sm text-neutral-600 outline-none resize-none placeholder:text-neutral-400 dark:placeholder:text-neutral-400 bg-white dark:bg-neutral-800 dark:text-neutral-400 border border-neutral-300 dark:border-neutral-700 bg-transparent transition-all ease-in-out duration-150 hover:border-neutral-400 w-full py-3 focus:border-blue-600 px-5 pb-10 pt-3 rounded-lg"
          placeholder="This is your Opening Room Headline"
        ></textarea>
      </div>
      <p class="font-semibold text-sm text-neutral-800">Font Family</p>
      <select
        class="font-normal text-sm text-neutral-600 transition-all ease-in-out duration-150 hover:border-neutral-400 rounded-lg border-[#d4d4d4] border-[1px] py-3 px-2"
      >
        <option>Cursive</option>
        <option>Sans Serif</option>
        <option>Serif</option>
      </select>
      <p class="font-semibold text-sm text-neutral-800">Font Weight</p>
      <select
        class="font-normal text-sm text-neutral-600 transition-all ease-in-out duration-150 hover:border-neutral-400 rounded-lg border-[#d4d4d4] border-[1px] py-3 px-2"
      >
        <option>Normal</option>
        <option>Bold</option>
      </select>
      <p class="font-semibold text-sm text-neutral-800">Font Size</p>
      <div class="flex items-center gap-2">
        <div class="w-full">
          <input
            type="text"
            placeholder="14"
            class="font-normal text-sm text-neutral-600 outline-none placeholder:text-neutral-400 dark:placeholder:text-neutral-400 bg-white dark:bg-neutral-800 dark:text-neutral-400 border border-neutral-300 dark:border-neutral-700 bg-transparent transition-all ease-in-out duration-150 hover:border-neutral-400 w-full rounded-md px-4 py-3 focus:border-blue-600"
            autocomplete="off"
          />
        </div>
        <p
          class="px-4 py-[15px] bg-neutral-100 dark:bg-neutral-900 border box-border border-neutral-200 dark:border-neutral-700 rounded font-normal text-sm leading-none text-neutral-600 dark:text-neutral-400"
        >px</p>
      </div>
      <p class="font-semibold text-sm text-neutral-800">Font Color</p>
      <div class="flex items-center gap-5">
        <div class="h-full rounded">
          <div
            class="h-full rounded-md border dark:border-neutral-700 box-border"
            style="background-color: rgb(0, 0, 0);"
          >
            <input type="color" class="opacity-0 cursor-pointer h-full" />
          </div>
        </div>
        <div class="flex">
          <select
            class="font-normal text-sm text-neutral-600 border-[#e5e5e5] border-[1px] bg-[#d4d4d4] py-2 px-3 rounded-l-lg"
          >
            <option>HEX</option>
          </select>
          <input
            type="text"
            class="outline-none rounded-r-lg transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 border-[1px] py-2 px-1 max-w-[50px]"
          />
        </div>
      </div>
      <p class="font-semibold text-sm text-neutral-800">BG Color</p>
      <div class="flex items-center gap-5">
        <div class="h-full rounded">
          <div
            class="h-full rounded-md border dark:border-neutral-700 box-border"
            style="background-color: rgb(255, 255, 255);"
          >
            <input type="color" class="opacity-0 cursor-pointer h-full" />
          </div>
        </div>
        <div class="flex">
          <select
            class="font-normal text-sm text-neutral-600 border-[#e5e5e5] border-[1px] bg-[#d4d4d4] py-2 px-3 rounded-l-lg"
          >
            <option>HEX</option>
          </select>
          <input
            type="text"
            class="outline-none rounded-r-lg transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 border-[1px] py-2 px-1 max-w-[50px]"
          />
        </div>
      </div>
      <p class="font-semibold text-sm text-neutral-800">Padding</p>
      <div class="grid max-w-[250px] grid-cols-2 gap-3">
        <div class="flex">
          <p
            class="border-[#e5e5e5] border-[1px] py-2 px-4 rounded-l-lg font-normal text-sm text-neutral-600"
          >Top</p>
          <input
            type="text"
            class="outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[60px]"
          />
        </div>
        <div class="flex">
          <p
            class="border-[#e5e5e5] border-[1px] py-2 px-4 rounded-l-lg font-normal text-sm text-neutral-600"
          >Left</p>
          <input
            type="text"
            class="outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[50px]"
          />
        </div>
        <div class="flex">
          <p
            class="border-[#e5e5e5] border-[1px] py-2 px-4 rounded-l-lg font-normal text-sm text-neutral-600"
          >Top</p>
          <input
            type="text"
            class="outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[60px]"
          />
        </div>
        <div class="flex">
          <p
            class="border-[#e5e5e5] border-[1px] py-2 px-4 rounded-l-lg font-normal text-sm text-neutral-600"
          >Left</p>
          <input
            type="text"
            class="outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[50px]"
          />
        </div>
      </div>
    </div>
  </div>
  </div>
  </div>
</template>
<script setup>
const templateData = ref({
  headline: "Hi there its me, am building dynamic builder",
  subHeadline: "Here is sub headline",
  timmerText: "Here is dummy data"
});
</script>

<style >
</style>