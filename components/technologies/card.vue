<template>
  <div class="technology-card">
    <header>
      <slot name="logo" />
    </header>

    <div class="technology-card-overlay">
      <main class="text-xl font-bold">
        <slot />
      </main>

      <footer class="text-center text-sm italic">
        <slot name="area"></slot>
      </footer>
    </div>
  </div>
</template>

<style>
.technology-card {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0.25rem;
  padding: 1rem;
  cursor: pointer;
}

.technology-card-overlay {
  position: absolute;
  background-color: rgba(255, 255, 255, 0.85);
  inset: 0;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  justify-content: center;
  align-items: center;
}

.technology-card,
.technology-card > .technology-card-overlay {
  transition: all 0.5s ease-in-out;
}
.technology-card:hover {
  box-shadow: 0 5px 8px 0 rgba(0, 0, 0, 0.1);
}

.technology-card > .technology-card-overlay {
  opacity: 0;
}

.technology-card:hover > .technology-card-overlay {
  opacity: 1;
}
</style>
