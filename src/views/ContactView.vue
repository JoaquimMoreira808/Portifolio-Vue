<template>
  <BackButton />
  <div>
    <h1 class="pb-20 text-bold text-white text-6xl text-center">Contatos:</h1>
  </div>
  
  <div class="flex justify-center items-center gap-8">
    <CardComponent
      :img="GitLogo"
      alt="Logo do GitHub"
      link="https://github.com/JoaquimMoreira808"
    />
    <CardComponent
    :img="LinkedLogo" 
    alt="Logo do GitHub"
    link="https://www.linkedin.com/in/joaquim-moreira-03a10a2bb/"
    />
    <CardComponent
      :img="EmailLogo"
      alt="Logo do GitHub"
      link="malito:joaquimfernando808@gmail.com"
    />
  </div>

    <div class="mt-16 max-w-xl mx-auto text-white">
      <h2 class="text-4xl font-bold mb-6 text-center">Me envie uma mensagem direta</h2>
      <form @submit.prevent="enviarFormulario" class="space-y-6">
        <div>
          <label class="block mb-1">Nome</label>
          <input v-model="form.nome" type="text" class="w-full px-4 py-2 rounded bg-[#1e293b] text-white border border-gray-600" required>
        </div>
        <div>
          <label class="block mb-1">Email</label>
          <input v-model="form.email" type="email" class="w-full px-4 py-2 rounded bg-[#1e293b] text-white border border-gray-600" required>
        </div>
        <div>
          <label class="block mb-1">Mensagem</label>
          <textarea v-model="form.mensagem" rows="4" class="w-full px-4 py-2 rounded bg-[#1e293b] text-white border border-gray-600" required></textarea>
        </div>
        <button type="submit" class="bg-gradient-to-r from-[#20222e] to-[#7185eb] px-6 py-2 rounded text-white hover:opacity-50">
          Enviar
        </button>
      </form>
    </div>

</template>

<script>
import BackButton from '@/components/BackButtonComponent.vue'
import CardComponent from '@/components/CardComponent.vue'
import GitLogo from '@/imgs/gitlogo.png'
import EmailLogo from '@/imgs/EmailLogo.png'
import LinkedLogo from '@/imgs/LinkedLogo.png'

export default {
  name: 'ContactView',
  components: { CardComponent, BackButton },
  data() {
    return {
      GitLogo,
      EmailLogo,
      LinkedLogo,
      form: {
        nome: '',
        email: '',
        mensagem: ''
      }
    }
  },
  methods: {
    enviarFormulario() {
      console.log('Mensagem enviada:', this.form)
      alert('Mensagem enviada!')
  
      this.form.nome = ''
      this.form.email = ''
      this.form.mensagem = ''
    }
  }
}
</script>
