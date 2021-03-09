<template>
  <div class="container">
    <div class="left-column">
      <p class="att-1">20' x 21'</p>
      <div class="att-2">
        <div class="att-arrow att-arrow-up-triangle" />
        <div class="att-arrow-up-line" />
        <p class="att-text">24</p>
        <div class="att-arrow-down-line" />
        <div class="att-arrow att-arrow-down-triangle" />
      </div>
      <div class="left-column-text">
        <p class="main-text">Hi,<br />I'am Gunay</p>
        <p class="main-text-desc">INTERIOR DESIGNER</p>
        <p class="main-text-intro">Welcome to my Personal Website...</p>
      </div>
      <!-- <div class="att-3">
        <div class="att-step-line"></div>
        <div class="att-step-line"></div>
        <div class="att-step-line"></div>
        <div class="att-step-line"></div>
        </div> -->
    </div>

    <div class="right-column">
      <img src="../assets/circle-cropped.png" />
    </div>
  </div>
</template>

<style lang="css" scoped>
* {
  padding: 0;
  margin: 0;
}

.container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}

.left-column {
  display: flex;
  position: relative;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  flex-grow: 2;
  padding: 10em 3em 10em 3em;
}

.left-column-text {
  margin-left: 40px;
}

.left-column .main-text-desc {
  color: #928c00;
  font-size: 1.3em;
  font-family: Poppins, sans-serif;
}

.left-column .main-text {
  color: #1c1c1d;
  font-size: 4em;
  font-weight: 900;
  font-family: Poppins, sans-serif;
  line-height: 60px;
  margin: 10px 0 30px 0;
}

.left-column .main-text-intro {
  font-family: Poppins, sans-serif;
  font-size: 2em;
}

.right-column {
  display: flex;
  justify-content: center;
  align-items: center;
  border-left: 1px solid black;
  border-right: 1px solid black;
  flex-grow: 2;
  max-width: 500px;
  margin-right: 3em;
  /* background:url(
data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAgAAAAICAYAAADED76LAAAAMklEQVQoU2NkwA/+M+KR/8/AwMCISwFYEqQZmwK4JDYFKJLoCjAkkRVglYQpwCkJUgAAGOQICDcTvB4AAAAASUVORK5CYII=
   ) repeat; */
}

.right-column img {
  border-top: 1px solid black;
  border-bottom: 1px solid black;
  max-width: 70%;
  max-height: 70%;
  padding: 15%;
  /* filter: grayscale(100%) ; */
}

.att-1 {
  display: block;
  position: absolute;
  right: 0px;
  top: 0px;
  padding: 10px 10px 10px 10px;
  text-align: center;
  font-family: Poppins, sans-serif;
  border-left: 1px solid black;
  border-bottom: 1px solid black;
}

.att-2 {
  position: absolute;
  left: 2em;
  margin-right: 2em;
}

.att-2 .att-arrow-up-line {
  width: 0.1em;
  height: 7em;
  margin-bottom: 0.9em;
  margin-left: 0.95em;
  background-color: #1c1c1d;
}

.att-2 .att-arrow-up-triangle {
  transform: rotate(-135deg);
  -webkit-transform: rotate(-135deg);
  margin-bottom: -0.55em;
}

.att-arrow {
  border: solid black;
  border-width: 0 2.5px 2.5px 0;
  padding: 3px;
  display: inline-block;
  margin-left: 11.5px;
}

.att-2 .att-arrow-down-triangle {
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
  position: absolute;
  margin-top: -4px;
}

.att-2 .att-arrow-down-line {
  width: 0.1em;
  height: 7em;
  margin-top: 15px;
  margin-left: 15px;
  background-color: #1c1c1d;
}

.att-2 .att-text {
  transform: rotate(-90deg);
  font-size: 1em;
  margin-left: 0.3em;
  font-family: Poppins, sans-serif;
}
/* 
.att-3 {
  position: absolute;
  bottom: 0;
  width: 100px;
  height: 100px;
  margin-left: 30%;
  border: 1px solid black;
  border-bottom: none;
  padding-top: 3px;
}


.att-3 .att-step-line {
  width: 100%;
  height: 1px;
  background-color: black;
  margin-top: 19px;
} */

@media (max-width: 575.98px) {
  .left-column {
    padding: 10% 10% 10% 10%;
    border-bottom: 1px solid black;
  }

  .left-column .main-text-desc {
    color: #928c00;
    font-size: 1.3em;
    font-family: Poppins, sans-serif;
  }

  .left-column .main-text {
    color: #1c1c1d;
    font-size: 3em;
    font-weight: 900;
    font-family: Poppins, sans-serif;
    line-height: 60px;
    margin: 10px 0 30px 0;
  }

  .left-column .main-text-intro {
    font-family: Poppins, sans-serif;
    font-size: 1.5em;
  }
}

/* Small devices (landscape phones, less than 768px) */
@media (max-width: 767.98px) {
}

/* // Medium devices (tablets, less than 992px) */
@media (max-width: 991.98px) {
}

/* // Large devices (desktops, less than 1200px) */
@media (max-width: 1265.98px) {
  .right-column {
    display: none;
  }
}
</style>

<script></script>
