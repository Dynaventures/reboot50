# 🎨 UI Kit & Frontend Guidelines – Generation Reboot

## 🧱 Struktur

UI-kitet fungerar som grund för utvecklingen av Reboot 50-webbplatsen. Det är anpassat för **Next.js + Tailwind CSS** och följer den designbrief vi tog fram. Målet är en varm, luftig och förtroendeingivande upplevelse.

---

## 🎨 Färgvariabler (Tailwind-konfiguration)

```js
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: '#3E7D7C',     // Dämpad blågrön
        secondary: '#DCD2C8',   // Sandbeige
        accent: '#EBA45E',      // Mjuk orange
        background: '#F7F7F7',  // Ljus bakgrund
        text: '#333333',        // Mörk grafit
      }
    }
  }
}
```

---

## ✍️ Typografi

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&family=Lato:wght@400;700&display=swap" rel="stylesheet">
```

**Rubriker:** Inter, 600–700 vikt
**Brödtext:** Lato, 400–500 vikt
**Citat:** Lato italic eller Source Serif Pro italic

**Tailwind-exempel:**

```html
<h1 class="text-4xl font-semibold text-primary mb-4">Från stillastående till nystart</h1>
<p class="text-lg text-text leading-relaxed">Du har redan allt du behöver – erfarenhet, omdöme och driv. Vi hjälper dig att sätta pricken över i:et.</p>
```

---

## 🧭 Layoutkomponenter

### 1️⃣ Fast toppmeny

```html
<header class="fixed top-0 left-0 w-full bg-white/80 backdrop-blur-md shadow-sm z-50">
  <nav class="max-w-6xl mx-auto flex justify-between items-center py-4 px-6">
    <div class="flex items-center space-x-3">
      <img src="/assets/logo-reboot.svg" alt="Reboot 50" class="h-8 w-auto">
      <span class="font-semibold text-primary text-xl">Generation Reboot</span>
    </div>
    <ul class="hidden md:flex space-x-6 text-text">
      <li><a href="#about" class="hover:text-primary">Om</a></li>
      <li><a href="#program" class="hover:text-primary">Programmet</a></li>
      <li><a href="#stories" class="hover:text-primary">Historier</a></li>
      <li><a href="#partners" class="hover:text-primary">Bli partner</a></li>
      <li><a href="#contact" class="hover:text-primary">Kontakt</a></li>
    </ul>
    <a href="#support" class="ml-6 bg-accent text-white font-medium px-4 py-2 rounded-lg shadow hover:bg-primary transition">Stöd oss</a>
  </nav>
</header>
```

---

### 2️⃣ Hero-sektion

```html
<section class="pt-28 pb-20 bg-gradient-to-r from-primary/10 via-secondary/20 to-white text-center">
  <div class="max-w-4xl mx-auto px-6">
    <h1 class="text-5xl font-semibold text-primary mb-6">Från stillastående till nystart</h1>
    <p class="text-lg text-text mb-8 leading-relaxed">Reboot 50 hjälper människor 50+ att hitta tillbaka till nyfikenhet, skaparlust och digital styrka – med AI som verktyg.</p>
    <a href="#pilot" class="bg-accent hover:bg-primary text-white px-6 py-3 rounded-lg text-lg font-medium shadow transition">Läs om piloten</a>
  </div>
</section>
```

---

### 3️⃣ Sektioner (Problem / Lösning / Berättelse / Vision)

```html
<section id="problem" class="py-20 bg-white">
  <div class="max-w-5xl mx-auto px-6">
    <h2 class="text-3xl font-semibold text-primary mb-4">Problemet</h2>
    <p class="text-lg text-text leading-relaxed">Sverige sitter fast i en paradox. Aldrig förr har vi haft så mycket erfarenhet – och aldrig förr har så många stått utanför arbetsmarknaden. Ålderismen är vår tysta samhällssjukdom.</p>
  </div>
</section>

<section id="solution" class="py-20 bg-secondary/30">
  <div class="max-w-5xl mx-auto px-6">
    <h2 class="text-3xl font-semibold text-primary mb-4">Lösningen</h2>
    <p class="text-lg text-text leading-relaxed">Vi vänder på perspektivet. Generation Reboot är en 30-dagars resa där människor 50+ återfår sin nyfikenhet och lär sig samarbeta med AI för att lösa riktiga problem.</p>
  </div>
</section>
```

---

### 4️⃣ Knappstilar

```css
.btn-primary {
  @apply bg-primary text-white px-5 py-2 rounded-lg font-medium hover:bg-primary/90 transition;
}

.btn-accent {
  @apply bg-accent text-white px-5 py-2 rounded-lg font-medium hover:bg-primary transition;
}
```

---

## 🧩 Bildrekommendationer

* **Hero:** ensamt skrivbord → värme & ljus (före/efter-känsla)
* **Sektioner:** dokumentär känsla, naturligt ljus, svenska miljöer
* **Färgton:** övergång från kallgrå till varmbeige genom hela sidan

---

## 📱 Responsivitet

* Menyn blir hamburgare vid <768px (Tailwind `md:hidden`).
* Textblock staplas vertikalt, CTA centreras.
* Bilder beskärs inte – använd `object-contain`.

---

## 🪙 CTA-texter (förslag)

| Kontext    | Text                        |
| ---------- | --------------------------- |
| Hero       | "Läs om piloten"            |
| Problem    | "Var med och gör skillnad"  |
| Programmet | "Anslut som partner"        |
| Footer     | "Jag vill stödja Reboot 50" |

---

## ✅ Sammanfattning

Detta UI-kit definierar ett lugnt, tillgängligt och värmande visuellt språk. Det är kontrasten till Fragsheets mörka gamingprofil: ljus, hoppfull och mänsklig. Designen ska inge förtroende hos 55+, samtidigt som den känns modern nog för myndigheter och filantroper.

> **Ledord:** Empati. Energi. Enkelhet.
