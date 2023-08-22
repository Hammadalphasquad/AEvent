<template>
  <div class="temp-modal flex flex-col gap-5 max-w-[245px] w-full">
    <div class="w-full flex items-center justify-between mb-5">
      <h4 class="font-medium text-base text-neutral-800 dark:text-neutral-200">Template</h4>
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
    <div class="border-b-[1px] pb-2 flex items-center justify-between">
      <p
        @click="$emit('toggle', 'heading')"
        class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
      >Heading</p>
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
              <rect width="20" height="20" fill="white" transform="translate(0 0.5)" />
            </clipPath>
          </defs>
        </svg>
      </span>
    </div>
    <div class="border-b-[1px] pb-2 flex items-center justify-between">
      <p
        @click="$emit('toggle', 'subheading')"
        class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
      >Sub Heading</p>
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
              <rect width="20" height="20" fill="white" transform="translate(0 0.5)" />
            </clipPath>
          </defs>
        </svg>
      </span>
    </div>
    <div class="border-b-[1px] pb-2 flex items-center justify-between">
      <p
        class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
      >Timer Text</p>
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
              <rect width="20" height="20" fill="white" transform="translate(0 0.5)" />
            </clipPath>
          </defs>
        </svg>
      </span>
    </div>
    <div class="border-b-[1px] pb-2 flex items-center justify-between">
      <p
        class="cursor-pointer font-medium text-base text-neutral-800 dark:text-neutral-200"
      >Pro Webinar Media</p>
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
              <rect width="20" height="20" fill="white" transform="translate(0 0.5)" />
            </clipPath>
          </defs>
        </svg>
      </span>
    </div>
  </div>
</template>
