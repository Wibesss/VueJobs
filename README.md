# VueJobs

VueJobs je web aplikacija koja za cilj ima demonstraciju prednosti, mana kao i načina kreiranja korisničkog interfejsa pomoću Vue.js framework-a.

## Sadržaj

- [Uvod](#uvod)
  - [Tehnologije](#tehnologije)
- [Instalacija i pokretanje projekta](#instalacija-i-pokretanje-projekta)
  - [Preduslovi](#preduslovi)
  - [Instalacija](#instalacija)
  - [Funkcionalnosti](#funkcionalnosti)
- [Vue.js](#vuejs)
  - [Šta je Vue.js](#šta-je-vuejs)
  - [Zašto Vue.js](#zašto-vuejs)
  - [Vue Komponente](#vue-komponente)
  - [Kreiranje Stanja i Podataka](#kreiranje-stanja-i-podataka)
  - [Vue Direktive](#vue-direktive)
    - [v-if](#v-if)
    - [v-for](#v-for)
    - [v-bind](#v-bind)
    - [v-on](#v-on)
    - [v-model](#v-model)
  - [Lifecycle Hooks](#lifecycle-hooks)
- [Zaključak](#zaključak)

---

## Uvod

VueJobs aplikacija je projekat koji je fokusirana na frontend kako bi demonstrirao moć Vue.js frameworka-a za kreiranje dinamičkih korisničkih interfejsa. Korisnici mogu da pretražuju oglase poslova dok kompanije mogu da dodaju svoje nove oglase. Projekat je kreiran kako bi na najbolji način pomogao developerima koji žele da nauče Vue.js framework ili onima koji žele da prošire svoje znanje u ovoj oblasti.

### Tehnologije

- [Vue.js](https://vuejs.org/)
- [TailwindCSS](https://tailwindcss.com/)
- [JSON Server](https://github.com/typicode/json-server)
- [Vite](https://vitejs.dev/)

---

## Instalacija i pokretanje projekta

Pratite sledeće korake kako bi lokalno pokrenuli ovaj projekat.

### Preduslovi

Potrebno je imati instalirane sledeće alate:

- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/) - dolazi uz Node.js

### Instalacija

1. Klonirati repozitorijum:
   ```bash
   git clone https://github.com/Wibesss/VueJobs.git
   ```
2. Pozicionirati se u direktorijumu projekta:
   ```bash
   cd VueJobs
   ```
3. Instalirati potrebne alate:
   ```bash
   npm install
   ```
4. Pokrenuti projekat i json server konkutrentno jednom naredbom:
   ```bash
   npm run start
   ```
5. Otvoriti web pretraživač i pristupiti aplikaciji na:
   http://localhost:3000/

### Funkcionalnosti

Projekat je kreiran na način kako bi pokrio sve osnovne funkcionalnosti Vue.js framework-a i na taj način veoma efikasno demonstrira prednosti i način rada ove tehnologije.

Pored funkcionalnosti projekat takodje pokriva i korišćenje svih CRUD operacija nad podacima u ovom framework-u, to jest implementirane su funkcije za:

- Keiranje oglasa
- Pribavljanje oglasa
- Ažuriranje oglasa
- Brisanje oglasa

Nakon pažljivog prelasaka ovog tutorijala možete se upozanti sa najvažnijim delovima ove tehnologije i onog što ćete koristiti u svim budućim Vue.js projektima tako da vam on daje sve ono što je potrebno da postante dobar Vue.js developer.

---

## Vue.js

U narednom delu će se govoriti više o samom Vue.js frameworku i njegovim karakteristikama

### Šta je Vue.js

Vue.js je progresivan JS framework pomoću koga je moguće kreirati korisničke interfejse ili single page aplikacije. Dizajniran je da bude jednostavan, fleksibilan i inkrementalno adaptibilan, što znači da možete početi da ga koristite za manje delove aplikacije a zatim postepeno proširiti njegovu primenu. Vue omogućava developerima da ga veoma lako integriraju u projekte svih veličina, bilo da samo dodajete neku interaktivnost već postojećoj web stranici ili kreirate kompleksnu web aplikaciju od početka. Sa svojom reactive data binding i component-based arhitekturom, Vue.js pomaže developerima da kreiraju dinamičke i interaktivne korisničke interfejse na jednostavan i efikasan način.

Vue.js je kreiran 2013. godine od strane developera pod imenom Evan You. Samim tim što ovaj framework nije kreiran od strane velikih kompanija kao što su Google ili Facebook kao ostali popularni alati, a još uvek poseduje ovako veliku popularnost, govori o tome koliko je on kvalitetan.

### Zašto Vue.js

Zašto bi koristili Vue umesto tehnologija kao što su React ili Angular?

- **Jednostavnost i Pristupačnost** - Vue.js je poznat po tome kako je jednostavan i lak za integraciju u postojećim projektima. Veoma je lak za učenje i to ga čini dostupnim developerima sa raznim nivoima iskustva, dozvoljavajući im da brzo počnu sa radom.
- **Fleksibilnost** - Vue.js je dizajniran da bude inkrementno adaptibilan, tako da ga je moguće postepeno dodavati postojećim projektima, bilo da pravite malu funkcionalnost ili kompletnu single-page aplikaciju, Vue.js se može skalirati bez problema kako bi se prilagodio bilo kom projektu i njegovim zahtevima. Takođe je moguće kreirati server-side renerovane i statičke web stranice sa Vue meta framework-om.
- **Performanse i Veličina** - Vue.js nudi jako dobre performanse zahvaljujući svom efikasnom render mehanizmu, uključujući i virtualni DOM. Dodatno, glavna biblioteka Vue framework-a je veoma mala, što doprinosi brzom inicijalnom učitavanju i boljim performansama u toku rada. Poznat je po tome što je jedan od najbržih frontend framework-a
- **Component-Based Arhitektura** - kao moderni frontend framework, Vue.js promoviše component-based arhitekturu. Koponente su odvojeni delovi koda koji mogu biti korišćeni više puta unutar iste aplikacije i omogućavaju lakše održavanje koda.
- **Aktivan Open-Source Community i Bogat Ekosistem Biblioteka** - Vue.js poseduje veoma aktivan open open-source community i bogat ekosistem biblioteka, alata, plugin-ova. Pored kreiranja single-page aplikacija, takođe postoje meta frameworks kao Nuxt.js koji omogućava server-side renderovanje ali i framework kao što je Grindsome, koji omogućava kreiranje statičkih web stranica.

### Vue Komponente

Kao i kod bilo kog drugog frontend JavaScript framework-a, Vue.js je izgrađen oko koncepta komponenata. Koponente su odvojeni delovi koda koji mogu lako da se integrišu u različite projekte. Vue komponente imaju veoma jednostavnu strukturu koja je podeljena u 3 delova a to su:

- Logički JavaScript deo, gde se definišu stanja, podaci kao i metodi, događaji, imports itd.
- Tamplete deo, koji se sastoji od HTML koda koji će biti renderovan ali pored toga poseduje i dinamičke elemente kao što su promenljive, petlje, uslovne promenljive koristeći Vue direktive.
- Stil deo, koji poseduje CSS koji može biti "scoped" to jest odnosi se samo na trenutnu komponentu u kojoj se nalazi.

U nastavku je jednostavan primer strukture Vue komponente:

```HTML
<script>
// Definisanje logike
</script>

<template>
  <!-- HTML kod koji će se renderovati -->
  <div>
    <h2>Vue.js!</h2>
    <p>Jednostavna Vue.js komponenta</p>
  </div>
</template>

<style scoped>
/* Scoped CSS za ovu komponentu */
</style>
```

### Kreiranje Stanja i Podataka

Većina komponenata će posedovati stanja ili podatke koji su sa njima povezani. Na primer, komponenta koja prikazuje listu poslova će imati niz poslova kao svoje podatke.

Primer definisanja stanja i podataka:

```javascript
<script setup>
import { ref } from 'vue';

const name = ref('John Doe');
const status = ref('active');
const tasks = ref(['Task One', 'Task Two', 'Task Three', 'Task Four']);
const link = ref('https://google.com');

const toggleStatus = () => {
  if (status.value === 'active') {
    status.value = 'pending';
  } else if (status.value === 'pending') {
    status.value = 'inactive';
  } else {
    status.value = 'active';
  }
};
```

### Vue Direktive

Vue poseduje specijalne atribute koji se nazivaju direktive i koje se mogu dodati HTML elementima kako bi promenile način na koji se ti elementi renderuju.
Neke od osnovnih direktiva su:

- **v-if** – renderuj element jedino ako je izraz tačan. Poseduje i v-else i v-else-if
- **v-for** – iterativno prolazi kroz neki niz elemenata i renderuje ih
- **v-bind** – povezuje neki atribut elementa sa nekim property-em komponente
- **v-on** – povezuje događaj sa metodom
- **v-model** – povezuje input sa nekim property-em komponente
- **v-show** – prikazuje ili krije element u zavisnosti od izraza

#### v-if

Korišćenjem podataka o statusu korisnika koje smo prethodno kreirali možemo koristi v-if direktivu kako bi odlučili koji od sledećih HTML elementa će biti renderovan.

```HTML
<h1 class="text-2xl">{{ name }}</h1>
<p v-if="status === 'active'" class="text-green-600">User is Active</p>
<p v-else-if="status === 'pending'" class="text-yellow-600">
    User is Pending
  </p>
<p v-else class="text-red-700">User is Inactive</p>
```

#### v-for

Korišćenjem liste tasks koju smo prethodno kreirali možemo koristi v-for direktivu kako bi za svaki elemenat liste bio renderovan poseban HTML element.

```HTML
<h3 class="text-xl my-3">Tasks:</h3>
<ul>
   <li v-for="task in tasks" :key="task" class="flex items-center my-3">
      {{ task }}
   </li>
</ul>
```

#### v-bind

Korišćenjem link promenljive koju smo prethodno kreirali možemo koristi v-bind direktivu kako taj link povezali sa HTML elementom.
Takodje je moguće koristi skraćenicu ove direktive tako što se ispred href atributa HTML elementa dodaju dve tačke ( : ).

```HTML
<a v-bind:href="link" class="text-blue-600">Link to Google</a>

<a :href="link" class="text-blue-600">Link to Google</a>
```

#### v-on

Pomoću v-on direktive možemo povezati funkciju toggleStatus sa specifičnim dogadjajem koji se može pojaviti.
Takodje je moguće koristi skraćeni zapis ove direktiva gde se ispred naziva dogadjaja koristi @.

```HTML
<button
  v-on:click='toggleStatus'
  class='mt-3 px-4 py-2 bg-blue-500 text-white rounded-md'
>
   Change Status
</button>

<button
  @click="toggleStatus"
  class="mt-3 px-4 py-2 bg-blue-500 text-white rounded-md"
>
   Change Status
</button>
```

#### v-model

Ako kreiramo promenljivu newTask pomoću funckije ref, možemo povezati tu promenljivu sa nekim inputom pomoću direktive v-model tako da ta promenljiva sada prati promene tog speficifčnog inputa.

```HTML
<div class="flex flex-col items-center mt-10">
    <h1 class="text-2xl">{{ name }}</h1>
    <p v-if="status === 'active'" class="text-green-600">User is Active</p>
    <p v-else-if="status === 'pending'" class="text-yellow-600">
      User is Pending
    </p>
    <p v-else class="text-red-700">User is Inactive</p>
    <button
      @click="toggleStatus"
      class="mt-3 px-4 py-2 bg-blue-500 text-white rounded-md"
    >
      Change Status
    </button>
    <h3 class="text-xl my-3">Tasks:</h3>
    <ul>
      <li v-for="task in tasks" :key="task" class="flex items-center my-3">
        {{ task }}
      </li>
    </ul>
    <a v-bind:href="link" class="text-blue-600">Link to Google</a>
  </div>
</template>
```

### Lifecycle Hooks

Vue framework poseduje specijalne funkcije koje se zovu lifecycle hooks. Ove funkcije se pozivaju u različitim momentima životnog ciklusa komponenata. Na primer, kada je komponenta kreirana, renderovana, ažurirana i uništena.

Neke od osnovnih su:

- **onBeforeMount** – pre renderovanja
- **onMounted** – pri renderovanju
- **onBeforeUpdate** – kada se reaktivni podatak promeni ali pre renderovanja
- **onUpdate** – pri re-renderovanju
- **onBeforeUnmount** – pre nego što se Vue instanca uništi
- **onUnmounted** – nakon što se Vue instanca uništi
- **onActivated** – kada se kept-alive komponenta aktivira
- **onDeactivated** – kada se kept-alive komponenta deaktivira
- **onErrorCaptured** – kada se pojavi greška u nekim child komponentama

## Zaključak

Vue.js je moćan, fleksibilan i pristupačan JavaScript framework koji omogućava brzo i efikasno razvijanje korisničkih interfejsa i SPA.

Intuitivan je za korišćenje i lak za učenje pa je dostupan velikom spektru developera.

Idealan je za manje projekta a može se koristi i u mnogo komplikovanim projektima tako da nudi ravnozežu izmedju jednostavnosti i funkcionalnosti.
