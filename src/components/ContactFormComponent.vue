<template>
    <section class="contact-section">
      <h2>Contato</h2>
      <form @submit.prevent="submitForm" class="contact-form">
        <div>
          <label for="name">Nome:</label>
          <input type="text" id="name" v-model="form.name" required />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="form.email" required />
        </div>
        <div>
          <label for="message">Mensagem:</label>
          <textarea id="message" v-model="form.message" required></textarea>
        </div>
        <button type="submit">Enviar</button>
      </form>
      <p v-if="submitted">Mensagem enviada! Obrigado pelo contato.</p>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ContactComponent',
    data() {
      return {
        form: {
          name: '',
          email: '',
          message: ''
        },
        submitted: false
      }
    },
    methods: {
      submitForm() {
        // Aqui você pode adicionar a lógica para enviar os dados do formulário
        console.log(this.form);
        this.submitted = true;
  
        // Limpar o formulário
        this.form.name = '';
        this.form.email = '';
        this.form.message = '';
      }
    }
  }
  </script>
  
  <style scoped>
  .contact-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
  }
  
  .contact-form {
    width: 80%; /* Ajuste a largura conforme necessário */
    margin: 0 auto;
    text-align: left;
  }
  
  .contact-form div {
    margin-bottom: 15px;
  }
  
  .contact-form label {
    display: block;
    margin-bottom: 5px;
  }
  
  .contact-form input, .contact-form textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
  }
  
  .contact-form button {
    padding: 10px 15px;
    background-color: #007BFF;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .contact-form button:hover {
    background-color: #0056b3;
  }
  </style>

  
  
  