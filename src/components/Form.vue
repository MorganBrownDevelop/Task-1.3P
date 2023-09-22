<template>
    <div class="cta_banner">
      <div class="content_block">
        <h1>{{ heading }}</h1>
        <h2>{{ Subheading }}</h2>

        <form action="https://airform.io/morganbrown756@gmail.com" method="post">
          <input type="email" required name="Email" id="email" placeholder="Email...">
          <textarea name="Message" id="message" cols="30" rows="10" placeholder="Message..."></textarea>
          <input type="submit" value="Send Message">
        </form>
      </div>
    </div>
</template>

<script>
    export default {
    name: 'Banner',
    data() {
      return {
        heading: 'CONTACT US',
        Subheading: 'Fill out the form below',
      }
    }
  }
</script>

<style scoped>
    .cta_banner {
      width: 100%;
      height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .content_block {
      width: auto;
      height: auto;
    }
    form {
      margin: 30px 0 0 0;
    }
    input {
      appearance: none;
    }
    input[type="email"]
    {
      width: 100%;
      border: 1px solid #949393;
      background: none;
      color: #949393;
      padding: 8px;
      margin: 0 0 15px 0;
    }
    textarea
    {
      width: 100%;
      border: 1px solid #949393;
      background: none;
      color: #949393;
      resize: none;
      padding: 8px;
    }
    ::placeholder {
      color: #949393;
    }
    input[type="submit"]
    {
      border: 1px solid #949393;
      color: black;
      background: #949393;
      width: 100%;
      padding: 8px;
      transition: 0.25s ease;
      cursor: pointer;
      margin: 15px 0 0 0;
    }
    input[type="submit"]:hover {
      opacity: 0.6;
      font-weight: bold;
    }
</style>