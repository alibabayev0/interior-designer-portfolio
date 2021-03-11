<template>
  <div class="header">
    <div class="line"></div>
    <p>GET IN TOUCH</p>
    <div class="line"></div>
  </div>
  <div class="container">
    <div class="info">
      <p class="info-text">
        It all starts with a conversation. Feel free to send us an email.
      </p>
      <div class="info-information">
        <div class="info-address">
          <p>Office</p>
          <p>
            GAAN LLC,<br />B.Vahabzada 46a,<br />
            Baku, Azerbaijan
          </p>
        </div>
        <div class="info-social">
          <div class="email">
            <p>General email:</p>
            <p>gunay.9r1@gmail.com</p>
          </div>
          <div class="call-us">
            <p>Call me</p>
            <p>+39 351 665 27 57 (IT)</p>
            <p>+994 50 243 44 00 (AZ)</p>
          </div>
        </div>
      </div>
    </div>
    <div class="contact">
      <div class="att-1" />
      <ul>
        <li>
          <a href="https://www.linkedin.com/in/gunaybabayeva/">
            <img src="../assets/linkedin.svg" width="24" height="24" />
          </a>
        </li>
        <li>
          <a href="mailto:gunay.9r1@gmail.com">
            <img src="../assets/gmail-logo.svg" width="24" height="24" />
          </a>
        </li>
        <li>
          <a href="https://www.instagram.com/gunaybabayeva16/">
            <img src="../assets/instagram.svg" width="24" height="24" />
          </a>
        </li>
        <li>
          <a href="tel:+39-351-665-27-57">
            <img src="../assets/phone.svg" width="24" height="24" />
          </a>
        </li>
      </ul>
      <div class="att-1" />
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
}

.header {
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  margin-top: 3em;
}

.header p {
  font-size: 2em;
  padding-left: 3%;
  padding-right: 3%;
  text-align: center;
  white-space: nowrap;
}

.header .line {
  width: 100%;
  height: 1px;
  right: 0;
  background-color: #928c00;
}

.container {
  display: flex;
  flex-wrap: wrap;
  padding: 5%;
  padding-left: 10%;
}

.container .info {
  display: flex;
  flex-direction: column;
  flex-grow: 2;
  max-width: 70%;
}

.container .contact {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  min-width: 30%;
}
.info-text {
  padding-bottom: 3vw;
  font-size: 1.5em;
  font-family: Poppins, sans-serif;
  max-width: 90%;
}

.info-information {
  display: flex;
  flex-wrap: wrap;
  min-width: 20%;
}

.info-address {
  flex-grow: 1;
}

.info-address p:first-child {
  font-size: 0.8em;
  color: gray;
}

.info-address p:last-child {
  line-height: 2;
}

.info-social {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.email {
  flex: 1;
}

.email p:first-child {
  font-size: 0.8em;
  color: gray;
}

.call-us {
  margin-top: 10px;
  flex: 1;
}

.call-us p:first-child {
  font-size: 0.8em;
  color: gray;
}

.contact {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: -4%;
}

.contact ul {
  list-style: none;
  margin-top: 15px;
  margin-bottom: 10px;
}

.contact .att-1 {
  width: 1px;
  height: 35%;
  background-color: #928c00;
}

@media (max-width: 575.98px) {
  .container {
    padding-bottom: 13%;
  }
}
</style>

<script>
export default {}
</script>
