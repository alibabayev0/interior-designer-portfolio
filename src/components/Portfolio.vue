<template>
  <!-- <div class="main">
    <div class="project-card">
      <div class="card-header">
        <img id="main-img" ref="main_img" :src="current_project.profile" />
        <div id="header-right-column">
          <div class="info">
            <div>
              <p>{{ current_project.name }}</p>
              <p>{{ current_project.location }}</p>
              <p>{{ current_project.date }}</p>
            </div>
          </div>
          <div class="owner">
            <div>
              <p>{{ current_project.type }}</p>
              <p>{{ current_project.owner }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="card-info">
       

        <div class="description">
          <p>{{ current_project.description }}</p>
        </div>

        <div class="next-project">
          
        </div>
      </div>
    </div>
    <div
      v-for="(item, name) in current_project.images"
      :key="name"
      class="gallery-card"
    >
      <p class="card-name">{{ name }}</p>
      <div class="card-images">
        <div class="card-image" v-for="images in item" :key="images">
          <img :src="images" v-on:click="openImage(images, name)" />
        </div>
      </div>
    </div>
  </div> -->
  <div class="container">
    <div class="project-info">
      <div class="project-title">
        Dream House
      </div>

      <p class="sidebar">Location</p>
      <p>Example</p>
      <p class="sidebar">Owner</p>
      <p>Example</p>  
      <p class="sidebar">Date</p>
      <p>Example</p>      

      <div class="project-description">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nobis facilis nihil ullam quos eum expedita maiores veniam minima, dolores reprehenderit soluta architecto voluptatibus similique nulla perspiciatis magnam quisquam repudiandae veritatis!
      </div>

      <div class="project-nav">
         <div class="prev">
          <button v-on:click="previous()" class="previous-button">
            <img
              class=""
              src="../assets/arrow-right.svg"
              width="32"
              height="32"
              alt="previos project"
            />
            <p>Previous</p>
          </button>
        </div>
        <div class="next">
          <button v-on:click="next()" class="next-button">
            <p>Next</p>
            <img
              src="../assets/arrow-right.svg"
              width="32"
              height="32"
              alt="previos project"
            />
          </button>
        </div>
      </div>
    </div>
    <div class="project-content">
        <div class="project-header">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero nemo dicta saepe nesciunt ratione fugiat repudiandae 
        </div>
        <img class="project-item" src="../assets/item-1.jpg"/>
        <img class="project-item" src="../assets/item-2.jpg"/>
        <img class="project-item" src="../assets/item-3.jpg"/>
        <img class="project-item" src="../assets/item-4.jpg"/>
        <img class="project-item" src="../assets/item-5.jpg"/>
    </div>  
  </div>
  <div id="myModal" class="modal" ref="modal">
    <!-- The Close Button -->
    <span class="close" v-on:click="closeImage()">&times;</span>

    <!-- Modal Content (The Image) -->
    <div class="modal-content">
      <img class="modal-content" id="img" ref="img" />
      <!-- Modal Caption (Image Text) -->
      <div id="caption" ref="caption"></div>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  font-family: Poppins,sans-serif;
}

.container {
  display: flex;
  position: relative;
}

.project-info {
  display: flex;
  flex: 2;  
  flex-direction: column;
  position: sticky;
  max-height: 100vh;
  width: 100%;
  top: 0;
  padding-left:30px;
  padding-top: 30px;
  padding-right: 30px;
  border:1px solid black;
  border-top: 0;
}

.project-title { 
  font-weight: 900;
  font-size: 2em;
  text-transform: uppercase;
}

.sidebar:first-of-type { 
  margin-top: 40px;
}

.sidebar {
  font-weight: 600;
}

.project-description {
  margin-top: 40px;
  margin-bottom: 80px;
}


.project-content{
  display:flex;
  flex-direction: column;
  position: relative;
  justify-content: flex-start;
  width: 100%;
  margin-top: 100px;
  padding-left: 40px;
  padding-right: 40px;
  padding-bottom: 40px;
  border-top: 1px solid black;
  border-bottom: 1px solid black;
  flex: 5;
}

.project-header {
  font-weight: 900;
  font-size: 2.3vw;
  line-height: 95%;
  padding-top: 30px;
}

.project-item{
  margin-top: 5%;
}

.project-nav {
  display: flex;
  margin-top:25%;
  padding-bottom:5%;
}

.prev {
  display:flex;
  flex:1;
  justify-content: flex-start;
}

.next {
  display:flex;
  justify-content: flex-end;
  flex:1;
}


.previous-button,
.next-button {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: transparent;
  border: 0;
  flex:1;
  cursor: pointer;
}

.previous-button img {
  margin-right: 7px;
  transform: rotate(180deg);
}

.next-button img {
  margin-left: 7px;
}
/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (max-width: 1025px ) {
  .container{
    display: flex;
    flex-direction: column;
  }

  .project-info {
    position: static;
    width: auto;
    max-height: none;
  }

  .project-description {
    margin-bottom: 0px;
  }

  .project-content {
    display: flex;
    padding: 0px;
    margin-top: 0;
    border-top: 0;
  }

  .project-header {
    font-size: 22px;
    padding-left: 30px;
    padding-right: 30px;
    font-weight: 700;
  }

  .project-item {
    padding-left: 30px;
    padding-right: 30px;
  }

  .project-item:last-of-type{
    padding-bottom: 30px;
  }

}


</style>

<script>
import projectData from '../assets/data/projects.json'
export default {
  data() {
    return {
      current_project: {},
      current_id: 0
    }
  },
  created() {
    this.current_project = projectData[this.current_id]
  },
  methods: {
    next() {
      if (this.current_id + 1 == Object.keys(projectData).length) {
        this.current_id = 0
      } else {
        this.current_id = this.current_id + 1
      }
      this.current_project = projectData[this.current_id]
    },
    previous() {
      if (this.current_id - 1 == -1) {
        this.current_id = Object.keys(projectData).length - 1
      } else {
        this.current_id = this.current_id - 1
      }
      this.current_project = projectData[this.current_id]
    },
    openImage(src, alt) {
      this.$refs.modal.style.display = 'flex'
      this.$refs.img.src = src
      this.$refs.caption.textContent = alt
    },
    closeImage() {
      this.$refs.modal.style.display = 'none'
    }
  }
}
</script>
