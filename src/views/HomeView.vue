<template>
  <main>
    <div class="w-[100vw] flex flex-col pt-0">
      <div class="w-[100%] text-center">
        <div
          class="text-4xl my-10 text-center w-[100%] text-gray-300 font-bold"
        >
          Willkommen beim SV Winterstettenstadt 1956 e.V.
        </div>
        <div class="w-100 max-w-[2500px] mx-auto relative">
          <img src="/images/erste_zweite_mannschaft.webp" class="hero-img" />
          <div
            class="w-100 h-[30px] md:h-[50px] absolute top-0 left-0 right-0 bg-gradient-to-b from-black to-transparent"
          ></div>
          <div
            class="w-100 h-[30px] md:h-[50px] absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black to-transparent"
          ></div>
        </div>
        <div class="text-3xl my-20 text-center font-serif text-white">
          Die Homepage des SV Winterstettenstadt 1956 e.V. wird derzeit
          überarbeitet.<br />
          Wir bitten um Geduld.
        </div>
      </div>
      <div class="hidden">
        <span class="text-md text-center font-serif mt-28 mb-5">
          Wir danken unseren Sponsoren:
        </span>

        <div class="bg-white">
          <div class="text-5xl pb-2 pt-5 border-b-4 border-black mb-24">
            Partner
          </div>

          <div class="grid grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
            <div v-for="sponsor in partner" :key="sponsor.name" class="my-4">
              <a
                class="flex flex-col justify-center h-[100%]"
                :href="sponsor.url"
                target="_blank"
              >
                <span class="text-xs text-left font-serif mb-3">
                  {{ sponsor.name }}
                </span>
                <div class="spacer"></div>
                <div class="flex items-center">
                  <img :src="sponsor.img" :alt="sponsor.name" />
                </div>
                <div class="spacer"></div>
              </a>
            </div>
          </div>
        </div>
        <div class="bg-white">
          <div class="text-5xl pb-2 pt-5 border-b-4 border-black my-24">
            Premium-Sponsoren
          </div>

          <div class="grid grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-8">
            <div v-for="sponsor in premium" :key="sponsor.name" class="my-4">
              <a
                class="flex flex-col justify-center h-[100%]"
                :href="sponsor.url"
                target="_blank"
              >
                <span class="text-xs text-left font-serif mb-3">
                  {{ sponsor.name }}
                </span>
                <div class="spacer"></div>
                <div class="flex items-center">
                  <img :src="sponsor.img" :alt="sponsor.name" />
                </div>
                <div class="spacer"></div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script setup>
import { computed } from "vue";

const sponsoren_wip = [
  {
    name: "Volksbank Ulm-BC",
    img: "/images/sponsoren/voba.png",
    url: "https://www.volksbank-ulm-biberach.de/startseite.html",
    priority: 1,
  },
  {
    name: "Kreissparkasse Biberach",
    img: "/images/sponsoren/ksk.svg",
    url: "https://www.ksk-bc.de/de/home.html",
    priority: 1,
  },
  {
    name: "EnBW",
    img: "/images/sponsoren/enbw.svg",
    url: "https://www.enbw.com/",
    priority: 1,
  },
  {
    name: "Fischer Edelstahltechnik",
    img: "/images/sponsoren/fischer.jpg",
    url: "https://fischer-edelstahltechnik.de/",
    priority: 1,
  },
  {
    name: "Mohr Maschinenservice",
    img: "/images/sponsoren/mohr.png",
    url: "https://mohr-maschinenservice.de/",
    priority: 1,
  },
  {
    name: "Steuerberatung Voltenauer",
    img: "/images/sponsoren/voltenauer.png",
    url: "https://www.stb-voltenauer.de/de/startseite/index.html",
    priority: 1,
  },
  {
    name: "Gerd Weiler Zahnarzt",
    img: "/images/sponsoren/weiler.png",
    url: "https://www.gerd-weiler.com/",
    priority: 1,
  },
  {
    name: "Schussenrieder Brauerei Ott",
    img: "/images/sponsoren/ott.png",
    url: "https://www.schussenrieder.de/de/",
    priority: 1,
  },
  {
    name: "Risstalmetzgerei Hartmann",
    img: "/images/sponsoren/risstal.png",
    url: "https://www.risstalmetzgerei.de/",
    priority: 1,
  },
  {
    name: "Sport Heinzel",
    img: "/images/sponsoren/heinzel.svg",
    url: "https://sport-heinzel.de/",
    priority: 1,
  },
  {
    name: "LC Top Handwerkersoftware",
    img: "/images/sponsoren/lctop.svg",
    url: "https://www.lc-top.de/",
    priority: 1,
  },
  {
    name: "Lemmle Gebäudetechnik",
    img: "/images/sponsoren/lemmle.jpg",
    url: "http://www.lemmle.de/",
    priority: 1,
  },
  {
    name: "KS Werbung",
    img: "/images/sponsoren/ks.jpg",
    url: "http://www.ks-werbung.biz/",
    priority: 1,
  },
  {
    name: "Manfred Löffler",
    img: "/images/sponsoren/loffler.jpg",
    url: "https://www.bauen-mit-loeffler.de/",
    priority: 1,
  },
  {
    name: "Utz Lebensmittel",
    img: "/images/sponsoren/utz.png",
    url: "https://www.utz-lebensmittel.de/",
    priority: 1,
  },
  {
    name: "Ehrhart Feuerschutz",
    img: "/images/sponsoren/ehrhart.webp",
    url: "https://www.ehrhart-feuerschutz.eu/",
    priority: 1,
  },
  {
    name: "Sodafixx",
    img: "/images/sponsoren/sodafixx.webp",
    url: "https://www.sodafixx.de/",
    priority: 1,
  },
  {
    name: "Trockeneis24",
    img: "/images/sponsoren/trockeneis.webp",
    url: "http://www.trockeneis24.eu/",
    priority: 1,
  },
  {
    name: "Curios Sandra Cleppien",
    img: "/images/sponsoren/curios.jpg",
    url: "https://curios-sc.de/",
    priority: 1,
  },
  {
    name: "a+b",
    img: "/images/sponsoren/ab.png",
    url: "https://asphalt-und-beton.de/",
    priority: 2,
  },
  {
    name: "Hummler Rolladen",
    img: "/images/sponsoren/hummler.webp",
    url: "https://rolladenhummler.wixsite.com/bertholdhummler/kontakt",
    priority: 2,
  },
  {
    name: "Baur + Gut",
    img: "/images/sponsoren/baurgut.jpeg",
    url: "https://baur-gut.de/",
    priority: 2,
  },
  {
    name: "Bochtler Innenausbau",
    img: "/images/sponsoren/bochtler.png",
    url: "https://www.trockenbauunternehmen.net/ingoldingen/bochtler-innenausbau-gmbh-aUO41d",
    priority: 2,
  },
  {
    name: "Diesch Busreisen",
    img: "/images/sponsoren/diesch.jpg",
    url: "https://diesch-gmbh.de/",
    priority: 2,
  },
  {
    name: "Metzler Werbung",
    img: "/images/sponsoren/metzler.png",
    url: "https://www.metzler-werbung.de/",
    priority: 2,
  },
  {
    name: "Allianz Ruttka",
    img: "/images/sponsoren/allianz.svg",
    url: "https://vertretung.allianz.de/rudolf.rutka/",
    priority: 2,
  },
  {
    name: "Möbel Grell",
    img: "/images/sponsoren/grell.png",
    url: "https://www.moebel-grell.de/",
    priority: 2,
  },
  {
    name: "B+K Baumaschinen",
    img: "/images/sponsoren/bk.svg",
    url: "https://www.buk-baumaschinen.de/",
    priority: 2,
  },
];

const partner = computed(() => {
  return sponsoren_wip
    .filter((e) => e.priority === 1)
    .sort((a, b) =>
      a.name.toUpperCase() > b.name.toUpperCase()
        ? 1
        : b.name.toUpperCase() > a.name.toUpperCase()
        ? -1
        : 0
    );
});

const premium = computed(() => {
  return sponsoren_wip
    .filter((e) => e.priority === 2)
    .sort((a, b) =>
      a.name.toUpperCase() > b.name.toUpperCase()
        ? 1
        : b.name.toUpperCase() > a.name.toUpperCase()
        ? -1
        : 0
    );
});

const classic = computed(() => {
  return sponsoren_wip
    .filter((e) => e.priority === 3)
    .sort((a, b) =>
      a.name.toUpperCase() > b.name.toUpperCase()
        ? 1
        : b.name.toUpperCase() > a.name.toUpperCase()
        ? -1
        : 0
    );
});

const sponsoren = [
  "Voba Ulm-BC",
  "KSK Biberach",
  "EnBW",
  "Fischer Edelstahltechnik",
  "Mohr Maschinenservice",
  "STB Voltenauer",
  "Zahnarzt Dr. Gerd Weiler",
  "Brauerei Ott",
  "Risstalmetzgerei Hartmann",
  "Sport Heinzel",
  "LC Top Christ",
  "Lemmle Gebäudetechnik",
  "KS-Werbung",
  "Manfred Löffler Bauunternehmung",
  "Utz Gmbh & Co KG",
  "Ehrhart Feuerschutz",
  "Sodafixx",
  "Trockeneis24",
  "Danner Logistik",
  "A+B",
  "Bäckerei Engel",
  "Wunschgarten Atelier",
  "Friedrich Meier Gebäudesystemt.",
  "Steuerberater Elmar Renz",
  "Hofladen Birgit Zinser",
  "Hummler Rolladen",
  "Baur & Gut",
  "Bochtler Innenausbau",
  "Raiba Bad Sch.-ried Ing.",
  "Maler Christ",
  "Landbäckerei Mohr",
  "Diesch Busunternehmen",
  "SV Sparkassenversicherung",
  "Auto Gebhart",
  "Metzler Werbung",
  "Renz & Gerner Kachelöfen",
  "Praxis für Physioth. Thomas Oberhaus",
  "Aral Tankstelle Ganal",
  "Rüdiger Ballmann Physiotherapie",
  "Allianz Rutka",
  "Landgasthof zur Linde",
  "Möbel Grell",
  "s`Fahrrädle Uwe Sproll",
  "B+K",
  "Stahlhandel Scheffold B.W.",
  "Waldseer Weinmarkt",
  "Ferienhof Tiergarten",
  "Weingut Schwarz GbR",
  "AGS Autohaus",
  "Raab Karcher",
  "Hörl+Hartmann Vertriebs GmbH",
  "Schweizer Sanitär",
  "Impuls Gesundheitszentrum",
  "BAG U.-dorf",
  "BMA Ing.",
  "Maurus BauPunkt GmbH",
  "Rinninger Kisslegg",
  "Zahnarzt Dr. Käßmeyer",
  "Fahrschule Gebhard",
  "Haus Regenta",
  "Friseurstüble Silvia Scheffold",
  "Landgasthof Grüner Baum",
  "Poldi Sport Gbr",
  "Getreidemühle W.-dorf",
  "Gärtnerei Moll",
  "Eis Cafe Fontana BW",
  "Pizzeria La Palma Bad Waldsee",
  "REWE Bad Sch.-ried",
  "Shell Station - Kessler O.-dorf",
  "Gerd König",
  "Farny Edelweissbrauerei",
  "Tobias Köhler Allianz",
  "serveria IT-Systemhaus",
  "Schmidinger Immobilien BC",
  "Auto Ott Mühlhausen",
  "Edeka Haidorf Oberessendorf",
  "Spedition Veeser",
  "Neue Werbepartner 18/19",
  "Fa. Luna Modeschmuck",
  "Restaurant Klosterhof",
  "Reutter Blechbearbeitung",
  "Werbe Wassmer",
  "Silvio`s Bauservice Bad Sch.-ried",
  "Modeecke BC",
  "Tewa",
  "Allianz Maucher & Betz OHG",
  "Krumbacher Sprudel",
  "Dennis Wiedergrün",
  "Banert Steuerberater BC",
  "Zimmerei Thoma U.-dorf",
  "Bestattungen Schmidberger Bad Sch.-ried Herr Fisel / Herr von Borstel",
  "Oberland Gruppe",
  "Mezger Gerüst G+M",
  "Kosmetik Käppeler",
  "Allianz GV Thomas Fessler",
  "Mostbesen Härle Dunzenhausen",
  "Curios Sandra Cleppien",
];
</script>

<style scoped>
img {
  width: 100%;
  max-height: 150px;
  height: auto;
  object-fit: contain;
}
.spacer {
  flex: 1;
}

.hero-img {
  width: 100%;
  height: auto;
  max-height: 1000px;
  object-fit: cover;
  object-position: top;
}

.gradient {
  background: rgb(0, 0, 0);
  background: linear-gradient(0deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 1) 100%);
}
</style>
