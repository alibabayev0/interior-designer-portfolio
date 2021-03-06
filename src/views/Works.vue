<template>
    <div class="container">
        <div class="header">
            <div class="h-item">
                Portfolio
            </div>
            <div class="h-item">
                Gunay Babayeva
            </div>
            <div class="h-item"></div>
            <div class="h-item"></div>
        </div>
    </div>
    <div class="main">
        <div class="project-card">
            <div class="previous-project">
                <img src="../assets/right-arrow.svg" width="48" height="48" alt="previos project"/>
                <p>Previous project</p>
            </div>
            <div class="project-info">
                <p class="name">Dream Space</p>
                <p class="location">Baku, Azerbaijan</p>
                <p class="description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, consectetur explicabo nostrum blanditiis cumque dolor ex modi earum fuga adipisci consequuntur illum dicta ducimus repudiandae nesciunt sed veritatis fugiat velit?</p>
            </div>
            <div class="next-project">
                <p>Next project</p>
                <img src="../assets/right-arrow.svg" width="48" height="48" alt="previos project"/>
            </div>
        </div>
        <div class="gallery-header">
            <p>Gallery</p>
        </div>
        <div class="gallery">
            
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
    width: 100%;
    border-bottom: 2px solid rgb(184, 184, 184);
}

.header .h-item{
    display: flex;
    align-items: flex-end;
    border-left: 2px solid rgb(184, 184, 184);
    height: 200px;
    width: 300px;
    font-size: 1em;
    margin: 0% 0% 0% 10%;
    padding-left: 10px;
    padding-bottom: 10px;
    font-family: Poppins,sans-serif;
    color: rgb(49, 49, 49);
    font-size: 1.5em;
    border-bottom: 2px solid rgb(184, 184, 184);
}

.header .h-item:first-child{
    background-color: rgb(49, 49, 49);
    color:white;
    padding-left: 20px;
}

.header .h-item:nth-child(2){
    height: 250px;
    white-space: nowrap; 
    margin:0;
    font-size: 1.1em;
    border-bottom: 0;
}

.header .h-item:nth-child(n+3){
    height: 100px;  
    border-bottom: 0;
}

.header .h-item:nth-child(4){
    height: 160px;  
}

.project-card {
    display: flex;
    flex-direction: row;
    padding-top: 4%;
    padding-bottom: 4%;
    border-bottom: 1px dashed black;
}

.previous-project, .next-project {
    display: flex;
    min-width: 20%;
    flex-grow: 1;
    align-self: center;
}

.previous-project {
    justify-content: flex-end;
    align-items: center;
}

.previous-project img {
    margin-right: 7px;
    transform: rotate(180deg);
}

.next-project{
    justify-content: flex-start;
    align-items: center;
}

.next-project img {
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

.gallery-header {
    display: flex;
    width: 100%;
    margin-left: 10%;
    border-left: 3px solid black;
    font-size: 2em;
    font-family: Poppins,sans-serif;
    padding-top: 1em;
}

.gallery-header p {
    padding-left: 1em;
    padding-right: 1em;
    border-bottom: 3px solid black;
}

.gallery {
    display: flex;
    margin-left: 10%;
    border-left: 3px solid black;
}

</style>


<script>
    export default {
        
    }
</script>
