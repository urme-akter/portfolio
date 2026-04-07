<!-- <template>
  <template v-if="!style_2">
    <div
      v-for="item in footer_social"
      :key="item.id"
      class="col-xl-4 col-lg-4 col-md-6 mb-30"
    >
      <a href="#">
        <div
          class="tp-footer-social-item d-flex align-items-center justify-content-between"
        >
          <span class="tp-footer-anim-border"></span>
          <div class="tp-footer-social-text z-index-1">
            <span class="child-1">{{ item.name }}</span>
            <span class="child-2">{{ item.title }}</span>
          </div>
          <div class="tp-footer-social-icon z-index-1">
            <span v-html="item.icon"></span>
          </div>
        </div>
      </a>
    </div>
  </template>

  <div v-if="style_2" class="tp-footer-4__social">
    <a v-for="s in social_2" :key="s.id" :href="s.link" target="_blank">
      <span v-html="s.icon"></span>
    </a>
  </div>
</template> -->

<template v-if="!style_2">
  <div
    v-for="item in footer_social"
    :key="item.id"
    class="col-xl-4 col-lg-4 col-md-6 mb-30"
  >
    <a :href="item.link" target="_blank">
      <div
        class="tp-footer-social-item d-flex align-items-center justify-content-between"
      >
        <span class="tp-footer-anim-border"></span>
        <div class="tp-footer-social-text z-index-1">
          <span class="child-1">{{ item.name }}</span>
          <span class="child-2">{{ item.title }}</span>
        </div>
        <div class="tp-footer-social-icon z-index-1">
          <span v-html="item.icon"></span>
        </div>
      </div>
    </a>
  </div>
</template>
<script setup lang="ts">
defineProps<{ style_2?: boolean }>();
const footer_social = [
  {
    id: 1,
    name: "Whatsapp",
    title: "",
    link: "https://wa.me/8801798581950",
    icon: `<svg width="19" height="19" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M20.52 3.48A11.82 11.82 0 0 0 12.01 0C5.38 0 .01 5.37.01 12c0 2.11.55 4.17 1.6 5.99L0 24l6.17-1.62A11.93 11.93 0 0 0 12 24c6.63 0 12-5.37 12-12 0-3.2-1.25-6.21-3.48-8.52ZM12 21.82c-1.82 0-3.6-.49-5.15-1.42l-.37-.22-3.66.96.98-3.57-.24-.37A9.82 9.82 0 0 1 2.18 12c0-5.41 4.41-9.82 9.82-9.82 2.62 0 5.08 1.02 6.93 2.87A9.73 9.73 0 0 1 21.82 12c0 5.41-4.41 9.82-9.82 9.82Zm5.4-7.36c-.29-.15-1.71-.84-1.98-.94-.27-.1-.46-.15-.66.15-.19.29-.75.94-.91 1.13-.17.19-.34.22-.63.07-.29-.15-1.21-.44-2.3-1.39-.85-.76-1.42-1.69-1.59-1.98-.17-.29-.02-.45.13-.6.13-.13.29-.34.44-.51.15-.17.19-.29.29-.49.1-.19.05-.37-.02-.51-.07-.15-.66-1.59-.91-2.18-.24-.57-.48-.49-.66-.5h-.56c-.19 0-.51.07-.78.37-.27.29-1.02 1-1.02 2.44 0 1.44 1.05 2.84 1.2 3.03.15.19 2.07 3.16 5.02 4.43.7.3 1.24.48 1.66.62.7.22 1.34.19 1.85.12.56-.08 1.71-.7 1.95-1.38.24-.68.24-1.26.17-1.38-.07-.12-.27-.19-.56-.34Z" fill="currentColor"/>
  </svg>`,
  },
  {
    id: 2,
    name: "Gmail",
    title: "",
    link: "mailto:urmeakter02sm@gmail.com",
    icon: `<svg width="18" height="18" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M2 6.5L12 13.5L22 6.5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    <path d="M3.5 5H20.5C21.33 5 22 5.67 22 6.5V17.5C22 18.33 21.33 19 20.5 19H3.5C2.67 19 2 18.33 2 17.5V6.5C2 5.67 2.67 5 3.5 5Z" stroke="currentColor" stroke-width="1.5"/>
  </svg>`,
  },
  {
    id: 3,
    name: "Phone",
    title: "",
    link: "tel:+8801798581950",
    icon: `<svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M22 16.92V20C22 20.55 21.55 21 21 21C10.51 21 3 13.49 3 3C3 2.45 3.45 2 4 2H7.09C7.57 2 7.99 2.34 8.07 2.81L8.57 6.11C8.65 6.57 8.44 7.03 8.03 7.26L5.91 8.5C7.23 11.09 9.91 13.77 12.5 15.09L13.74 12.97C13.97 12.56 14.43 12.35 14.89 12.43L18.19 12.93C18.66 13.01 19 13.43 19 13.91V16.92C19 17.47 18.55 17.92 18 17.92H22Z" fill="currentColor"/>
  </svg>`,
  },
];

const social_2 = [
  {
    id: 1,
    link: "https://www.behance.net",
    icon: `<svg width="17" height="15" viewBox="0 0 17 15" fill="none" xmlns="http://www.w3.org/2000/svg"> <path d="M12.25 13.75H4.75C2.5 13.75 1 12.625 1 10V4.75C1 2.125 2.5 1 4.75 1L12.25 1C14.5 1 16 2.125 16 4.75V10C16 12.625 14.5 13.75 12.25 13.75Z" stroke="currentcolor" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round" /> <path d="M12.25 5.12488L9.9025 6.99988C9.13 7.61488 7.8625 7.61488 7.09 6.99988L4.75 5.12488" stroke="currentcolor" stroke-width="1.5" stroke-miterlimit="10"  stroke-linecap="round" stroke-linejoin="round" /></svg>`,
  },
  {
    id: 2,
    link: "https://www.dribbble.com",
    icon: `<svg width="18" height="17" viewBox="0 0 18 17" fill="none" xmlns="http://www.w3.org/2000/svg"> <path d="M2.50589 12.2494C4.57662 15.836 9.16278 17.0648 12.7494 14.9941C14.2113 14.15 15.2816 12.888 15.8962 11.4461C16.7895 9.35066 16.7208 6.87526 15.4941 4.75063C14.2674 2.62599 12.1581 1.32872 9.89669 1.05462C8.34063 0.866 6.71259 1.16183 5.25063 2.00589C1.66403 4.07662 0.435172 8.66278 2.50589 12.2494Z" stroke="currentcolor" stroke-width="1.5" /> <path d="M12.712 14.9291C12.712 14.9291 12.0079 9.98655 10.5004 7.37547C8.99289 4.76439 5.28862 2.07143 5.28862 2.07143M5.68375 15.1123C6.79479 11.7605 12.3392 8.04512 16.3967 8.93525M12.3103 1.90808C11.1945 5.22332 5.75659 8.88441 1.71802 8.08903" stroke="currentcolor" stroke-width="1.5" stroke-linecap="round" /> </svg>`,
  },
  {
    id: 3,
    link: "mailto:xyz@example.com",
    icon: `<svg width="17" height="11" viewBox="0 0 17 11" fill="none" xmlns="http://www.w3.org/2000/svg"> <path d="M1 5.50008H6.25009C7.52511 5.50008 8.50013 6.47509 8.50013 7.75012C8.50013 9.02514 7.52511 10.0002 6.25009 10.0002H1.75001C1.30001 10.0002 1 9.70015 1 9.25014V1.75001C1 1.30001 1.30001 1 1.75001 1H5.50008C6.7751 1 7.75012 1.97502 7.75012 3.25004C7.75012 4.52506 6.7751 5.50008 5.50008 5.50008H1Z" stroke="currentcolor" stroke-width="1.5" stroke-miterlimit="10" /> <path d="M9.99988 7.00005H16C16 5.35002 14.65 4 12.9999 4C11.3499 4 9.99988 5.35002 9.99988 7.00005ZM9.99988 7.00005C9.99988 8.65008 11.3499 10.0001 12.9999 10.0001H14.275" stroke="currentcolor" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round" /> <path d="M14.1249 2.125H11.8749" stroke="currentcolor" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round" /> </svg>`,
  },
  {
    id: 4,
    link: "https://www.youtube.com",
    icon: `<svg width="18" height="14" viewBox="0 0 18 14" fill="none" xmlns="http://www.w3.org/2000/svg"> <path d="M12.75 13H5.25C3 13 1.5 11.5 1.5 9.25V4.75C1.5 2.5 3 1 5.25 1H12.75C15 1 16.5 2.5 16.5 4.75V9.25C16.5 11.5 15 13 12.75 13Z" stroke="currentcolor" stroke-width="1.5" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round" /> <path d="M8.70822 5.14898L10.802 6.40526C11.5558 6.90777 11.5558 7.66154 10.802 8.16405L8.70822 9.42033C7.8707 9.92285 7.20068 9.50409 7.20068 8.58281V6.07025C7.20068 4.98147 7.8707 4.64646 8.70822 5.14898Z" fill="currentcolor" /> </svg>`,
  },
];
</script>
