<template>
  <div class="form-container">
    <form v-on:submit.prevent="onSubmit" name="contact" netlify netlify-honeypot="bot-field" hidden>
      <input type="hidden" name="form-name" value="contact" />
      <label>Email:</label>
      <input type="text" name="name">
      <label>Message:</label>
      <textarea name="message"></textarea>
      <div netlify-recaptcha></div>
      <button type=”submit”>Send</button>
    </form>
  </div>
</template>

<script>
  export default {
    methods: {
      onSubmit: function ({target}) {
        var formData = new FormData(target);
        formData.append('form-name', 'contact')
        fetch('/', {
          headers: { "Content-Type": "application/x-www-form-urlencoded" },
          method: 'POST',
          body: formData
        })
      }
    }
  }
</script>

<style>
  .form-container {

  }

  .form-container form {
    display: flex;
    flex-direction: column;
  }

  .form-container input {
    display: flex;
    flex-direction: column;
  }
</style>
