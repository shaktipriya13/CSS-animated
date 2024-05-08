# CSS-animated
<!DOCTYPE html>
<html>
<head>
	<title>Cube animation</title>
	<link rel="preconnect" href="https://fonts.gstatic.com">
	<link href="https://fonts.googleapis.com/css2?family=Reggae+One&display=swap" rel="stylesheet">
	<link rel="preconnect" href="https://fonts.gstatic.com">
	<link rel="preconnect" href="https://fonts.gstatic.com">
	<link href="https://fonts.googleapis.com/css2?family=Charm&display=swap" rel="stylesheet">

	<meta name="viewport" content="width=device-width,initial-scale=1">

	<style>
		body
		{
			background:#444;
		}
		#container
		{
			width:200px;
			height:200px;
			margin:auto;
			position:relative;
			top:200px;
			perspective:900px;

		}

		#cube
		{
			width:200px;
			height:200px;
			transform-style:preserve-3d;
			position:relative;
			transform:translateZ(-100px);
			-webkit-animation:twirl 15s infinite alternate;
			-moz-animation:twirl 15s infinite alternate;
			animation:twirl 15s infinite alternate;
		}
		.face
		{
			height:inherit;
			width:inherit;
			position:absolute;
			/*opacity:0.6;*/
			text-align:center;
			line-height:200px;
			font-family: 'Reggae One', cursive;
			font-size:17px;
			text-shadow:2px 1px 1px grey;
		}
		#front
		{
			background:#0DE0A5;
			transform:translateZ(100px);
		}
		#back
		{
			background:#807A62;
			transform:translateZ(-100PX) rotateY(180deg);
		}
		#top
		{
			transform:translateY(-100px) rotateX(90deg);
				background:#aff018;
			
		}
		#bottom
		{
			transform:translateY(100px) rotateX(-90deg);
			background:#E0419E;
		}
		#left
		{
			transform:translateX(-100px) rotateY(-90deg);
			background:rgb(8, 53, 185);
			background:#F7EB0A;
		}
		#right
		{
			transform:translateX(100px) rotateY(90deg);
		/*	background:#E03A0F;*/
			background:#1cf12d;
		}
		@-webkit-keyframes twirl
		{
			0%{
				-webkit-transform:rotate3d(0,0,0,0);
			}
			50%
			{
				-webkit-transform:rotateX(360deg) rotateY(360deg);
			}
			100%
			{
				-webkit-transform:rotateY(360deg);
			}

		}
		@-moz-keyframes twirl
		{
			0%{
				-moz-transform:rotate3d(0,0,0,0);
			}
			50%
			{
				-moz-transform:rotateX(360deg) rotateY(360deg);
			}
			100%
			{
				-moz-transform:rotateY(360deg);
			}

		}


		#side
		{
			height:350px;
		}
		@media (max-height:600px)
		{
			#side
			{
				height:210px;
			}
			#container
			{
				top:110px;
			}
		}
		h2
		{
			color:rgb(214, 19, 19);
			float:right;
			margin:20px;
			font-family: 'Charm', cursive;
			letter-spacing:2px;

		}
		

	</style>
</head>
<body>
	<div id="container">
		<div id="cube">
			<div id="front" class="face">Front</div>
			<div id="back" class="face">Back</div>
			<div id="top" class="face">Top</div>
			<div id="bottom" class="face">Bottom</div>
			<div id="left" class="face">Left</div>
			<div id="right" class="face">Right</div>
		</div>
	</div>

	<div id="side">
	</div>

	<h2>by ShaktiPriya </h2>


</body>
</html>
