<template>
  <body>
    <div class="newsletter">
      <!-- Sign-up form start -->
      <div class="newsletter__signup">
        <div class="__image">
          <img src="../../assets/images/illustration-sign-up-desktop.svg" alt="" />
        </div>

        <div class="__text">
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
      </div>

      <!-- Sign-up form end -->

      <!-- Success message start -->
      <!-- <div class="newsletter__message">
        <h2>Thanks for subscribing!</h2>
        <p>
          A confirmation email has been sent to ash@loremcompany.com. Please open it and click the
          button inside to confirm your subscription.
        </p>

        <button>Dismiss message</button>
      </div> -->
      <!-- Success message end -->
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
  margin: 1rem;
  padding: 1rem 1rem 1rem 2rem;

  font-family: 'Roboto', sans-serif;
  src: url('../../assets/fonts/Roboto-Regular.ttf');
  font-size: 16px;
  color: black;

  h1{
    font-family: 'Roboto', sans-serif;
    src: url('../../assets/fonts/Roboto-Bold.ttf');
    font-weight: 700 ;
  }

  &__signup {
    display: flex;
    flex-direction: row-reverse;

    img {
      width: 20rem;
      height: auto;
    }

    .__text {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;

      ul{
        margin-block-start: 0;
        padding-inline-start: 20px;
        margin-inline-end: 1rem;

        display: table;

        list-style-image: url(../../assets/images/icon-list.svg);

        li{
          ::marker{
            padding: 0;
            margin: 0;
          }
          padding-left: 1rem;
        }
      }
    }
  }
}
</style>
