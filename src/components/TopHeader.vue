<template>
  <div class="header-top">
    <div class="container">
      <div class="box">
        <p>Vida toda</p>
        <p>BEM ESTAR</p>
        <p>Solução completas para viver mais e melhor</p>
        <button>Quero uma consultoria</button>
      </div>
      <form class="contact-form">
        <h3>Pronto para planejar o seu sossego?</h3>
        <p>Agente uma consultoria sem compromisso pelo formulário abaixo!</p>
        <div class="inputs">
          <label for="name">Nome:</label>
          <input type="text" id="name" />
          <label for="email">E-mail:</label>
          <input type="email" id="email" />
          <label for="marital-status">Estado Civil:</label>
          <input type="text" id="marital-status" />
          <label for="ocupation">Profissão:</label>
          <input type="text" id="ocupation" />
          <label for="phone">Telefone/Whatsapp:</label>
          <input type="phone" id="phone" />
          <label for="income">Renda Mensal</label>
          <input type="text" id="income" />
          <button type="submit" class="submit">Enviar</button>
        </div>
      </form>
    </div>
    <div class="card">
      <h3>Pense nisso...</h3>
      <p>
        O quanto antes o diagnóstico de uma doença grave, internação ou cirurgia
        inesperada pode afetar, hoje, sua vida pessoal ou financeira?
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
/* General style */
h3 {
  color: #ff9b23;
}

/* Header */
.header-top {
  padding: 0 0 1rem 8rem;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  position: relative;
  max-width: 1366px;
  min-width: 1250px;
  margin: auto;
}

/* Container  */
.container {
  display: flex;
  margin-top: 6rem;
}

/* Call to action box */
.box {
  border: 2px solid var(--default-bg);
  width: 33rem;
  padding: 3rem 4rem;
  font-size: 2.1rem;
  display: flex;
  flex-direction: column;
}
.box > p:nth-child(2) {
  font-size: 8.5rem;
  padding-bottom: 4rem;
  font-weight: 800;
  margin-left: -7px;
}
.box button {
  margin-top: 6rem;
  background-color: #ff9b23;
  color: #fff;
  padding: 1.5rem 1rem;
  font-size: 2rem;
}

/* Contact form */
.contact-form {
  background-color: var(--default-bg);
  padding: 2.5rem 2rem;
  height: 48rem;
  width: 26rem;
  align-self: flex-end;
  position: absolute;
  right: 9rem;
  color: #fff;
  display: flex;
  flex-direction: column;
  font-size: 1.4rem;
  top: 555px;
}
.contact-form h3 {
  font-size: 1.7rem;
}
.contact-form p {
  padding: 4rem 0;
}
.inputs {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.inputs > input {
  background-color: rgba(255, 255, 255, 0.466);
}
.submit {
  background: #ff9b23;
  border-radius: 16px;
  padding: 0.5rem 2rem;
  align-self: center;
  margin-top: 2.5rem;
}

/* Card */
.card {
  width: 50ch;
  padding: 4rem;
  margin-top: 4rem;
}
.card h3 {
  font-size: 2.5rem;
  padding: 1rem 0;
}
.card p {
  font-size: 1.4rem;
}
@media (max-width: 1250px) {
  .header-top {
    padding: 0 0 1rem 0;
    min-width: 100%;
  }
  .container {
    flex-direction: column;
    margin: auto;
  }
  .contact-form {
    position: relative;
    top: auto;
    right: auto;
    align-self: flex-start;
    margin: 1rem auto 0;
  }
  .card {
    margin: auto;
  }
}
@media (max-width: 998px) {
  .header-top {
    min-width: auto;
    padding: 0;
  }
  .header-top,
  .box,
  .contact-form {
    width: 100%;
  }
  .box {
    padding: 0 1.5rem;
  }
  .box button {
    width: 200px;
    font-size: 16px;
    margin-bottom: 1rem;
  }
  .contact-form {
    height: auto;
  }
  .card {
    margin-top: 0;
    width: auto;
  }
}
</style>
