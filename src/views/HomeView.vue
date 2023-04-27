<template>
  <main>
    <div class="w-[100vw] flex flex-col items-center justify-center p-10">
      <div class="w-[100vw] p-16 bg-black text-white text-center">
        <span class="text-3xl text-center font-serif">
          Die Homepage des SV Winterstettenstadt 1956 e.V. wird derzeit
          überarbeitet.<br />
          Wir bitten um Geduld.
        </span>
      </div>
      <span class="text-md text-center font-serif mt-28">
        Wir danken unseren Sponsoren: <br />
        <span
          class="text-xs text-center font-serif mr-2"
          v-for="sponsor in sponsoren"
          :key="sponsor"
        >
          {{ sponsor }},
        </span>
      </span>
    </div>
  </main>
</template>

<script setup>
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
