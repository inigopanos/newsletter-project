<template>
  <body>
    <div class="newsletter">
      <!-- Sign-up form start -->
      <div class="newsletter__signup">
        <img src="" alt="">
        <h1>Stay updated!</h1>
        <p>Join 60,000+ product managers receiving monthly updates on:</p>
        <ul>
          <li>Product discovery and building what matters</li>
          <li>Measuring to ensure updates are a success</li>
          <li>And much more!</li>
        </ul>

        <form action="submit">
          <p>Email address</p>
          <input type="text" name="email" id="" placeholder="email@company.com" />
          <button>Subscribe to monthly newsletter</button>
        </form>
      </div>

      <!-- Sign-up form end -->

      <!-- Success message start -->

      Thanks for subscribing! A confirmation email has been sent to ash@loremcompany.com. Please
      open it and click the button inside to confirm your subscription. Dismiss message

      <!-- Success message end -->

      <div class="attribution">
        Challenge by
        <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
        Coded by <a href="#">Your Name Here</a>.
      </div>
    </div>
  </body>
</template>

<script lang="ts">
export default {
  data() {
    return {
      email: ''
    }
  },
  methods: {
    submitForm() {
      // Handle form submission logic here
      // You can use the 'email' data property to access the entered email value
      // For example, you can make an API request to subscribe the user to the newsletter
    }
  }
}
</script>

<style scoped lang="scss">
body {
  background-color: hsl(235, 18%, 26%);

  display: flex;
  flex-direction: column;
  justify-content: center;
}

.newsletter {
  background-color: white;
  border-radius: 15px;
  color: red;
}
</style>
