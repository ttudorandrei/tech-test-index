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
          @click="currentContent = 'Temporarburo'"
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

    <div class="my-5" style="font-family: Lato">
      <!-- First section -->
      <div v-if="currentContent === 'Arbeitnehmer'">
        <h1 class="text-3xl text-center text-gray-600 font-medium px-3">
          {{ Arbeitnehmer.header }}
        </h1>

        <div class="h-full">
          <!-- first piece of news -->
          <div class="h-96 my-20 flex flex-col justify-center align-center">
            <img src="../assets/img/undraw-profile-data.png" class="mx-auto" />
            <div class="flex flex-wrap justify-around">
              <div class="w-50 text-9xl text-gray-400 font-medium">1.</div>
              <div class="w-50 text-2xl my-auto align-text-bottom">
                {{ Arbeitnehmer.ersteSchritte }}
              </div>
            </div>
          </div>

          <!-- second piece of news -->
          <div
            class="h-96 my-20 flex flex-col justify-around align-center"
            style="background-color: #e6fffa"
          >
            <div class="flex flex-wrap justify-center">
              <div class="w-50 text-9xl text-gray-400 font-medium">2.</div>
              <div class="w-50 text-2xl my-auto align-text-bottom">
                {{ Arbeitnehmer.zweiteSchritte }}
              </div>
            </div>
            <img src="../assets/img/undraw-task.png" class="mx-auto" />
          </div>

          <!-- third piece of news -->
          <div class="h-96 my-20 flex flex-col justify-around align-center">
            <div class="flex flex-wrap justify-center">
              <div class="w-32 text-9xl text-gray-400 font-medium">3.</div>
              <div class="w-52 text-2xl my-auto align-text-bottom">
                {{ Arbeitnehmer.dritteSchritte }}
              </div>
            </div>
            <img src="../assets/img/undraw-personal-file.png" class="mx-auto" />
          </div>
        </div>
      </div>

      <!-- Second section -->
      <div v-else-if="currentContent === 'Arbeitgeber'">
        <h1 class="text-3xl text-center text-gray-600 font-medium px-3">
          {{ Arbeitgeber.header }}
        </h1>

        <div class="h-full">
          <!-- first piece of news -->
          <div class="h-96 my-20 flex flex-col justify-center align-center">
            <img src="../assets/img/undraw-profile-data.png" class="mx-auto" />
            <div class="flex flex-wrap justify-around">
              <div class="w-50 text-9xl text-gray-400 font-medium">1.</div>
              <div class="w-50 text-2xl my-auto align-text-bottom">
                {{ Arbeitnehmer.ersteSchritte }}
              </div>
            </div>
          </div>

          <!-- second piece of news -->
          <div
            class="h-96 my-20 flex flex-col justify-around align-center"
            style="background-color: #e6fffa"
          >
            <div class="flex flex-wrap justify-center">
              <div class="w-50 text-9xl text-gray-400 font-medium">2.</div>
              <div class="w-50 text-2xl my-auto align-text-bottom">
                {{ Arbeitgeber.zweiteSchritte }}
              </div>
            </div>
            <img src="../assets/img/champion-pictogram.png" class="mx-auto" />
          </div>

          <!-- third piece of news -->

          <div class="h-96 my-20 flex flex-col justify-around align-center">
            <div class="flex flex-wrap justify-center">
              <div class="w-32 text-9xl text-gray-400 font-medium">3.</div>
              <div class="w-60 text-2xl my-auto align-text-bottom">
                {{ Arbeitgeber.dritteSchritte }}
              </div>
            </div>
            <img src="../assets/img/employee-cards.png" class="mx-auto" />
          </div>
        </div>
      </div>

      <!-- Third Section -->
      <div v-else-if="currentContent === 'Temporarburo'">
        <h1 class="text-3xl text-center text-gray-600 font-medium px-3">
          {{ Temporarburo.header }}
        </h1>

        <div class="h-full">
          <!-- first piece of news -->
          <div class="h-96 my-20 flex flex-col justify-center align-center">
            <img src="../assets/img/undraw-profile-data.png" class="mx-auto" />
            <div class="flex flex-wrap justify-around">
              <div class="w-32 text-9xl text-gray-400 font-medium">1.</div>
              <div class="w-52 text-2xl my-auto align-text-bottom">
                {{ Temporarburo.ersteSchritte }}
              </div>
            </div>
          </div>

          <!-- second piece of news -->
          <div
            class="h-96 my-20 flex flex-col justify-around align-center"
            style="background-color: #e6fffa"
          >
            <div class="flex flex-wrap justify-center">
              <div class="w-32 text-9xl text-gray-400 font-medium">2.</div>
              <div class="w-72 text-2xl my-auto align-text-bottom">
                {{ Temporarburo.zweiteSchritte }}
              </div>
            </div>
            <img src="../assets/img/undraw-job-offers.png" class="mx-auto" />
          </div>

          <!-- third piece of news -->
          <div class="h-96 my-20 flex flex-col justify-around align-center">
            <div class="flex flex-wrap justify-center">
              <div class="w-32 text-9xl text-gray-400 font-medium">3.</div>
              <div class="w-52 text-2xl my-auto align-text-bottom">
                {{ Temporarburo.dritteSchritte }}
              </div>
            </div>
            <img src="../assets/img/undraw-business-deal.png" class="mx-auto" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato&display=swap");
</style>



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
      },
      Arbeitgeber: {
        id: 2,
        header: "Drei einfache Schritte zu deinem neuen Mitarbeiter",
        ersteSchritte: "Erstellen dein Unternehmensprofil",
        zweiteSchritte: "Erstellen ein Jobinserat",
        dritteSchritte: "Wahle deinen neuen Mitarbeiter aus",
      },
      Temporarburo: {
        id: 3,
        header: "Drei einfache Scritte zur Vermittlung neuer Mitarbeiter",
        ersteSchritte: "Erstellen dein Unternehmensprofil",
        zweiteSchritte: "Erhalte Vermittlungs-angebot von Arbeitgeber",
        dritteSchritte: "Vermittlung nach Provision oder Studentlohn",
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