<template>
<div class="">
		<!-- Shelf heading -->
    <ShelfHeading>
      <template v-slot:title>Welcome!</template>
      <template v-slot:subtitle>ContentShelf is brought to you by:</template>
    </ShelfHeading>

<!-- Profile card -->
  <div class="container-md mt-3 p-4 shadow-lg rounded" id="card-container">
    <div class="d-flex flex-row">
        <img src="https://i.imgur.com/gwmPxgs.png" class="mr-3 rounded img-fluid" id="portrait-img"/>
<!-- https://i.pinimg.com/originals/39/26/db/3926db089d7af5fa91711db1dbb82b7c.jpg -->
      <div id="info-section" class="text-left w-100">

        <div>
          <h1 id="heading-name">Sean Hickey</h1>
        </div>

        <div>
          <h6 id="heading-subtitle" class="font-italic">Full Stack Developer</h6>
        </div>
        
        <hr class=""/>

      <div class="container w-100">
        <div class="row">
    
        <!-- Left side -->
        <div class="col p-0">
          <h6 id="heading-name">Technologies:</h6>
          <ul>
            <li>Web (Vue, Express, Mongo, AWS)</li>
            <li>Mobile (Kotlin, Android SDK)</li>
            <li>Scripting (JavaScript, Python)</li>
            <li>Design (Adobe Suite)</li>
            <li>Audio (Ableton, FL Studio)</li>
          </ul>
        </div>

        <!-- Vertical rule -->

        <div class="h-100"></div>

        <!-- Right side -->
        <div class="col">
          <h6 id="heading-name">Projects:</h6>
          <ul>
            <li><a target="_blank" href="https://github.com/muzucode/ContentShelf">ContentShelf</a></li>
            <li><a target="_blank" href="https://github.com/muzucode/Morningstar-API-Addon">MorningStar API Addon</a></li>
            <li><a target="_blank" href="https://github.com/muzucode/MLB-BoxScore-Scraper">MLB Boxscore Webscraper</a></li>
            <li><a target="_blank" href="https://github.com/muzucode/NBA-RapidAPI-Pandas">NBA Odds Sentiment-Analyzer</a></li>
            <li><a target="_blank" href="https://github.com/muzucode/Immersify">Immersify Language Learning App</a></li>
          </ul>
        </div>

      </div>
      </div>
      


        

      </div>
    </div>
  </div>

</div>
</template>


<script>
// @ is an alias to /src
import CenterMessage from '@/components/CenterMessage.vue';
import ShelfHeading from '@/components/ShelfHeading';
export default {
  name: "Home",
	components: {
    ShelfHeading
	}
};
</script>

<style>
#img-tech{
  width: 100px;
}
#main-wrapper{
    height:80vh
}
#card-container{
  background-color: white;
  border: 0px solid #46939A;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
#heading-subtitle{
  color:#C65549;
}
#portrait-img{
  object-fit: cover;
  width:25%;
}
</style>