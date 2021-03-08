<template>
  <div class="container">
    <div class="column-1 lc">
      <div class="profile-col">
        <img id="profile2" src="../assets/bctmuhwgee.jpg" alt="nothing">
        <img id="profile" src="../assets/ngcxixrqph.jpg" alt="nothing">
      </div>
    </div>
    <div class="column-1 rc">
      <div class="info">
        <div class="header">
          <p>About</p>
          <span></span>
        </div>
        <div class="description">
          I am an interior designer with 3+ years professional experience. Project management skills, strong background in space planning, technical drawing, knowledge of FF&E, 10 different design programs and being advanced speaker of 5 foreign languages make easier creation and presentation of my projects. As an interior designer, I always work on the new technologies and advanced techniques, trying to be inventive to make each pixel unique in every project I do. 
        </div>
      </div>
    </div>
  </div>
  <div class="main">
    <div class="left-container">
      <div class="card education">
        <div class="card-header">
          <p>EDUCATION</p>
          <span></span>
        </div>
        <div class="card-main">
          <div class="column-info">
            <p class="name">Master's in Interior and Spatial design</p>
            <p>IED University, Rome, Italy</p>
          </div>
          <p class="date">2014 - 2017</p>
        </div>
        <div class="card-main">
          <div class="column-info">
            <p class="name">Bachelor's in Interior design</p>
            <p>IED University, Rome, Italy</p>
            <ul>
              <li><p>Relevant courses: Material typology, color theory, drawing, Graphic design, Marketing, Modelling.</p></li>
              <li><p>Thesis design: "ZahAmaze". (grade(110/110))</p></li>
              <li><p>GPA: 29.11/30</p></li>
            </ul>
          </div>
          <p class="date">2014 - 2017</p>
        </div>
        <div class="card-main">
          <div class="column-info">
            <p class="name">Bachelor's in Interior design</p>
            <p>IED University, Rome, Italy</p>
          </div>
          <p class="date">2014 - 2017</p>
        </div>
      </div>
    </div>
    <div class="right-container">
      
    </div>
  </div>
</template>


<style scoped>
* {
  margin:0;
  padding: 0;
  font-family: Poppins,sans-serif;
}
.container,.main {
  display: flex;
  flex-wrap: wrap;
  margin: 3% 10% 0% 5%;
}

.column-1 {
  display: flex;
  flex-direction: column;
  flex:1;
}

.lc {
  align-items: center;
}

.rc {
  justify-content: center;
}

.profile-col {
  position: relative;
  min-height: 400px;
  min-width: 260.25px;
  border:2px solid black;
  padding:5px 10px 5px 10px;
}


.column-1 .header {
  flex:1;
}

.column-1 .description {
  flex:1;
  text-align: justify;
}

#profile {
  position: absolute;
  max-height: 400px;
  transform: rotate(5deg);
  -webkit-transition: opacity .25s ease-in-out;
  -moz-transition: opacity .25s ease-in-out;
  -o-transition: opacity .25s ease-in-out;
  transition: opacity .25s ease-in-out;
}

#profile:hover {
  opacity: 0;
}

#profile2 {
  position: absolute;
  max-height: 400px;
  transform: rotate(5deg);
}


.header{
  display: flex;
  align-items: center;
  font-size: 1.5em;
  font-weight: 900;
  margin-bottom: 30px;
}

.header span {
  width: 40px;
  margin-left: 15px;
  height: 2px;
  background-color: black;
}


.left-container {
  flex:1;
  min-width: 300px;
}

.right-container {
  flex:1;
}


.card-header {
  display: flex;
}

.card-header p{
  font-size: 1.5em;
  font-weight: 500;
}

.card-header span {
  margin-left: 15px;
  height: 2px;
  margin:auto;
  margin-left: 25px;
  background-color: #b8b8b8;
  flex-grow: 1;
}


.card-main {
  display: flex;
  flex-direction: row;
  margin-top: 14px;
  margin-bottom: 14px;
  padding: 3px;
}

.card-main .date{
  text-align: end;
  flex:1;
}


.card-main .column-info{
  display: flex;
  flex:1;
  flex-direction: column;
  align-items: flex-start;
}

.card-main .column-info .name {
  font-weight: 700;  
}

.card-main .column-info ul {
  margin-top: 15px;
  text-align: left;
}


@media (max-width: 768.98px) { 
 
}

@media (max-width: 768.98px) { 
  .container {
    flex-direction: column;
    justify-content: center;
    margin: 3% 1em 0% 1em; 
    margin-top: 40px;
  }

  .rc {
    margin: 40px 1em 0% 1em; 
  }
}
</style>


<script>

</script>
