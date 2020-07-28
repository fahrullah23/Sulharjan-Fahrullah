# Sulharjan-Fahrullah
Sulharjan Fahrullah - 1900018125 - C
<!DOCTYPE html>
<html>
<head>
	<title>Gallery</title>
	<link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">
	<img src="img/a.jpg" class="jumbo">
	<div class="thumbnail">

</div>
<div class="footer">
	CopyRight@SulharjanFahrullah
		<img src="img/a.jpg" class="thumb">
		<img src="img/b.jpg" class="thumb">
		<img src="img/c.jpg" class="thumb">
		<img src="img/d.jpg" class="thumb">
		<img src="img/e.jpg" class="thumb">
		<img src="img/f.jpg" class="thumb">
		
	</div>

</div>

<script src="script.js"></script>
</body>
</html> 





* {
	margin: 0;
	padding: 0;
	line-height: 0;
}

body {
	background-color: #ccc;
	text-align: center;
}

.container {
	width: 600px;
	margin: 10px auto;
	border: 5px solid white;
	overflow: auto;
}

.thumb {
	width: 200px;
	float: left; 
	border: 2px solid white;
	box-sizing: border-box;
}

.thumb:hover {
	opacity: 0.5;
	cursor: pointer;
}

@keyframes fadeIn {
	to {
		opacity: 1;
	}
}

.fade {
	opacity: 0;
	animation: fadeIn 0.5s forwards;
}

.active {
	opacity: 0.5;
}







const container = document.querySelector('.container');
const jumbo = document.querySelector('.jumbo');
const thumbs = document.querySelectorAll('.thumb');

container.addEventListener('click', function(e) {

	if( e.target.className == 'thumb'){

		jumbo.src = e.target.src;
		jumbo.classList.add('fade');
		setTimeout(function() {
			jumbo.classList.remove('fade');
		}, 500)

		thumbs.forEach(function(thumb){

			thumb.className = 'thumb';
		});   


		e.target.classList.add('active');

	}
});
