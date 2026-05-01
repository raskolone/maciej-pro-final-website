<div align="center">
  <img src="attached_assets/image.png" alt="Maciej.pro - Less noise. More language." width="100%" style="border-radius: 12px; margin-bottom: 20px;" />

  <h1>🚀 maciej.pro | Portfolio & EdTech Space</h1>
  
  <p>
    <strong>Nowoczesna, dwujęzyczna aplikacja SPA.</strong><br>
    Minimalistyczna wizytówka łącząca świat edukacji (Lektor / English Coach) ze światem technologii (EdTech Builder).
  </p>

  <p>
    <img src="https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React 19" />
    <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Tailwind_CSS_4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS 4" />
    <img src="https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E" alt="Vite" />
  </p>
</div>

<br />

## 🎯 O Projekcie

Repozytorium zawiera kod źródłowy mojej autorskiej strony internetowej **[maciej.pro](https://maciej.pro)**. 
Projekt powstał jako coś więcej niż tylko CV – to cyfrowy dowód moich kompetencji jako twórcy łączącego kod, sztuczną inteligencję i nowoczesne podejście do nauczania języka angielskiego.

Założeniem projektowym było stworzenie środowiska **"ADHD-friendly"** (mniej bodźców wizualnych, czystszy przekaz) w estetyce *Dark Editorial*. 

Aplikacja jest w pełni dwujęzyczna (PL/EN) i zbudowana jako Single Page Application (SPA) nastawiona na maksymalną wydajność i doskonały Developer Experience (DX).

---

## 🛠 Tech Stack & Architektura projektu

Budując ten projekt od zera, postawiłem na nowoczesne rozwiązania i stabilną architekturę, co pozwala na łatwe utrzymanie oraz skalowanie platformy (np. dodawanie nowych aplikacji EdTech w sekcji `/apps`).

*   **Frontend Framework:** React 19 (Hooks-first, functional components)
*   **Routing:** `wouter` – minimalistyczny, wyjątkowo lekki router (poniżej 2KB), optymalny dla płynnych SPA. Dodany smooth-scrolling pomiędzy zakotwiczeniami (`#sections`).
*   **Styling & Design System:**
    *   **Tailwind CSS 4** wykorzystywany do szybkiego prototypowania i utility-first styling.
    *   **OKLCH Color Space:** Zamiast tradycyjnego HEX/RGB użyłem przestrzeni barw OKLCH, co gwarantuje percepcyjną jednorodność kolorów i lepszy kontrast (szczególnie istotne przy czytelności tekstu w Dark Mode).
    *   Mieszana typografia edytorska: *Cormorant Garamond* (szeryfowe nagłówki) + *DM Sans* (czytelny tekst główny) + *DM Mono* (akcenty/kod).
*   **Komponenty Interaktywne:** Radix UI / shadcn (dostępne cyfrowo/ARIA kompatybilne elementy UI jak Accordion, Dialog, Forms).
*   **Narzędzia Build & Dev:** Vite + TypeScript (ścisłe typowanie dla bezpieczeństwa i refaktoryzacji).

---

## 🔍 Główne funkcjonalności (Pod lupą rekrutera)

Jako osoba techniczna, projektując aplikację, zadbałem o detale "pod maską", które świadczą o dojrzałości kodu:

### 1. Wydajne Animacje (Performance-First)
Zamiast obciążać główny wątek bibliotekami takimi jak React Spring ułomnymi dla prostych rzek, cała główna animacja tła ("Konstelacje") w komponencie `<ConstellationCanvas />` została napisana natywnie w **HTML5 Canvas API** z użyciem `requestAnimationFrame`. Gwarantuje to gładkie 60fps bez klatek (jank-free).

### 2. Scroll-Reveal z użyciem IntersectionObserver
Zaimplementowałem autorski mechanizm ujawniania sekcji (fade-in & stagger) bazujący na `IntersectionObserver`. Elementy DOM są animowane tylko wtedy, gdy wchodzą w viewport (lazy-reveal), co znacząco obniża narzut renderowania na urządzeniach mobilnych.

### 3. Własny kontekst i18n (Dwujęzyczność)
Zamiast "ciężkich" bibliotek typu `react-i18next`, stworzyłem leciutki, dedykowany `LanguageContext`. Komponenty same re-renderują się na podstawie wybranego języka, z zachowaniem bezstanowości w odświeżeniach, a sam tekst przesyłany jest przez zoptymalizowaną funkcję pomocniczą `t()`.

### 4. Semantic HTML & Dostępność (A11y)
Strona respektuje strukturę `main`, `section`, `nav`, `footer`. Elementy interaktywne posiadają znaczniki `aria-label`, focus rings dla nawigacji z klawiatury (Tab, Enter) pokryte logiką z `:focus-visible`. 

---

## 📸 Zrzuty ekranu (Showcase)

*Poniżej miejsce na dodanie faktycznych screenshotów z działającej aplikacji (wystarczy podmienić ścieżki do obrazów!)*

<div align="center">
  <table width="100%">
    <tr>
      <td width="50%" align="center">
        <b>Hero & Constellation Canvas</b><br/>
        <img src="https://via.placeholder.com/600x400/030805/00ff88?text=Hero+Section+Screenshot" alt="Hero Section" width="100%"/>
        <br/><em>Dynamiczne tło i efekt typewriter'a (Full Immersion Teacher).</em>
      </td>
      <td width="50%" align="center">
        <b>Metodologia (Bilingual UI)</b><br/>
        <img src="https://via.placeholder.com/600x400/030805/00ff88?text=Methodology+Section" alt="Methodology" width="100%"/>
        <br/><em>Przejrzyste, minimalistyczne karty dla sekcji O Mnie & Metoda.</em>
      </td>
    </tr>
    <tr>
      <td width="50%" align="center">
        <b>Cennik i FAQ</b><br/>
        <img src="https://via.placeholder.com/600x400/030805/00ff88?text=FAQ+%26+Pricing" alt="FAQ" width="100%"/>
        <br/><em>Dostępne z klawiatury komponenty Accordion.</em>
      </td>
      <td width="50%" align="center">
        <b>Cribro Apps Grid</b><br/>
        <img src="https://via.placeholder.com/600x400/030805/00ff88?text=EdTech+Apps+Grid" alt="Apps" width="100%"/>
        <br/><em>Sekcja aplikacji autorskich (m m.in. Cribro Journal).</em>
      </td>
    </tr>
  </table>
</div>

---

## 💻 Uruchomienie lokalne

Jeżeli chcesz przetestować kod osobiście, aplikacja jest banalna w instalacji dzięki Vite:

```bash
# Sklonuj repozytorium
git clone https://github.com/twoj-profil/maciej-portfolio.git

# Przejdź do folderu
cd maciej-portfolio

# Zainstaluj zależności
npm install  # (lub pnpm install)

# Uruchom tryb deweloperski
npm run dev
```
Główny punkt wejścia to `client/src/main.tsx`.

---

## 📬 Kontakt

Szukasz Programisty Front-End / UI Buildera z backgroundem filologicznym? Chcesz pogadać o optymalizacji apek, AI lub EdTechu?

*   🌐 Strona: [maciej.pro](https://maciej.pro)
*   📧 Email: [Złap mnie z formularza kontaktowego na stronie](https://maciej.pro) (obsługiwane przez Formspree)

<div align="center">
<br/>
<em>"Less noise. More Action."</em>
</div>
