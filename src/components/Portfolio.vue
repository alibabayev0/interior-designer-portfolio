<template>
    <div class="main">
        <div class="project-card">
            <div class="card-header">
                <img id="main-img" ref="main_img" :src="current_project.profile"/>
                <div id="header-right-column">
                    <div class="info">
                        <div>
                            <p>{{current_project.name}}</p>
                            <p>{{current_project.location}}</p>
                            <p>{{current_project.date}}</p>
                        </div>
                    </div>
                    <div class="owner">
                        <div>
                            <p>{{current_project.type}}</p>
                            <p>{{current_project.owner}}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="card-info">
                <div class="previous-project">
                    <button v-on:click="previous()" class="previous-button">
                        <img class="" src="../assets/arrow-right.svg"  width="32" height="32" alt="previos project"/>
                        <p>Previous</p>
                    </button>
                </div>

                <div class="description">
                    <p>{{current_project.description}}</p>
                </div>

                <div class="next-project">
                    <button v-on:click="next()" class="next-button">
                        <p>Next</p>
                        <img src="../assets/arrow-right.svg"  width="32" height="32" alt="previos project"/>
                    </button>
                </div>
            </div>
        </div>
        <div v-for="(item,name) in current_project.images" :key="name" class="gallery-card">
            <p class="card-name">{{name}}</p>
            <div class="card-images">
                <div class="card-image" v-for="images in item" :key="images">
                    <img :src="images" v-on:click="openImage(images,name)"/>
                </div>
            </div>
        </div>
    </div>

    <div id="myModal" class="modal" ref="modal">

        <!-- The Close Button -->
        <span class="close"  v-on:click="closeImage()">&times;</span>

        <!-- Modal Content (The Image) -->
        <div class="modal-content" >
            <img class="modal-content" id="img" ref="img">
            <!-- Modal Caption (Image Text) -->
            <div id="caption" ref="caption"></div>
        </div>
    </div>
</template>

<style scoped>

* {
    margin:0;
    padding:0;
}


.container {
    display: flex;
    position: relative;
}

.header{
    display: flex;
    flex-wrap: wrap;
    width: 100%;
}

.header .h-item{
    display: flex;
    align-items: flex-end;
    border-left: 2px solid #b8b8b8;
    border-right: 2px solid #b8b8b8;
    height: 200px;
    width: 18%;
    font-size: 1em;
    margin: 0% 0% 0% 10%;
    padding: 10px 5% 30px 50px;
    font-family: Poppins,sans-serif;
    color: black;
    font-size: 2em;
}


.project-card {
    display: flex;
    flex-direction: column;
    border-bottom: 1px solid #b8b8b8;
}

.card-header {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    flex:1;
}

.card-info {
    display: flex;
    width: 100%;
    flex:1;
}

#main-img {
    flex-grow:2;
    max-height: 350px;
    max-width: 100%;
}

#header-right-column {
    display: flex;
    width: 600px;
    min-width: 50%;
    min-height: 120px;
    flex:5;
}

.info {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-end;
    width: 300px;
    min-width: 20%;
    border: 1px solid grey;
    border-left: 0;
    border-top: 0;
    flex: 1;
    padding-top: 15px;
    padding-bottom: 15px;
}

.info div {
    margin: 0 0 30px 35px;
}

.info div p:first-child {
    font-size: 1.75em;
    font-weight: 900;
}

.info div p:not(:first-child) {
    font-size: 0.9em;
    color:#616161
}

.owner {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
    width: 300px;
    min-width: 20%;
    border: 1px solid grey;
    border-top: 0;
    border-left: 0;
    flex: 1;
}

.owner div {
    margin: 30px 0 0 40px;
}


.card-info {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
}

.previous-project, .description , .next-project {
    display: flex;
    height: 100px;
    justify-content: center;
    align-items: center;
}

.previous-project {
    display: flex;
    flex: 1;
}

.description {
    flex: 2;
    text-align: center;
    color:#616161
}

.next-project {
    height: 100%;
    flex: 1;
}

.previous-button, .next-button {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: transparent;
    border:0;
    cursor: pointer;
}

.previous-button img {
    margin-right: 7px;
    transform: rotate(180deg);
}

.next-button img {
    margin-left: 7px;
} 

.project-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-grow: 1;
}

.project-info p {
    font-family: Poppins,sans-serif;
    margin-top: 0.4%;
    margin-bottom: 0.4%;
}

.project-info .name {
    font-size: 2em;
}

.project-info .description{
    max-width: 60%;
    text-align: center;
}

.gallery-card {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    min-width: 46%;
    margin-left: 10%;
    border-left: 4px solid #b8b8b8;
    font-size: 2em;
    font-family: Poppins,sans-serif;
    padding-top: 1em;
}

.card-name {
    padding: 100px 100px 10px 40px;
    border-bottom: 4px solid #b8b8b8;
    width: 46%;
    max-width: 250px;
    text-transform: capitalize;
    flex:1;
    white-space: nowrap;
}

.card-images {
    display: flex;
    flex-wrap: wrap;
    flex:1;
    border-bottom-right-radius: 100px;
}

.card-image {
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    padding: 120px 40px 0 40px;
    width: 75%; 
    max-width: 350px;
    border-bottom: 4px solid #b8b8b8;
}

.card-image img{
    width: 100%; 
    border-radius: 5px 5px 0px 0px;
}

.card-images img:hover {
    opacity: 0.7;
}


.modal {
    display: none; /* Hidden by default */
    flex-direction: column;
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    justify-content: center;
    align-items: center;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    /* Black w/ opacity */
    background-color: rgb(0,0,0); /* Fallback color */
    background-color: rgba(0,0,0,0.9); 
    backdrop-filter: blur(8px);
}

.modal-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 800px;
}

.modal-content img {
    max-width: 800px;
}

#caption {
    display: flex;
    justify-content: center;
    text-align: center;
    color: #ccc;
    padding: 10px 0;
    height: 20px;
    font-size: 1.2em;
    text-transform: capitalize;
    font-family: Poppins,sans-serif;
}

.modal-content, #caption {
  animation-name: zoom;
  animation-duration: 0.5s;
}

@keyframes zoom {
  from {
    transform:scale(0);
  }
  to {
    transform:scale(1);
  }
}   

.close {
  position: absolute;
  top: 15px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}   






@media (max-width: 1245.98px) { 
    .info {
        align-items: center;
        padding-top: 20px;
        padding-bottom: 20px;
    }

    .info div {
        margin: 0 0 0 70px;
    }

    .owner {
        align-items: center;
    }

    .owner div {
        margin: 0 0 0 70px;
    }
}

@media only screen and (max-width: 700px){
  .modal-content {
    width: 100%;
  }
}

@media only screen and (max-width: 575.98px) { 
    .owner div {
        margin: 0;
        font-size: 0.8em;
    }

    .owner {
        justify-content: center;
    }

    .info div {
        margin: 0;
        font-size: 0.8em;
    }
    
    .info {
        justify-content: center;
    }
}
</style>


<script>
import projectData from '../assets/data/projects.json';
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
    methods:{
        next() {
            if(this.current_id + 1 == Object.keys(projectData).length){
                this.current_id = 0;
            }
            else {
                this.current_id = this.current_id + 1;
            }
            this.current_project = projectData[this.current_id]
        },
        previous() {
            if(this.current_id - 1 == -1){
                this.current_id = Object.keys(projectData).length - 1;
            }
            else {
                this.current_id = this.current_id - 1;
            }
            this.current_project = projectData[this.current_id]
        },
        openImage(src,alt) {
            this.$refs.modal.style.display = "flex";
            this.$refs.img.src = src;
            this.$refs.caption.textContent = alt;
        },
        closeImage() {
            this.$refs.modal.style.display = "none";
        }
    }
}
</script>
