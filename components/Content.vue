<template>
  <div class="mb-28">
    <nav
      class="
        flex
        w-full
        h-20
        my-30
        overflow-x-scroll
        text-xl text-green-600
        hide-scrollbar
      "
    >
      <span><div class="h-16 w-20"></div></span>
      <span
        ><button
          @click="currentContent = 'Arbeitnehmer'"
          class="
            w-72
            h-20
            align-middle
            border border-gray-300
            rounded-l-2xl
            focus:bg-green-300 focus:text-white focus:border-green-300
          "
        >
          Arbeitnehmer
        </button>
      </span>
      <span
        ><button
          @click="currentContent = 'Arbeitgeber'"
          class="
            w-72
            h-20
            align-middle
            border border-gray-300
            focus:bg-green-300 focus:text-white focus:border-green-300
          "
        >
          Arbeitgeber
        </button>
      </span>
      <span
        ><button
          @click="currentContent = 'Arbeitnehmer'"
          class="
            w-72
            h-20
            align-middle
            border border-gray-300
            rounded-r-2xl
            focus:bg-green-300 focus:text-white focus:border-green-300
          "
        >
          Temporarburo
        </button>
      </span>
      <span><div class="h-20 w-20"></div></span>
    </nav>

    <div>
      <div v-if="currentContent === 'Arbeitnehmer'">
        <div class="h-full">
          <div>
            <img src="../assets/img/section-1.png" width="100%" height="100%" />
          </div>
        </div>
      </div>
      <div v-else-if="currentContent === 'Arbeitgeber'">
        <div class="h-full">
          <img src="../assets/img/section-2.png" width="100%" height="100%" />
        </div>
      </div>
      <div v-else-if="currentContent === 'Temporarburo'">
        <div class="h-full">
          <img src="../assets/img/section-3.png" width="100%" height="100%" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Content",
  data() {
    return {
      currentContent: "Arbeitnehmer",
      Arbeitnehmer: {
        id: 1,
        image: "../assets/img/section-1.png",
      },
      Arbeitgeber: {
        id: 2,
        image: "~/assets/img/section-2.png",
      },
      Temporarburo: {
        id: 3,
        image: "~/assets/img/section-3.png",
      },
    };
  },
};
</script>

<style>
/* Hide scrollbar for Chrome, Safari and Opera */
.hide-scrollbar::-webkit-scrollbar {
  display: none;
}

.hide-scrollbar {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}
</style>