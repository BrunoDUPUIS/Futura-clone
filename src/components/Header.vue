<template>
  <main>
    <div>
      <img src="../assets/logo-futura-dark.svg" alt="" />
    </div>
    <nav>
      <p>SCIENCES <font-awesome-icon :icon="['fas', 'angle-down']" /></p>

      <p>SANTE <font-awesome-icon :icon="['fas', 'angle-down']" /></p>

      <p>TECH <font-awesome-icon :icon="['fas', 'angle-down']" /></p>

      <p>MAISON <font-awesome-icon :icon="['fas', 'angle-down']" /></p>

      <p>PLANETE <font-awesome-icon :icon="['fas', 'angle-down']" /></p>
    </nav>
    <div><button>JE M'ABONNE</button></div>
  </main>
</template>
<style scoped>
h1 {
  color: white;
  font-weight: bold;
  font-size: 20px;
}
svg {
  color: white;
}
p {
  color: white;
}

main {
  padding: 10px 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* border: 1px solid blue; */
  background: linear-gradient(45deg, #be80ff, #6325ff);
}
nav {
  /* border: 1px solid red; */
  display: flex;
  gap: 25px;
  font-size: 12px;
}
button {
  background-color: #fbb10d;
  color: white;
  border: none;
  padding: 10px;
}
</style>
