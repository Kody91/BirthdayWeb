<template>
  <section class="hero-heading">
    <h1>Happy Birthday<span>!</span></h1>


  </section>
</template>

<style scoped>
.hero-heading {
  position: relative;
  z-index: 2;
  max-width: 43rem;
  padding: clamp(1.5rem, 5vw, 3.5rem);
  border: 1px solid rgba(255, 241, 220, 0.48);
  border-radius: 1.25rem;
  background: rgba(48, 29, 42, 0.58);
  box-shadow: 0 1.5rem 4rem rgba(35, 16, 29, 0.26);
  backdrop-filter: blur(9px);
  animation: rise-in 900ms ease both;
}


h1 {
  margin: 0;
  color: #fff7eb;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(3rem, 9vw, 7rem);
  font-weight: 400;
  letter-spacing: 2px;
  line-height: 1;
}

h1 span {
  color: #f4a6ad;
}


@keyframes rise-in {
  from { opacity: 0; transform: translateY(1.25rem); }
  to { opacity: 1; transform: translateY(0); }
}
</style>