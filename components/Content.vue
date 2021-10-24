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
          <h1>{{ Arbeitnehmer.header }}peter</h1>
          <div class="h-80 border border-black">
            {{ Arbeitnehmer.ersteSchritte }}
          </div>
          <div class="h-80 border border-black">
            {{ Arbeitnehmer.zweiteSchritte }}
          </div>
          <div class="h-80 border border-black">
            {{ Arbeitnehmer.dritteSchritte }}
          </div>
        </div>
      </div>
      <div v-else-if="currentContent === 'Arbeitgeber'">
        <div class="h-full">
          <h1>{{ Arbeitgeber.header }}peter</h1>
          <div class="h-80 border border-black">Content</div>
          <div class="h-80 border border-black">Content</div>
          <div class="h-80 border border-black">Content</div>
        </div>
      </div>
      <div v-else-if="currentContent === 'Temporarburo'">
        <div class="h-full">
          <h1>{{ Temporarburo.header }}peter</h1>
          <div class="h-80 border border-black">Content</div>
          <div class="h-80 border border-black">Content</div>
          <div class="h-80 border border-black">Content</div>
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
        header: "Drei einfache Scritte zu deinem neuen Job",
        ersteSchritte: "Erstellen dein Lebenslauf",
        zweiteSchritte: "Erstellen dein Lebenslauf",
        dritteSchritte: "Mit nur einem Klick bewerben",
        firstImage: "",
        secondImage: "",
        thirdImage: "",
      },
      Arbeitgeber: {
        id: 2,
        header: "Drei einfache Schritte zu deinem neuen Mitarbeiter",
        ersteSchritte: "Erstellen dein Unternehmensprofil",
        zweiteSchritte: "Erstellen ein Jobinserat",
        dritteSchritte: "Wahle deinen newuen Mitarbeiter aus",
        firstImage: "",
        secondImage: "",
        thirdImage: "",
      },
      Temporarburo: {
        id: 3,
        header: "Drei einfache Scritte zur Vermittlung neuer Mitarbeiter",
        ersteSchritte: "Erstellen dein Unternehmensprofil",
        zweiteSchritte: "Erhalte Vermittlungs-angebot von Arbeitgeber",
        dritteSchritte: "Vermittlung nach Provision oder Studentlohn",
        firstImage: "",
        secondImage: "",
        thirdImage: "",
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