<template>
  <div
    :class="`tp-offcanvas-area-2 tp-menu-2 ${isOffCanvasOpen ? 'opened' : ''}`"
  >
    <div class="tp-offcanvas-shape">
      <!-- <img class="tp-offcanvas-shape-2" src="/images/offcanvas/bg-shape-3.png" alt=""> -->
    </div>
    <div class="tp-offcanvas-circle-1">
      <span></span>
    </div>
    <div class="tp-offcanvas-circle-2">
      <span></span>
    </div>
    <div class="tp-offcanvas-wrapper">
      <div
        class="tp-offcanvas-top-2 d-flex align-items-center justify-content-between"
      >
        <!-- <div class="tp-offcanvas-logo-2">
          <a href="#">
            <img class="logo-white" src="/images/logo/logo.png" alt="" />
            <img class="logo-black" src="/images/logo/logo-black.png" alt="" />
          </a>
        </div> -->
        <div class="tp-offcanvas-close-2">
          <button
            @click="closeOffcanvas"
            class="tp-offcanvas-close-btn-2 tp-offcanvas-open-btn-2"
          >
            <svg-close />
          </button>
        </div>
      </div>
      <div class="tp-offcanvas-main-2">
        <div class="tp-offcanvas-content-2">
          <h3 class="tp-offcanvas-content-title-2">Hello There!</h3>
          <p>
            Let’s connect to explore how we can build the next big thing
            together.
          </p>
        </div>
        <div class="tp-main-menu-mobile d-lg-none">
          <nav>
            <offcanvas-menus />
          </nav>
        </div>
        <!-- <div class="tp-offcanvas-gallery">
          <div class="row gx-2">
            <div
              v-for="(imgSrc, i) in gallery_images"
              :key="i"
              class="col-md-3 col-3"
            >
              <div class="tp-offcanvas-gallery-img fix">
                <a href="#"><img :src="imgSrc" alt="" /></a>
              </div>
            </div>
          </div>
        </div> -->
        <div class="tp-offcanvas-contact-2">
          <h3 class="tp-offcanvas-contact-title-2">Information</h3>

          <ul>
            <li><a href="tel:+8801798581950">+8801798581950</a></li>
            <li>
              <a href="mailto:urmeakter02sm@gmail.com"
                >urmeakter02sm@gmail.com</a
              >
            </li>
            <li>
              <a href="mailto:toyahajannat@gmail.com">toyahajannat@gmail.com</a>
            </li>
            <li><a href="#">Mirpur 10, Dhaka, Bangladesh.</a></li>
          </ul>
        </div>
        <div class="tp-offcanvas-social-2">
          <h3 class="tp-offcanvas-contact-title-2">Follow Us</h3>
          <ul>
            <li>
              <a
                href="https://www.instagram.com/toyaha_jannat?igsh=MXNoeHVyeW11NW9ybw=="
              >
                <svg-instagram />
              </a>
            </li>
            <li>
              <a href="https://linkedin.com/in/urme-akter-0279a9241">
                <svg
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M6.94 6.5C6.94 7.33 6.27 8 5.44 8C4.61 8 3.94 7.33 3.94 6.5C3.94 5.67 4.61 5 5.44 5C6.27 5 6.94 5.67 6.94 6.5Z"
                    fill="currentColor"
                  />
                  <path d="M4 9H7V19H4V9Z" fill="currentColor" />
                  <path
                    d="M9 9H12V10.5C12.5 9.7 13.7 9 15 9C18 9 19 10.8 19 13.5V19H16V14C16 12.8 15.2 12 14.2 12C13.2 12 12.5 12.8 12.5 14V19H9V9Z"
                    fill="currentColor"
                  />
                </svg>
              </a>
            </li>
            <li>
              <a href="https://www.facebook.com/toyahajannat07?mibextid=ZbWKwL">
                <svg
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M14 9H16V6H14C12.34 6 11 7.34 11 9V11H9V14H11V21H14V14H16L17 11H14V9Z"
                    fill="currentColor"
                  />
                </svg>
              </a>
            </li>
            <li>
              <a href="https://wa.me/8801798581950">
                <svg
                  width="19"
                  height="19"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M20.52 3.48A11.82 11.82 0 0 0 12.01 0C5.38 0 .01 5.37.01 12c0 2.11.55 4.17 1.6 5.99L0 24l6.17-1.62A11.93 11.93 0 0 0 12 24c6.63 0 12-5.37 12-12 0-3.2-1.25-6.21-3.48-8.52ZM12 21.82c-1.82 0-3.6-.49-5.15-1.42l-.37-.22-3.66.96.98-3.57-.24-.37A9.82 9.82 0 0 1 2.18 12c0-5.41 4.41-9.82 9.82-9.82 2.62 0 5.08 1.02 6.93 2.87A9.73 9.73 0 0 1 21.82 12c0 5.41-4.41 9.82-9.82 9.82Zm5.4-7.36c-.29-.15-1.71-.84-1.98-.94-.27-.1-.46-.15-.66.15-.19.29-.75.94-.91 1.13-.17.19-.34.22-.63.07-.29-.15-1.21-.44-2.3-1.39-.85-.76-1.42-1.69-1.59-1.98-.17-.29-.02-.45.13-.6.13-.13.29-.34.44-.51.15-.17.19-.29.29-.49.1-.19.05-.37-.02-.51-.07-.15-.66-1.59-.91-2.18-.24-.57-.48-.49-.66-.5h-.56c-.19 0-.51.07-.78.37-.27.29-1.02 1-1.02 2.44 0 1.44 1.05 2.84 1.2 3.03.15.19 2.07 3.16 5.02 4.43.7.3 1.24.48 1.66.62.7.22 1.34.19 1.85.12.56-.08 1.71-.7 1.95-1.38.24-.68.24-1.26.17-1.38-.07-.12-.27-.19-.56-.34Z"
                    fill="currentColor"
                  />
                </svg>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
withDefaults(defineProps<{ isOffCanvasOpen: boolean }>(), {});
const emit = defineEmits();

const closeOffcanvas = () => {
  emit("closeOffcanvas");
};
const gallery_images = [
  "/images/offcanvas/offcanvas-1.jpg",
  "/images/offcanvas/offcanvas-2.jpg",
  "/images/offcanvas/offcanvas-3.jpg",
  "/images/offcanvas/offcanvas-2.jpg",
];
</script>
