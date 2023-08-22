<template>
  <div class="max-w-[1125px] w-full bg-white pb-8 rounded-xl">
    <p
      class="font-semibold text-base text-neutral-600 py-4 px-6 border-b border-neutral-200 dark:border-neutral-700"
    >Template Preview</p>
    <div class="pt-16 rounded-2xl background-img text-white pb-64 m-6">
      <div class="temp-prev text-center">
        <p class="pb-10 text-2xl">{{ templateData.headline }}</p>
        <p class="pb-10 text-2xl">{{templateData.subHeadline }}</p>
        <p class="pb-10 text-2xl">{{ templateData.timmerText }}</p>
        <div class="rounded-xl overflow-hidden max-w-[260px] mx-auto mb-8">
          <video autoplay muted loop>
            <source
              src="https://mazwai.com/videvo_files/video/free/2018-03/small_watermarked/180301_15_B_KowloonPark_06_preview.webm"
              type="video/mp4"
            />
          </video>
        </div>
       
        <button></button>
      </div>
    </div>
  </div>
</template>
<script setup>

const props = defineProps({
  templateData: String
});

</script>