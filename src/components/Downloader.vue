<template>
  <div class="">
    <h1 class="heading">Youtube downloader</h1>
	<div class="controls">
	    <input class="URL-input" placeholder="https://www.youtube.com/watch?v=MtN1YnoL46Q" v-model="myurl">
    	<button class="convert-button" id="mp4" @click="convert('mp4')">Download video</button>
    	<button class="convert-button" @click="convert('mp3')" id='mp3'>Download audio</button>
	</div>
  </div>
</template>

<script>
export default {
  name: 'Downloader',
  data () {
    return {
      myurl: "",
      server: 'http://localhost:4000'
    }
  },
  methods: {
    convert(myformat) {
      window.location.href = `${this.server}/download`+myformat+`?url=${this.myurl}`;
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.controls {
    display: flex;
    flex-direction: row;
    justify-content: center;
    -ms-flex-pack: center;
    justify-content: center;
    align-items: center;
    grid-row-gap: 16px;
    flex-wrap: wrap;
}

html {
	height: 100%;
    background: #333;
}

* {
	text-align: center;
}

.heading {
	font-family: Arial;
	margin-top:40vh;
	color: #e5e5e5;
}

.URL-input, .convert-button {
	font-size:1.3em;
	padding:5px 10px;
}

.URL-input {
	border-radius:4px 0px 0px 4px;
	width:30em;
	text-align: left;
	border:2px solid #5a5959;
	outline:none;
	background: #4c4c4c;
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
