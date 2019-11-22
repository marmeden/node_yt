<template>
  <div class="">
    <h1 class="heading">My Own Youtube Downloader !</h1>
    <input class="URL-input" placeholder="https://www.youtube.com/watch?v=MtN1YnoL46Q"><button class="convert-button" id="mp4">Convert mp4</button><button class="convert-button" id='mp3'>Convert mp3</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
	text-align: center;
}

.heading {
	font-family: Arial;
	margin-top:40vh;
}

.URL-input, .convert-button {
	font-size:1.3em;
	padding:5px 10px;
}

.URL-input {
	border-radius:4px 0px 0px 4px;
	width:30em;
	text-align: left;
	border:2px solid #EEEEEE;
	background: #EEEEEE;
	outline:none;
}

.URL-input:focus {
	border:2px solid #0485ff;
}

.convert-button {
	border:2px solid #0485ff;
	background: #0485ff;
	color:white;
	transition: 0.15s;
}

.convert-button:hover {
	background: #016acc;
	border-color: #016acc;
}

#mp3 {
	border-radius:0px 4px 4px 0px;
}
</style>
