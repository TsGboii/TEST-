<!DOCTYPE html>
<meta charset="utf-8">
<head>
        <title>Subreddit Network Graphs</title>
	<!-- sets the favicon to double party parrot -->
	<link rel="icon" href="https://i.redd.it/5ivdnx9xd05z.gif" type="image/gif" sizes="16x16">
</head>
<!--CSS styling-->
<style>
.lasso path {
    stroke: rgb(80,80,80);
    stroke-width:2px;
}
.lasso .drawn {
    fill-opacity:.05 ;
}
.lasso .loop_close {
    fill:none;
    stroke-dasharray: 4,4;
}
.lasso .origin {
    fill:#3399FF;
    fill-opacity:.5;
}
.not_possible {
    fill: rgb(200,200,200);
}
.possible {
    fill: #EC888C;
}
.selected {
    stroke: red;
}
body {
    /*constant zoom for the doge background no matter the scaling*/
    background:url('https://img.wallpapersafari.com/desktop/1920/1080/92/18/9CtzT0.jpg') no-repeat fixed;
    background-size: 127%;
    /*constant zoom for the doge background no matter the scaling*/
    color: white;
    font-family:'Comic Sans MS';
    text-shadow: 0px 0px 4px maroon;
    /*constant zoom for the doge background no matter the scaling*/
    padding-bottom:300px;
}
.centered {
    text-align: center;
}
.axis-label
{
    fill: black;
    font: 12px sans-serif;
}
svg {
    background-color:rgba(255, 255, 255, 0.85);
}
p {
    white-space: pre-wrap;
}
h1, h2 {
    left: 10px;
    font-size: 1.3em;
    font-weight: 100;
}
h2 {
    top: 30px;
    font-size: 1em;
}
/*changes the hyperlink colors*/
a:link {
    color: yellow;
}
a:visited {
    color: red;
}
.links line {
  stroke: #999;
  stroke-opacity: 0.6;
}
.nodes circle {
  stroke-width: 1.5px;
}
</style>
<body>
<div class="centered">
  	<!--Handles the party parrot conga line above the title-->
	<div class="partyparrots centered">
		<img src="https://i.redd.it/z0ybh0qd3y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/71v0c7414y3y.gif" width="100" />
		<img src="https://i.redd.it/147stqgf3y3y.gif" width="100" />
	</div>
	<!--Headers-->
	<h1>
		beautiful homework 5!
	</h1>
	<h2>
		brought to you by Jared Nussbaum
	</h2>
	<!--Handles the party parrot conga line below the title-->
	<div class="partyparrots ">
		<img src="https://i.redd.it/mpc092y83y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/i8garob53y3y.gif" width="100" />
		<img src="https://i.redd.it/1otch8oa3y3y.gif" width="100" />
	</div>
	<!--button to show and hide the party parrot title border-->
	<button id="btn" onclick="hideBirbs()">click for less party parrot</button>
	</div>
	<script>
		function hideBirbs() {
			//x is a list of the two class partyparrots elements
			var x = document.getElementsByClassName("partyparrots");
			//y is the button element
			var y = document.getElementById("btn");
			console.log(x);
			//changes the existence of the party parrot gifs and changes the button text
			if (x[0].style.display === "none") {
				for (var i = 0; i < x.length; i++) {
					x[i].style.display = "block";
				}
				y.innerHTML = "click for less party parrot"
			} else {
				for (var i = 0; i < x.length; i++) {
					x[i].style.display = "none";
				}
				y.innerHTML = "click for more party parrot"
			}
		}
	</script>
<p>
