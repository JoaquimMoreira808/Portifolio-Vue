<template>
    <a
    :href="link"
    target="_blank"
    rel="noopener noreferrer"
    class="w-48 h-48 bg-white rounded-lg flex items-center justify-center shadow-md transition duration-300 hover:bg-[#47545e] cursor-pointer"
    >
    <img :src="img" :alt="alt" class="max-w-[70%] max-h-[70%]" />
    </a>
</template>

<script>
export default {
  name: 'Card',
  props: {
    img: { type: String, required: true },
    alt: { type: String, default: 'Imagem' },
    link: { type: String, required: true }
  }
}
</script>
