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
            <li><span class="icon-check"></span> Product discovery and building what matters</li>
            <li><span class="icon-check"></span> Measuring to ensure updates are a success</li>
            <li><span class="icon-check"></span> And much more!</li>
          </ul>

          <form action="submit">
            <p><b>Email address</b></p>
            <v-text-field
              placeholder="email@company.com"
              type="email"
              variant="outlined"
              class="v-text"
              id="email"
            ></v-text-field>
            <button class="submit-button">Subscribe to monthly newsletter</button>
          </form>
        </div>
      </div>
    </div>
    <!-- Sign-up form end -->

    <!-- Success message start -->
    <div class="confirm__message">
      <img src="../../assets/images/icon-success.svg" alt="">
      <h2>Thanks for subscribing!</h2>
      <p>
        A confirmation email has been sent to <b>correo@company.com</b>. Please open it and click the
        button inside to confirm your subscription.
      </p>

      <button>Dismiss message</button>
    </div>
    <!-- Success message end -->
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

@font-face {
  font-family: 'Roboto-Bold';
  src: url('../../assets/fonts/Roboto-Bold.ttf');
}

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
  width: 85%;

  font-family: 'Roboto', sans-serif;
  src: url('../../assets/fonts/Roboto-Regular.ttf');
  font-size: 16px;
  color: black;

  h1 {
    font-family: 'Roboto-Bold', sans-serif;
    font-weight: 700;
    font-size: 3rem;
    color: hsl(235, 18%, 26%);
  }

  p {
    font-size: 16px;
  }

  &__signup {
    display: flex;
    flex-direction: row-reverse;
    justify-content: flex-end;

    img {
      width: 20rem;
      height: auto;
    }

    .__text {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;

      p {
        max-width: 20rem;
      }

      ul {
        margin-block-start: 0;
        padding-inline-start: 20px;
        margin-inline-end: 1rem;

        display: table;

        list-style-image: url(../../assets/images/icon-list.svg);

        li {
          ::marker {
            padding: 0;
            margin: 0;
            vertical-align: middle;
            display: inline-block;
          }
          padding-left: 1rem;
        }
      }
    }
  }

  .submit-button {
    background-color: hsl(235, 18%, 26%);
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    margin-top: 1rem;
    width: 350px;
    cursor: pointer;
  }
  .submit-button:hover {
    background-color: hsl(4, 100%, 67%);
  }

  .v-text {
    width: 350px;
    cursor: pointer;
  }
}

.confirm__message{
  background-color: white;
  display: flex;
  flex-direction: column;
  color: black;
  max-width: 25rem;
  align-items: center;
  padding: 3rem;
  border-radius: 15px;

  img{
    align-self: flex-start;
    width: 20%;
    height: 50%;
    margin: 5px;
  }

  h2{
    font-family: 'Roboto-Bold', sans-serif;
    font-weight: 700;
    font-size: 2rem;
    width: 100%;
    margin: 5px;
    color: hsl(235, 18%, 26%);
    line-height: normal;
  }

  p{
    font-size: 16px;
    margin: 5px;
    width: 100%;
  }

  button {
    background-color: hsl(235, 18%, 26%);
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    margin-top: 1rem;
    width: 100%;
    cursor: pointer;
  }
  button:hover {
    background-color: hsl(4, 100%, 67%);
  }

  
}
</style>
