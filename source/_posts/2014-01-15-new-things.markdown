---
layout: post
title: "New Things!"
date: 2014-01-15 09:12:30 +0800
comments: true
categories: 
---
<body>
<h1>Compass and SASS</h1>
<p>Recently, I learned how to use Compass and SASS. It is a great help for all the web developers out there. It gives them ease on doing or editing the CSS of their projects. It allows you to create mixins, makes it easy creating sprites, generates your CSS file fast, allows you to import css file to another css file so you'll just have to link 1 CSS file to your project. For a beginner like me, yes it benefits me a lot.</p>

<p>Compass is an open source application that uses SASS(Syntactically Awesome Style Sheets). SASS is an extension of CSS3 that allows you to nest rules, add variables, create mixins and etc. It is also the one who generates your CSS.</p>

<p>Examples of SASS Commands:</p>
<h2>Nested Rules</h2>
	#content{
		background-color:black;
		
	 	.box{
	 		background-color:black;
	 	}	

	}
<p> When compiled to CSS, it will look like this:</p>
	#content{
	background-color:black;
	}
	#content .box{
	background-color:black;
	}

<h2>Variables</h2>
	$black = #00000;
	$w = white; 

<p>Now you can use these variables anywhere on your project just don't forget to import it to the CSS file where you need to use it. You can simply type, <strong>@import 'name of the scss file';</strong>. You can use the variables like this:
	
	background-color:$black;
	color:$w;

<h2>Mixins</h2>
	@mixin myFont{
	font:{
		family:Arial;
		size:15px;
		weight:bold;
	}
 	}

<p>You can use it by using the <strong>@include</strong> method.</p>
	
	#pageHead{
	width:500px;
	text-align:center;
	@include myFont;
	}


<p>That's all for now. I'll update this blog again as soon as I learned something new! Thanks for reading! :)</p>
</body>