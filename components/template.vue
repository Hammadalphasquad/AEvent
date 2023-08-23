<template>
  <div>
    <div>
      <img src="../public/images/pic-bg.jpg" />
    </div>
    <div
      class="hover:bg-sky-700 text-black text-lg font-bold absolute top-[400px] left-[850px] border-[2px] bg- border-black cursor-pointer p-5 rounded-lg"
    >
      <h1 @click="modalOpen">Open Modal</h1>
    </div>

    <div
      v-if="modal"
      class="fixed inset-0 z-10 w-full bg-black bg-opacity-30 backdrop-blur-sm"
    >
      <div
        class="absolute px-5 inset-0 py-6 m-auto max-w-[1450px] w-full max-h-[879px] overflow-auto shadow-xl rounded-lg bg-[#f5f5f5] flex justify-center gap-5"
      >
        <!-- Preview -->
        <div class="max-w-[1125px] w-full bg-white pb-8 rounded-xl">
          <p
            class="font-semibold text-base text-neutral-600 py-4 px-6 border-b border-neutral-200 dark:border-neutral-700"
          >
            Template Preview
          </p>

          <div
            :style="wallpaperStyle"
            class="bg-cover pt-16 rounded-2xl text-white pb-64 m-6"
          >
            <div class="text-center">
              <p
                :style="headingStyle"
                class="text-2xl rounded-xl py-1 mx-10 overflow-hidden"
              >
                {{ headingStyle.text }}
              </p>
              <p
                :style="subHeadingStyle"
                class="text-2xl py-1 my-5 rounded-xl mx-10 overflow-hidden"
              >
                {{ subHeadingStyle.text }}
              </p>
              <p
                :style="timerTextStyle"
                class="text-2xl py-1 rounded-xl mx-10 overflow-hidden"
              >
                {{ timerTextStyle.text }}
              </p>
              <p
                :style="proWebinarStyle"
                class="text-2xl py-1 my-5 rounded-xl mx-10 overflow-hidden"
              >
                {{ proWebinarStyle.text }}
              </p>
              <div
                class="rounded-xl overflow-hidden max-w-[260px] mx-auto mb-8"
              >
                <video autoplay muted loop>
                  <source
                    src="https://mazwai.com/videvo_files/video/free/2018-03/small_watermarked/180301_15_B_KowloonPark_06_preview.webm"
                    type="video/mp4"
                  />
                </video>
              </div>
            </div>
          </div>
        </div>

        <!-- Side-bar -->

        <!-- Elements -->
        <div
          v-if="show"
          class="temp-modal flex flex-col gap-5 max-w-[245px] w-full"
        >
          <div class="w-full flex items-center justify-between mb-5">
            <h4
              class="font-medium text-base text-neutral-800 dark:text-neutral-200"
            >
              Template
            </h4>
            <svg
              @click="modalClose"
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
          <div class="border-b-[1px] pb-2 flex items-center justify-between">
            <p
              @click="(show = false), (currentElementStyle = headingStyle)"
              class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
            >
              Heading
            </p>
            <span>
              <svg
                width="20"
                height="21"
                viewBox="0 0 20 21"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g clip-path="url(#clip0_1_15899)">
                  <path
                    d="M9.99967 12.1668C10.9201 12.1668 11.6663 11.4206 11.6663 10.5002C11.6663 9.57969 10.9201 8.8335 9.99967 8.8335C9.0792 8.8335 8.33301 9.57969 8.33301 10.5002C8.33301 11.4206 9.0792 12.1668 9.99967 12.1668Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M18.3337 10.4998C16.1112 14.389 13.3337 16.3332 10.0003 16.3332C6.66699 16.3332 3.88949 14.389 1.66699 10.4998C3.88949 6.61067 6.66699 4.6665 10.0003 4.6665C13.3337 4.6665 16.1112 6.61067 18.3337 10.4998Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_1_15899">
                    <rect
                      width="20"
                      height="20"
                      fill="white"
                      transform="translate(0 0.5)"
                    />
                  </clipPath>
                </defs>
              </svg>
            </span>
          </div>
          <div class="border-b-[1px] pb-2 flex items-center justify-between">
            <p
              @click="(show = false), (currentElementStyle = subHeadingStyle)"
              class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
            >
              Sub Heading
            </p>
            <span>
              <svg
                width="20"
                height="21"
                viewBox="0 0 20 21"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g clip-path="url(#clip0_1_15899)">
                  <path
                    d="M9.99967 12.1668C10.9201 12.1668 11.6663 11.4206 11.6663 10.5002C11.6663 9.57969 10.9201 8.8335 9.99967 8.8335C9.0792 8.8335 8.33301 9.57969 8.33301 10.5002C8.33301 11.4206 9.0792 12.1668 9.99967 12.1668Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M18.3337 10.4998C16.1112 14.389 13.3337 16.3332 10.0003 16.3332C6.66699 16.3332 3.88949 14.389 1.66699 10.4998C3.88949 6.61067 6.66699 4.6665 10.0003 4.6665C13.3337 4.6665 16.1112 6.61067 18.3337 10.4998Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_1_15899">
                    <rect
                      width="20"
                      height="20"
                      fill="white"
                      transform="translate(0 0.5)"
                    />
                  </clipPath>
                </defs>
              </svg>
            </span>
          </div>
          <div class="border-b-[1px] pb-2 flex items-center justify-between">
            <p
              @click="(show = false)((currentElementStyle = timerTextStyle))"
              class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
            >
              Timer Text
            </p>
            <span>
              <svg
                width="20"
                height="21"
                viewBox="0 0 20 21"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g clip-path="url(#clip0_1_15899)">
                  <path
                    d="M9.99967 12.1668C10.9201 12.1668 11.6663 11.4206 11.6663 10.5002C11.6663 9.57969 10.9201 8.8335 9.99967 8.8335C9.0792 8.8335 8.33301 9.57969 8.33301 10.5002C8.33301 11.4206 9.0792 12.1668 9.99967 12.1668Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M18.3337 10.4998C16.1112 14.389 13.3337 16.3332 10.0003 16.3332C6.66699 16.3332 3.88949 14.389 1.66699 10.4998C3.88949 6.61067 6.66699 4.6665 10.0003 4.6665C13.3337 4.6665 16.1112 6.61067 18.3337 10.4998Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_1_15899">
                    <rect
                      width="20"
                      height="20"
                      fill="white"
                      transform="translate(0 0.5)"
                    />
                  </clipPath>
                </defs>
              </svg>
            </span>
          </div>
          <div class="border-b-[1px] pb-2 flex items-center justify-between">
            <p
              @click="(show = false)((currentElementStyle = proWebinarStyle))"
              class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
            >
              Pro Webinar Media
            </p>
            <span>
              <svg
                width="20"
                height="21"
                viewBox="0 0 20 21"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g clip-path="url(#clip0_1_15899)">
                  <path
                    d="M9.99967 12.1668C10.9201 12.1668 11.6663 11.4206 11.6663 10.5002C11.6663 9.57969 10.9201 8.8335 9.99967 8.8335C9.0792 8.8335 8.33301 9.57969 8.33301 10.5002C8.33301 11.4206 9.0792 12.1668 9.99967 12.1668Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                  <path
                    d="M18.3337 10.4998C16.1112 14.389 13.3337 16.3332 10.0003 16.3332C6.66699 16.3332 3.88949 14.389 1.66699 10.4998C3.88949 6.61067 6.66699 4.6665 10.0003 4.6665C13.3337 4.6665 16.1112 6.61067 18.3337 10.4998Z"
                    stroke="#52525B"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  />
                </g>
                <defs>
                  <clipPath id="clip0_1_15899">
                    <rect
                      width="20"
                      height="20"
                      fill="white"
                      transform="translate(0 0.5)"
                    />
                  </clipPath>
                </defs>
              </svg>
            </span>
          </div>
        </div>

        <!-- Edit elements -->
        <div
          v-else
          class="flex max-w-[245px] flex-col gap-3 font-medium pr-1 overflow-scroll"
        >
          <div class="w-full flex items-center justify-between mb-7">
            <div
              class="flex items-center gap-1 cursor-pointer text-neutral-800 dark:text-neutral-200"
            >
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
                @click="show = true"
                class="font-semibold text-base leading-none text-neutral-600 dark:text-neutral-400"
              >
                Back
              </p>
            </div>
            <svg
            @click="modalClose"

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
              v-model="currentElementStyle.text"
              class="px-5 font-normal text-sm text-neutral-600 outline-none resize-none placeholder:text-neutral-400 dark:placeholder:text-neutral-400 bg-white dark:bg-neutral-800 dark:text-neutral-400 border border-neutral-300 dark:border-neutral-700 bg-transparent transition-all ease-in-out duration-150 hover:border-neutral-400 w-full py-3 focus:border-blue-600 pb-10 pt-3 rounded-lg"
              placeholder="This is your Opening Room Headline"
            ></textarea>
          </div>
          <p class="font-semibold text-sm text-neutral-800">Font Family</p>
          <select
            v-model="currentElementStyle.fontFamily"
            class="font-normal text-sm text-neutral-600 transition-all ease-in-out duration-150 hover:border-neutral-400 rounded-lg border-[#d4d4d4] border-[1px] py-3 px-2"
            name="Cursive"
          >
            <option class="dropd">Cursive</option>
            <option class="dropd">Sans Serif</option>
            <option class="dropd">Courier New</option>
          </select>

          <p class="font-semibold text-sm text-neutral-800">Wallpaper</p>
          <select
            v-model="wallpaperStyle.backgroundImage"
            class="font-normal text-sm text-neutral-600 transition-all ease-in-out duration-150 hover:border-neutral-400 rounded-lg border-[#d4d4d4] border-[1px] py-3 px-2"
          >
            <option
              value="url(https://tuk-cdn.s3.amazonaws.com/can-uploader/background1.png)"
            >
              Wallpaper no 1
            </option>
            <option
              value="url(https://tuk-cdn.s3.amazonaws.com/can-uploader/backgroundimageno1.png)"
            >
              Wallpaper no 2
            </option>
            <option
              value="url(https://tuk-cdn.s3.amazonaws.com/can-uploader/backgroundimage.png)"
            >
              Wallpaper no 3
            </option>
          </select>

          <p class="font-semibold text-sm text-neutral-800">Font Weight</p>
          <select
            v-model="currentElementStyle.fontWeight"
            class="font-normal text-sm text-neutral-600 transition-all ease-in-out duration-150 hover:border-neutral-400 rounded-lg border-[#d4d4d4] border-[1px] py-3 px-2"
            placeholder="Bold"
          >
            <option>Normal</option>
            <option>Bold</option>
          </select>
          <p class="font-semibold text-sm text-neutral-800">Font Size</p>
          <div class="flex items-center gap-2">
            <div class="w-full">
              <input
                type="text"
                v-model="currentElementStyle.fontSize"
                placeholder="14"
                class="font-normal text-sm text-neutral-600 outline-none placeholder:text-neutral-400 dark:placeholder:text-neutral-400 bg-white dark:bg-neutral-800 dark:text-neutral-400 border border-neutral-300 dark:border-neutral-700 bg-transparent transition-all ease-in-out duration-150 hover:border-neutral-400 w-full rounded-md px-4 py-3 focus:border-blue-600"
                autocomplete="off"
              />
            </div>
            <p
              class="px-4 py-[15px] bg-neutral-100 dark:bg-neutral-900 border box-border border-neutral-200 dark:border-neutral-700 rounded font-normal text-sm leading-none text-neutral-600 dark:text-neutral-400"
            >
              px
            </p>
          </div>
          <p class="font-semibold text-sm text-neutral-800">Font Color</p>
          <div class="flex items-center gap-5">
            <div class="h-full rounded">
              <div
                class="h-full rounded-md border dark:border-neutral-700 box-border"
                style="background-color: rgb(0, 0, 0)"
              >
                <input
                  v-model="currentElementStyle.color"
                  type="color"
                  class="opacity-0 cursor-pointer h-full"
                />
              </div>
            </div>
            <div class="flex">
              <select
                class="font-normal text-sm text-neutral-600 border-[#e5e5e5] border-[1px] bg-[#d4d4d4] py-2 px-3 rounded-l-lg"
              >
                <option>HEX</option>
              </select>
              <input
                v-model="currentElementStyle.color"
                type="text"
                class="text-base font-normal outline-none rounded-r-lg transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 border-[1px] py-2 px-1 max-w-[75px]"
              />
            </div>
          </div>
          <p class="font-semibold text-sm text-neutral-800">BG Color</p>
          <div class="flex items-center gap-5">
            <div class="h-full rounded">
              <div
                class="h-full rounded-md border dark:border-neutral-700 box-border"
                style="background-color: rgb(255, 255, 255)"
              >
                <input
                  v-model="currentElementStyle.backgroundColor"
                  type="color"
                  class="opacity-0 cursor-pointer h-full"
                />
              </div>
            </div>
            <div class="flex">
              <select
                class="font-normal text-sm text-neutral-600 border-[#e5e5e5] border-[1px] bg-[#d4d4d4] py-2 px-3 rounded-l-lg"
              >
                <option>HEX</option>
              </select>
              <input
                v-model="currentElementStyle.backgroundColor"
                type="text"
                class="text-base font-normal outline-none rounded-r-lg transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 border-[1px] py-2 px-1 max-w-[75px]"
              />
            </div>
          </div>
          <p class="font-semibold text-sm text-neutral-800">Padding</p>
          <div class="grid max-w-[250px] grid-cols-2 gap-3">
            <div class="flex">
              <p
                class="border-[#e5e5e5] border-[1px] py-2 px-[19px] rounded-l-lg font-normal text-sm text-neutral-600"
              >
                Top
              </p>
              <input
                v-model="currentElementStyle.paddingTop"
                type="text"
                class="text-base font-normal outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[50px]"
              />
            </div>
            <div class="flex">
              <p
                class="border-[#e5e5e5] border-[1px] py-2 px-4 rounded-l-lg font-normal text-sm text-neutral-600"
              >
                Left
              </p>
              <input
                v-model="currentElementStyle.paddingLeft"
                type="text"
                class="text-base font-normal outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[50px]"
              />
            </div>
            <div class="flex">
              <p
                class="border-[#e5e5e5] border-[1px] py-2 px-2 rounded-l-lg font-normal text-sm text-neutral-600"
              >
                Bottom
              </p>
              <input
                v-model="currentElementStyle.paddingBottom"
                type="text"
                class="text-base font-normal outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[50px]"
              />
            </div>
            <div class="flex">
              <p
                class="border-[#e5e5e5] border-[1px] py-2 px-[11px] rounded-l-lg font-normal text-sm text-neutral-600"
              >
                Right
              </p>
              <input
                v-model="currentElementStyle.paddingRight"
                type="text"
                class="text-base font-normal outline-none transition-all ease-in-out duration-150 hover:border-neutral-400 focus:border-blue-600 rounded-r-lg border-[#d4d4d4] border-[1px] py-2 px-1 max-w-[50px]"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const show = ref(true);
const modal = ref(false);

const modalClose = () => {
  modal.value = false;
};
const modalOpen = () => {
  modal.value = true;
};

const imageBackground = ref(
  "url(https://tuk-cdn.s3.amazonaws.com/can-uploader/background.png)"
);

// const updateCurrentElementStyle = (event) => {
//   imageBackground = event.target.value;
// };
const headingStyle = ref({
  text: "Hi there its me, am building dynamic builder",
  fontSize: "18px",
  fontFamily: "Cursive",
  fontWeight: "Bold",
  color: "#ffffff",
  backgroundColor: "",
  paddingTop: "2px",
  paddingLeft: "2px",
  paddingBottom: "2px",
  paddingRight: "2px",
});
const currentElementStyle = ref(headingStyle.value);

const subHeadingStyle = ref({
  text: "Here is Sub Headline",
  fontSize: "18px",
  fontFamily: "cursive",
  fontWeight: "bold",
  color: "#ffffff",
  backgroundColor: "",
  paddingTop: "",
  paddingLeft: "",
  paddingBottom: "",
  paddingRight: "",
});
const timerTextStyle = ref({
  text: "Here is TimerText",
  fontSize: "18px",
  fontFamily: "cursive",
  fontWeight: "bold",
  color: "#ffffff",
  backgroundColor: "",
  paddingTop: "",
  paddingLeft: "",
  paddingBottom: "",
  paddingRight: "",
});
const proWebinarStyle = ref({
  text: "Here is ProWebinar",
  fontSize: "18px",
  fontFamily: "cursive",
  fontWeight: "bold",
  color: "#ffffff",
  backgroundColor: "",
  paddingTop: "",
  paddingLeft: "",
  paddingBottom: "",
  paddingRight: "",
});

const wallpaperStyle = ref({
  backgroundImage: imageBackground.value,
});
// const currentbackGroundrStyle = ref(wallpaperStyle.value);
</script>
<style scoped>
/* .background-img {
  background-image: url(https://tuk-cdn.s3.amazonaws.com/can-uploader/background.png);
  background-size: cover;
} */
</style>
<style scoped>
select:required:invalid {
  color: #666;
}
option[value=""][disabled] {
  display: none;
}
option {
  color: #000;
}
</style>
