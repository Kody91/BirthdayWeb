<script setup>
import Header from '../components/Header.vue';
</script>

<template>
  <main class="birthday-page">
    <div class="scene-wash"></div>
    <div class="petal petal-one">✦</div>
    <div class="petal petal-two">✦</div>
    <div class="buttons">
     <button class="b1">
      CLICK FOR A SURPRISE
     </button>
    </div>
    <Header/>
    
    <div class="floating-names" aria-label="Birthday wishes for Kitcute, Reya, Kit, and Kat">
      <span class="name name-one">Kitcute</span>
      <span class="name name-two">Reya</span>
      <span class="name name-three">Kit</span>
      <span class="name name-four">Kat</span>
    </div>
    <img class="flower-art flower-left" src="/flower-pastel.gif" alt="Pastel flowers floating beside the birthday message" />
    <img class="flower-art flower-right" src="/flower-pastel.gif" alt="Pastel flowers floating beside the birthday message" />
    <img class="kitty kitty-one" src="/kittyDance.gif" alt="A dancing kitten" />
    <img class="kitty kitty-two" src="/kittyDance.gif" alt="A dancing kitten" />
    <img class="kitty kitty-three" src="/kittyDance.gif" alt="A dancing kitten" />
    <img class="kitty kitty-four" src="/kittyDance.gif" alt="A dancing kitten" />
    <img class="kitty kitty-five" src="/kittyDance.gif" alt="A dancing kitten" />
    <img class="kitty kitty-six" src="/kittyDance.gif" alt="A dancing kitten" />
    <img class="kitty kitty-seven" src="/kittyDance.gif" alt="A dancing kitten" />
    <img class="kitty kitty-eight" src="/kittyDance.gif" alt="A dancing kitten" />
  </main>
 </template>

<style scoped>

.b1 {
  position: absolute;
  z-index: 2;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 1rem 2rem;
  font-size: 1.25rem;
  font-weight: bold;
  color: #fff;
  background-color: #f4a6ad;
  border: none;
  border-radius: 0.5rem;
  cursor: pointer;
  transition: background-color 220ms ease, color 220ms ease, box-shadow 220ms ease;
  animation: fade-in 10000ms ease both;
}

.b1:hover {
  color: #f4a6ad;
  background-color: #ffff;
  box-shadow: 0 0.5rem 1rem rgba(35, 16, 29, 0.2);
}

.birthday-page {
  position: relative;
  display: grid;
  min-height: 100vh;
  place-items: center;
  overflow: hidden;
  isolation: isolate;
  padding: 2rem;
  background: #3f2930 url('/background.png') center / cover no-repeat;
}

.scene-wash {
  position: absolute;
  z-index: -1;
  inset: 0;
  background:
    linear-gradient(90deg, rgba(31, 21, 30, 0.64) 0%, rgba(48, 29, 42, 0.24) 50%, rgba(34, 24, 31, 0.08) 100%),
    linear-gradient(0deg, rgba(31, 19, 26, 0.44), transparent 55%);
}

.floating-names {
  position: absolute;
  z-index: 1;
  inset: 0;
  pointer-events: none;
}

.name {
  position: absolute;
  display: grid;
  min-width: 5.25rem;
  min-height: 2.35rem;
  place-items: center;
  padding: 0.45rem 0.9rem;
  border: 1px solid rgba(255, 247, 235, 0.65);
  border-radius: 999px;
  color: #3f2930;
  background: #ffe8b7;
  box-shadow: 0 0.75rem 1.8rem rgba(40, 18, 27, 0.22);
  font-family: Georgia, 'Times New Roman', serif;
  font-style: italic;
  letter-spacing: 0;
  animation: float 6s ease-in-out infinite;
}

.name-one { top:15%; left: 20%; animation-delay: -1s; font-size: 3rem;}
.name-two { top: 17%; right: 20%; color: #fff8ee; background: #ce829c; animation-delay: -3.5s; font-size: 2.5rem;}
.name-three { bottom: 17%; left: 10%; color: #fff8ee; background: #668c78; animation-delay: -5s; font-size: 2rem;}
.name-four { right: 12%; bottom: 22%; background: #f1b27f; animation-delay: -2s;  font-size: 3rem}

.flower-art {
  position: absolute;
  z-index: 1;
  top: 4%;
  width: clamp(7rem, 15vw, 12rem);
  mix-blend-mode: screen;
  opacity: 0.88;
}

.flower-left {
  left: 31%;
  animation: flower-left-float 7s ease-in-out infinite -2s;
}

.flower-right {
  right: 31%;
  animation: flower-right-float 7s ease-in-out infinite -2s;
}


.kitty {
  position: absolute;
  z-index: 2;
  width: clamp(5rem, 10vw, 8.25rem);
  object-fit: contain;
  filter: drop-shadow(0 0.8rem 0.7rem rgba(24, 13, 18, 0.28));
}


.kitty-one { bottom: 4%; left: 3%; width: clamp(5.5rem, 12vw, 9rem); }
.kitty-two { top: 8%; left: 4%; width: clamp(4rem, 8vw, 6.5rem); transform: scaleX(-1); }
.kitty-three { top: 30%; left: 2%; width: clamp(4rem, 7vw, 6rem); }
.kitty-four { top: 10%; right: 4%; width: clamp(4.5rem, 9vw, 7rem); transform: scaleX(-1); }
.kitty-five { right: 3%; bottom: 5%; width: clamp(5rem, 10vw, 8rem); }
.kitty-six { right: 13%; bottom: 8%; width: clamp(3.5rem, 7vw, 5.5rem); transform: scaleX(-1); }
.kitty-seven { top: 43%; left: 16%; width: clamp(3.5rem, 7vw, 5.5rem); }
.kitty-eight { top: 49%; right: 17%; width: clamp(4rem, 8vw, 6.5rem); transform: scaleX(-1); }

@keyframes float {
  0%, 100% { transform: translateY(0) rotate(-2deg); }
  50% { transform: translateY(-0.8rem) rotate(2deg); }
}

@keyframes flower-left-float {
  0%, 100% { transform: translateY(0) rotate(-12deg) scaleX(-1); }
  50% { transform: translateY(-0.8rem) rotate(-7deg) scaleX(-1); }
}

@keyframes flower-right-float {
  0%, 100% { transform: translateY(0) rotate(12deg); }
  50% { transform: translateY(-0.8rem) rotate(7deg); }
}

@media (max-width: 640px) {
  .birthday-page { align-items: start; padding: 2rem 1rem 6rem; }
  .hero-heading { margin-top: 9vh; }
  .name-one { top: 5%; left: 5%; }
  .name-two { top: 12%; right: 5%; }
  .name-three { bottom: 13%; left: 4%; }
  .name-four { right: 5%; bottom: 17%; }
  .flower-left { left: 8%; width: 7rem; }
  .flower-right { right: 8%; width: 7rem; }
  .wish-note { bottom: 1rem; font-size: 0.65rem; }
}

@keyframes fade-in {
  from { opacity: 0 }
  to { opacity: 1 }
}
</style>