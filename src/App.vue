<template>
  <div class="carnet">
    <aside>
      <div>
        <span>CEDULA DE INDENTIDAD</span>
        <img width="40" src="./assets/img/chile_bandera.png" alt="Bandera de Chile" />
      </div>
      <img src="./assets/img/foto_elon.jpg" alt="Imagen Elon">
      <p>RUN {{ run }}</p>
    </aside>

    <main>
      <header>
        <p>REPUBLICA DE CHILE</p>
        <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
      </header>
      <section>
        <article>
          <header>APELLIDOS</header>
          <span>{{ apellidos }}</span>
        </article>
        <article>
          <header>NOMBRES</header>
          <span>{{ nombres }}</span>
        </article>

        <div class="grid-2-colums">
          <article>
            <header>NACIONALIDAD</header>
            <span>{{ nacionalidad }}</span>
          </article>
          <article>
            <header>SEXO</header>
            <span>{{ sexo }}</span>
          </article>
        </div>
        <div class="grid-2-colums">
          <article>
            <header>FECHA DE NACIMIENTO</header>
            <span>{{ fechaNacimiento }}</span>
          </article>
          <article>
            <header>NÙMERO DOCUMENTO</header>
            <span>{{ numeroDocumento }}</span>
          </article>
        </div>
        <div class="grid-2-colums">
          <article>
            <header>FECHA DE EMISIÒN</header>
            <span>{{ fechaEmision }}</span>
          </article>
          <article>
            <header>FECHA DE VENCIMIENTO</header>
            <span>{{ fechaVencimiento }}</span>
          </article>
        </div>
        <article>
          <header>FIRMA DEL TITULAR</header>
          <span>{{ firmaTitular }}</span>
        </article>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      run: '22.222.222-2',
      apellidos: 'MUSK',
      nombres: 'ELON REEVE',
      nacionalidad: 'SUDAFRICANO',
      sexo: 'M',
      fechaNacimiento: '28 JUN 1971',
      numeroDocumento: '222.222.222',
      fechaEmision: '01 ENE 2025',
      fechaVencimiento: '01 ENE 2030',
      firmaTitular: 'X Æ A-12'
    };
  }
}
</script>

<style scoped>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60vh;
  font-size: 10px;
  font-family: sans-serif;
  margin: 0;
}

.carnet {
  width: 400px;
  height: 230px;
  background: #c8deed;
  border-radius: 20px;
  display: grid;
  grid-template-columns: 30% 1fr;
  padding: 15px;
  box-shadow: 0px 0px 10px 2px black;
}

aside {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  margin-right: 15px;
  font-size: 8px;
}

aside span {
  color: black;
}

aside div {
  display: flex;
  align-items: center;
  margin-bottom: 0;
}

aside>img {
  width: 100%;
  height: 100%;
  margin-top: 10px;
}

aside p {
  text-align: center;
  font-size: 11px;
  font-weight: bold;
  margin-top: 10px;
  color: black;
}

main {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

main header {
  text-align: left;
  margin: 0;
}

main header p {
  font-size: 20px;
  font-weight: bold;
  color: #0235a4;
  margin: -10px 0;
}

main header span {
  font-size: 8px;
  color: #399be1;
}

main section article header {
  font-weight: bold;
  color: #0235a4;
  font-size: 8px;
  margin-bottom: -9px;
}

main section article span {
  font-size: 13px;
  font-weight: 600;
  color: black;
}

main section .grid-2-colums {
  display: grid;
  grid-template-columns: 50% 50%;
  gap: 2px;
}
</style>
