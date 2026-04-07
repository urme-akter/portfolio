<template>
  <section
    class="tp-skill-area pt-115 pb-105 p-relative z-index-1 fix theme-bg-2"
    style="background-image: url(/images/skill/bg-distort.png)"
  >
    <div class="tp-skill-shape">
      <span class="tp-skill-shape-1"></span>
      <span class="tp-skill-shape-2"></span>
    </div>

    <div class="container">
      <!-- Title -->
      <div class="row">
        <div class="col-xl-12">
          <div class="tp-skill-section-title">
            <div
              class="tp-section-title-wrapper tp_text_anim mb-30 text-center"
            >
              <div class="tp-section-title-inner tp_title_anim p-relative">
                <span class="tp-section-subtitle">Advantage</span>
                <h3 class="tp-section-title">Skills</h3>
              </div>
              <p>
                I build fast, responsive, and scalable front-end experiences.
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Tabs -->
      <div class="row">
        <div class="col-xl-12">
          <div
            class="tp-skill-tab tp-tab d-flex align-items-center justify-content-center mb-70"
          >
            <nav>
              <div
                class="nav nav-tabs tp-marker-tab"
                id="nav-tab"
                role="tablist"
              >
                <button
                  class="nav-link active"
                  id="nav-hard-tab"
                  data-bs-toggle="tab"
                  data-bs-target="#nav-hard"
                  type="button"
                  role="tab"
                >
                  Hard Skills
                </button>

                <button
                  class="nav-link"
                  id="nav-soft-tab"
                  data-bs-toggle="tab"
                  data-bs-target="#nav-soft"
                  type="button"
                  role="tab"
                >
                  Soft Skills
                </button>

                <span id="lineMarker"></span>
              </div>
            </nav>
          </div>
        </div>
      </div>

      <!-- Content -->
      <div class="row">
        <div class="col-xl-12">
          <div class="tab-content" id="nav-tabContent">
            <div
              v-for="(item, i) in skill_data"
              :key="i"
              :class="`tab-pane fade ${item.active ? 'show active' : ''}`"
              :id="`nav-${item.tab_id}`"
              role="tabpanel"
            >
              <div class="tp-skill-tab-content tp-skill-radius">
                <div class="row">
                  <!-- ✅ Soft skill description -->
                  <div v-if="item.description" class="col-12 text-center mb-40">
                    <p
                      class="text-white text-lg leading-relaxed max-w-2xl mx-auto"
                    >
                      {{ item.description }}
                    </p>
                  </div>

                  <!-- ✅ Hard skill items -->
                  <template v-if="item.items && item.items.length">
                    <div
                      v-for="(s, index) in item.items"
                      :key="index"
                      class="col-xl-2 col-lg-3 col-md-3 col-6"
                    >
                      <div class="tp-skill-item text-center">
                        <div
                          class="tp-skill-thumb d-flex align-items-center justify-content-center flex-column"
                        >
                          <div class="tp-skill-icon">
                            <span>
                              <img :src="s.img" alt="" />
                            </span>
                          </div>
                        </div>

                        <div class="tp-skill-content">
                          <h3 class="tp-skill-title">
                            {{ s.title }}
                          </h3>
                        </div>
                      </div>
                    </div>
                  </template>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const { tpTabLine2 } = useTabLine();

const skill_data = [
  {
    tab_id: "hard",
    active: true,
    items: [
      { img: "/images/skill/react.png", title: "React.js" },
      { img: "/images/skill/next.png", title: "Next.js" },
      { img: "/images/skill/vue.png", title: "Vue.js" },
      { img: "/images/skill/nuxt.png", title: "Nuxt.js" },
      { img: "/images/skill/java.png", title: "JavaScripts" },
      { img: "/images/skill/html.png", title: "HTML" },
      { img: "/images/skill/bootstrap.png", title: "Boostrap 5" },
      { img: "/images/skill/jquery.png", title: "JQuery" },
      { img: "/images/skill/tailwind.png", title: "Tailwind CSS" },
      { img: "/images/skill/github.png", title: "Git & Github" },
      { img: "/images/skill/wp.png", title: "WordPress" },
      { img: "/images/skill/netlify.png", title: "Netlify" },
    ],
  },
  {
    tab_id: "soft",
    description:
      "Problem solving, team working, a good work ethic, good communication skills.",
    items: [],
  },
];

onMounted(() => {
  tpTabLine2();
});
</script>
